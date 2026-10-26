---
tags: [room0, production, hotel, gameplay]
status: current
updated: 2026-10-25
---

# Hotel Gameplay Markers

Everything the shift scripts can find in the Hotel place (placeId 133290122655457), by CollectionService tag. The hotel build (P+C, `rbxyta-assets/tools/studio_hotel/v2`, `Workspace.HotelV2`) creates all of these on every rebuild, so **read them, don't move or create them** from game code. Gameplay follows [[Shift Tasks]] and the Ordinary Guests notes ([[Ordinary Guests - Index]], [[Ordinary Guests - Activities and Encounters]]).

Markers are small invisible, anchored, non-colliding parts unless the table says the tag sits on a model. Use the marker's position (or the model's pivot) as the walk-to point.

## Staff
| Tag | On | Attributes | Where |
|---|---|---|---|
| `R0_StaffSpawn` | marker `R0_StaffSpawn_StaffRoom` | none | Staff Room (56, 1, 64) |
| `R0_ClockIn` | marker inside model `StaffRoom.TimeClock` | `Area = "StaffRoom"` | time clock on the Staff Room north wall, stand at (47, 1, 73.2) |
| `R0_GuestSpawn` | marker | none | vestibule (0, 1, 9): where arriving guests appear |

The player spawn is `Markers.Hotel_Spawn` in reception. The Staff Room is reached through the Staff Only door behind reception, then the staff corridor.

## Guest rooms
| Tag | On | Attributes |
|---|---|---|
| `R0_GuestRoom` | marker just inside each room door (`GameplayMarkers`) | `Room` ("101".."104"), `BedType` ("Double" or "Twin"), `Capacity` (number), `Theme` |

| Room | Theme | BedType | Capacity |
|---|---|---|---|
| 101 | Alpine Lodge (own bathroom) | Double | 2 |
| 102 | Art Deco | Double | 2 |
| 103 | Royal Burgundy (four-poster) | Double | 2 |
| 104 | Teal Retro | Twin | 2 |

- **No four-person room yet.** The road crew quartet (Dawn, Pete, Ivo, Kelly) cannot be booked until one exists: defer that booking (Ordinary Guests Design Bible). Planned next: Room 105 as a family room.
- Rooms 102-104 have no bathrooms yet (towels are still delivered to the room). Rooms 105-112 are empty shells; 110-112 are closed for renovation. Never book those or Room 214.
- The room folders `HotelV2.Room101`..`Room104` carry `Room`, `Theme` and `State = "Clean"`.

## Fixable objects (maintenance requests)
| Tag | On | Attributes |
|---|---|---|
| `R0_Fixable` | the object's model | `Kind`, `Room` |

`Kind` values, in every guest room 101-104:
- `ReadingLamp`: the bedside lamps and the desk lamp.
- `RoomBulb`: the ceiling light (101: the iron chandelier).
- `NoisyFixture`: the vent grille high on the south wall (it rattles).
- `Curtain`: the window drapes (101 has two windows).
- `Radiator`: under the window (101: on the corridor wall by the door).

Room 101 also keeps its older `R0_Task` spots (below), including the dripping tap.

## Reception
| Tag | On | Attributes |
|---|---|---|
| `R0_Reception` | model | `Point`: `Computer` (the front-desk CRT), `Register` (guest register), `Phone` (desk phone), `WakeUpLog`, `TransportLog` (the two log books on the desk) |
| `R0_KeyHook` | marker at each key on the key wall | `Room` ("101".."112"): one hook per room; 113 has no hook |

## Stock (deliveries and loans)
| Tag | On | Attributes |
|---|---|---|
| `R0_Stock` | marker at each stocked item on a shelf | `Item`, `Area` |

| Shelf | Area | Items |
|---|---|---|
| `StaffCorridor.LinenShelf` | Linen | Towels (2), Pillow (2), Blanket (2), Toiletries, Hangers |
| `StaffCorridor.EquipmentShelf` | Loans | Iron, SewingKit, Vase, Jug |
| `StaffCorridor.MaintenanceShelf` | Maintenance | Bulbs (2), Tools |

These are **placeholder shelves** in the staff corridor (east wall, z 34-56) until the Maintenance room, Linen Store and Laundry are built. The markers will move with them, so look them up by tag, not by position. Loan items (Iron, SewingKit, Vase, Jug) go back to the same shelf.

## Guest routines
| Tag | On | Attributes | Notes |
|---|---|---|---|
| `R0_Seat` | Sofa / Armchair / TubChair models in the Grand Lobby | `Area` (`SunkenLounge`, `ReadingNook`, `TeaTables`, `Gallery`, `Lobby`), `Seats` (sofa 3, others 1) | the lounge for now; the Lounge Bar room isn't built |
| `R0_Table` | the tea tables' round tables | `Area = "TeaTables"` | lounge games, map reading |
| `R0_DryingSpace` | marker inside model `WestHall.DryingRack` | `Area = "WestHall"` | coat rack and boot tray in the ground-floor West Hall (x -42, z 116-125) |

## Older tags (still there)
| Tag | Attributes | Notes |
|---|---|---|
| `R0_Task` | `TaskType`, `Room`, `Area` | 7 fixed spots: CheckIn (CRT), CCTV (CCTV bank), RoomCall (switchboard), Clean_Bed, Clean_Bin, Clean_Towels, Fix_Tap (Room 101). Each has an `Interact` part with a ProximityPrompt. No new ones are added. |
| `R0_CCTV` | `CameraId`, `CameraName` | 12 cameras; the feeds are GUI-only |
| `R0_EventSpot` | `Event` | ChandelierFlicker, PianoNote, CartMoves, DoorNumberChanges, RedWater, LaundryKnock, PowerCut, ExtraCorridor, Room113 |
| `R0_PredatorSpawn` | `Predator` | Bellhop, Housekeeper, VentCrawler, FacelessGuest |

Lighting zones: lights carry a `Zone` attribute ("Room 102", "Staff Room", ...) for power cuts and flicker.
