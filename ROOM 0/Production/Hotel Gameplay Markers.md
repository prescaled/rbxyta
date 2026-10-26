---
tags: [room0, production, hotel, gameplay]
status: current
updated: 2026-10-26
---

# Hotel Gameplay Markers

Everything the shift scripts can find in the Hotel place (placeId 133290122655457), and the runtime API that changes it. The hotel build (P+C, `rbxyta-assets/tools/studio_hotel/v2`, `Workspace.HotelV2`) creates all of this on every rebuild. Game code **reads** the markers and **changes the hotel only through `R0_HotelAPI`**. It never moves, deletes or rebuilds anything in HotelV2. Gameplay follows [[Shift Tasks]], [[First Shift Implementation]] and the Ordinary Guests notes ([[Ordinary Guests - Index]], [[Ordinary Guests - Activities and Encounters]]).

Markers are small invisible, anchored, non-colliding parts unless the table says the tag sits on a model. Use the marker's position (or the model's pivot) as the walk-to point. Verified in the live scene on 2026-10-26, layout check 0, API test all pass.

## Staff
| Tag | On | Attributes | Where |
|---|---|---|---|
| `R0_StaffSpawn` | marker `R0_StaffSpawn_StaffRoom` | none | Staff Room (56, 1, 64) |
| `R0_ClockIn` | marker inside model `StaffRoom.TimeClock` | `Area = "StaffRoom"` | time clock on the Staff Room north wall, stand at (47, 1, 73.2) |
| `R0_GuestSpawn` | marker | none | vestibule (0, 1, 9) |

The player spawn is `Markers.Hotel_Spawn` in reception. The Staff Room is reached through the Staff Only door behind reception, then the staff corridor.

## Guest rooms
| Tag | On | Attributes |
|---|---|---|
| `R0_GuestRoom` | marker just inside each room door (`GameplayMarkers`) | `Room`, `BedType`, `Capacity`, `Theme`, and `State` (set by the API) |

| Room | Theme | BedType | Capacity | Suits |
|---|---|---|---|---|
| 101 | Alpine Lodge (own bathroom) | Double | 2 | solos, couples |
| 102 | Art Deco | Double | 2 | solos, couples |
| 103 | Royal Burgundy (four-poster) | Double | 2 | solos, couples |
| 104 | Teal Retro | Twin | 2 | pairs needing separate beds (P02 Aisha and Tom) |
| 105 | Garden Room | Triple (a double and a single) | 3 | T01 the wedding trio |
| 106 | Writer's Room | Family (four single beds) | 4 | Q01 the road crew |

- `BedType` values: `Double`, `Twin`, `Triple`, `Family` (see `HotelTypes.BED_TYPES`).
- Rooms 102-106 have no bathrooms yet (towels are delivered to the room). Rooms 107-109 are empty shells; 110-112 are closed for renovation. Never book those or Room 214.
- The room folders `HotelV2.Room101`..`Room106` carry `Room`, `Theme` and `State`.

## Fixable objects (maintenance requests)
| Tag | On | Attributes |
|---|---|---|
| `R0_Fixable` | the object's model | `Kind`, `Room`, `State` (set by the API) |

`Kind` values, in every guest room 101-106:
- `ReadingLamp`: the bedside lamps and the desk lamp.
- `RoomBulb`: the ceiling light (101: the iron chandelier).
- `NoisyFixture`: the vent grille high on the south wall.
- `Curtain`: the window drapes (101 and 106 have two windows).
- `Radiator`: under the window (101: on the corridor wall by the door).

Room 101 also keeps its older `R0_Task` spots (below), including the dripping tap.

## Reception
| Tag | On | Attributes |
|---|---|---|
| `R0_Reception` | model | `Point`: `Computer` (the front-desk CRT), `Register` (guest register), `Phone` (desk phone), `WakeUpLog`, `TransportLog` (the two log books on the desk) |
| `R0_KeyHook` | marker at each key on the key wall | `Room` ("101".."112"), and `Present` (set by the API); 113 has no hook |

## Stock (deliveries and loans)
| Tag | On | Attributes |
|---|---|---|
| `R0_Stock` | marker at each stocked item on a shelf | `Item`, `Area`, `Count`, `Max` |

| Shelf | Area | Items (proposed count per point) |
|---|---|---|
| `StaffCorridor.LinenShelf` | Linen | Towels 6 (x2), Pillow 2 (x2), Blanket 2 (x2), Toiletries 6, Hangers 8 |
| `StaffCorridor.EquipmentShelf` | Loans | Iron 1, SewingKit 1, Vase 1, Jug 1 |
| `StaffCorridor.MaintenanceShelf` | Maintenance | Bulbs 4 (x2), Tools 1 |

These are **placeholder shelves** in the staff corridor (east wall, z 34-56) until the Maintenance room, Linen Store and Laundry are built. Look them up by tag, not by position. The shelf prop shows fewer pieces as `Count` falls, and nothing when it is empty.

## Guest routines
| Tag | On | Attributes | Notes |
|---|---|---|---|
| `R0_Seat` | Sofa / Armchair / TubChair models in the Grand Lobby | `Area` (`SunkenLounge`, `ReadingNook`, `TeaTables`, `Gallery`, `Lobby`), `Seats` (sofa 3, others 1), `TakenBy` (set by the API) | the lounge for now; the Lounge Bar room isn't built |
| `R0_Table` | the tea tables' round tables | `Area = "TeaTables"` | lounge games, map reading |
| `R0_DryingSpace` | marker inside model `WestHall.DryingRack` | `Area = "WestHall"` | coat rack and boot tray in the ground-floor West Hall (x -42, z 116-125) |

## Guest navigation (`HotelV2.GuestNav`)
| Tag | Attributes | Where |
|---|---|---|
| `R0_Arrival` | `Area = "Forecourt"` | (0, 1, -12), outside the revolving door |
| `R0_Exit` | `Area = "Forecourt"` | (5, 1, -12) |
| `R0_QueuePoint` | `Order` 1-3 | at the desk (1) and behind it (2, 3) |
| `R0_GuestPath` | `Route` (`"Main"` or a room number), `Order` | `Main` 1-9: reception west, lobby arch, lobby, stair foot, half landing, west upper flight top, gallery, corridor arch, corridor. Then one point outside each room door (`Route = "101"`..`"106"`) |

- Walk between points with PathfindingService using `HotelAPI.PATH_COSTS` (`{ GuestBlocked = math.huge, Door = 1 }`). `GuestNav.Blocked` holds volumes with a `PathfindingModifier` labelled `GuestBlocked`: StaffWing, Renovation (110-112), Ballroom, Kitchen and both service stairs. They are in collision group `R0_NavOnly`, so player raycasts pass through them.
- `HotelAPI.Route(room)` returns the whole chain of positions for a room. Tested: arrival → queue → every room 101-106 → exit all path; the staff room cannot be reached.
- **Room 0 is not built**, so it has no block volume yet. Add it with the area.

## Runtime API: `R0_HotelAPI`
`local API = require(game.ServerScriptService.R0_HotelAPI.HotelAPI)` (server only). Names and states for client UI: `ReplicatedStorage.R0_HotelAPI.HotelTypes`. Sources: `rbxyta-assets/tools/studio_hotel/v2/api`. Smoke test: `tests/api_test.lua`.

| Function | Does |
|---|---|
| `SetFixable(model, state)` | `Working`, `Broken`, `Flicker`, `Stuck`. Lamps and bulbs go dark or flicker; a curtain slides half across and hangs crooked; a vent's slats rattle with a looping rattle sound; a radiator turns dull grey (cold). `Working` restores the authored look exactly. Sets `State`. |
| `GetFixables(room?, kind?)`, `GetFixableState(model)` | find them |
| `SetRoomState(room, state)` | `Ready`, `InUse`, `Messy`, `Turnover`. Shows the room's authored traces: InUse = cups, used towels, a suitcase; Messy = those plus rubbish and an unmade bed; Turnover = Messy without the suitcase. `Ready` hides them all. |
| `GetRoomState(room)` | current state |
| `TakeStock(item, n?)` | takes from the fullest point and returns that `R0_Stock` marker (walk there), or nil when none are left |
| `ReturnStock(item, n?, marker?)`, `StockCount(item)`, `RestockAll()` | loans go back to the shelf they came from |
| `GetKey(room)` / `ReturnKey(room)` / `KeyOnHook(room)` | the fob disappears from or returns to its hook; GetKey returns nil if the key is already out |
| `GetDoor(room)`, `SetDoor(doorOrRoom, state, holdOpen?)` | `Open`, `Closed`, `Locked`, `Unlocked`. `Hotel_Systems.DoorServer` swings the leaf. Locked closes the door and disables its prompt. `holdOpen` stops the 20 s auto-close while a guest walks through. |
| `ClaimSeat(seat, who)` / `ReleaseSeat(seat, who)` | reserve lounge seats before walking a guest there |
| `Route(room)` | waypoint positions from reception to inside the room door |
| `CloneProp(name)` | a copy of a carry prop from `ServerStorage.R0_PortableProps`: TowelStack, Pillow, Blanket, Hangers, Iron, SewingKit, Vase, Jug, Bulb, Toolbox, RoomServiceTray, Key. Each is unanchored, non-colliding and massless, welded to its `Handle` (the PrimaryPart). Parent clones in your own runtime folder. |

## Older tags (still there)
| Tag | Attributes | Notes |
|---|---|---|
| `R0_Task` | `TaskType`, `Room`, `Area` | 7 fixed spots from the first draft: CheckIn, CCTV, RoomCall, Clean_Bed, Clean_Bin, Clean_Towels, Fix_Tap (Room 101). Each has a ProximityPrompt. Not used by the v3 shift; no new ones are added. |
| `R0_CCTV` | `CameraId`, `CameraName` | 12 cameras; the feeds are GUI-only |
| `R0_EventSpot` | `Event` | ChandelierFlicker, PianoNote, CartMoves, DoorNumberChanges, RedWater, LaundryKnock, PowerCut, ExtraCorridor, Room113 |
| `R0_PredatorSpawn` | `Predator` | Bellhop, Housekeeper, VentCrawler, FacelessGuest |

Lighting zones: lights carry a `Zone` attribute ("Room 102", "Staff Room", ...) for power cuts and flicker.
