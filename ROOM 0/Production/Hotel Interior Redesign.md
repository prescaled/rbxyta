---
tags: [room0, production, hotel, art]
status: decided-direction
---

# Hotel Interior Redesign (v2)

**Decided 2026-10-25 by the user:** the first hotel build looked bad. Every room looked the same, objects seemed randomly placed, walls had gaps, and the corridors were cramped. The whole interior gets a **full redesign of every model and room**. The floor plan from the brief stays as a starting point, but it gets wider. The ROOM 0 game ideas all stay: [[Shift Tasks]], [[Guests]], [[Hotel Shop]], [[CCTV System]], [[Strange Events]], [[Anomalies]], [[End of Shift Inspection]], [[Classes]], [[Health]].

## The target feel
**A first-person game inside a hotel, with the hand-built, detailed "quest room" look of good Roblox interiors.** You play a night-shift worker doing the shift tasks, looking after guests and noticing things that are wrong. Every room should feel like a hand-built level with its own identity, things to look at, and a reason to be there.

Reference images (style, not layout): `rbxyta-assets/reference/style/hotel_ref_01-03.png`, also in project files under `roomzero-style/hotel/`:
1. **Grand lounge-lobby** (ref 01). A double-height space split into zones: round tables with green velvet tub chairs on bold patterned rugs, a sunken lounge with glowing step edges, a central fireplace column, sputnik chandeliers and lantern pendants, a mezzanine with railings, tall windows and a skylight at night, ivy hanging from above, slatted wooden ceilings. Lots of depth and layering.
2. **Art deco reception** (ref 02). Red carpet, black marble pillars, gold stepped deco arches, a glowing neon sign over the desk, a brass luggage trolley, wall sconces.
3. **Retro diner / restaurant** (ref 03). Checkered floor, booths, a counter with stools, bare bulb pendants, glowing ceiling panels, real food, candles and bottles on the tables, framed photos, red trim lines.

What these have in common, and what our build lacked:
- **Every room has its own theme, palette and signature piece.** No copy-paste rooms.
- **It's layered**: floor pattern, then rug, then furniture group, then props on the furniture, then wall art, then ceiling detail, then light fixtures.
- **Light comes from things you can see**: glowing ceiling panels, pendants, lamps, neon, fireplaces, step strips. Warm pools of light with contrast, readable but moody.
- **Props tell you what happens here**: food on plates, open books, keys, a ledger, a ringing phone.
- **Clean construction**: walls meet perfectly, nothing floats, nothing clips, everything sits on a grid.

Our identity still applies: an old, half-abandoned grand mountain hotel at night, spooky but not Halloween, with burgundy, brass gold and deep teal ([[Art Bible]]). The decay is now **selective**: the public rooms are kept up by the night staff, and decay shows in closed and forgotten areas.

## First-person rules
- The game is played in **first person** by default (LockFirstPerson, or a toggle). Design every room at eye level, about 4.5 studs high.
- Detail must hold up close: table tops, desk surfaces, door handles, light switches, wall art, ceilings.
- **Bigger spaces:**
  - guest corridors **12 wide**, ceilings **14 high**;
  - service corridors **8 wide**;
  - guest rooms at least **20 x 24**;
  - the lobby stays double height.
- Doorways are clearly framed and lit, so you always know where you can go. Each room has a **sign or plaque** at the door.

## Construction rules (fix the gaps and clipping)
- **One snap grid**: 1 stud, with walls on a 4-stud grid. Wall pieces have **corner posts and trim strips that cover the joints**. Every wall run is built as one continuous piece per room side, not loose tiles.
- **Every room is designed as a fixed layout** (hand-made positions per room), never randomly scattered. Furniture sits in groups facing each other or the room's focus, with clear walking paths at least 4 studs wide.
- **The automated check runs after every change**: overlaps, gaps between walls (any light leak or gap over 0.05 studs), floating parts, blocked doors, unreachable task spots. Zero failures before showing anything.
- **Review gate**: build **one room fully** first, check it from first-person screenshots, then get the user's OK before cloning the approach to the next rooms.

## Room-by-room design (v2)
Each room lists its **theme**, its **signature piece**, its **light** and its **gameplay** (from the game ideas).

### Ground floor: public
| Room | Theme and look | Signature piece | Light | Gameplay |
|---|---|---|---|---|
| **Entrance and vestibule** | Brass revolving door, black-and-white marble floor, umbrella stand, a rain-wet doormat | The revolving door, with fog and pines behind the glass | Warm brass wall lanterns | Guests arrive (spawn), Inspector enters at dawn |
| **Grand lobby** (ref 01) | Double height, herringbone wood floor, zones: 3 round table groups with velvet tub chairs on patterned rugs, a **sunken lounge** with glowing step edges, a central stone **fireplace column**, ivy from the mezzanine, potted palms | Fireplace column with the founder's portrait above, and the grand piano | Sputnik chandeliers, lantern pendants, fireplace glow, moonlight through the tall windows and skylight | Guests wait here; piano note event; chandelier flicker |
| **Reception** (ref 02) | **Art deco**: black marble pillars, gold stepped arches, red carpet runner, a curved marble-and-brass desk, a neon "RECEPTION" sign | **The desk**, with built-in **CCTV monitor screens** behind it (a bank of 6 small CRTs showing live camera feeds), a key wall with brass keys (hook 113 empty), a desk bell, register, CRT computer, switchboard | Neon sign, brass desk lamps, warm downlights | **Check-in**, **room calls**, **quick CCTV check** from the desk (the full camera room is still the Security Room) |
| **Grand staircase** | Imperial stairs, red runner with brass rods, carved balusters, a stained-glass window at the landing | Stained-glass window with the Ashbourne crest | Wall sconces, glow through the stained glass | Path to the guest floor |
| **Restaurant "The Ashbourne Grill"** (ref 03) | **Retro 1990s diner-grill**: checkered floor, burgundy booths, counter with stools, bare-bulb pendants, glowing ceiling panels, framed photos | The counter with a pie display and coffee machine | Ceiling light panels and bulb pendants | **Room service pickups**, food orders for guests |
| **Lounge bar** | Dark green velvet, a back-lit bottle wall (no branding), leather armchairs, a jazz record player, a library corner with a rolling ladder | The glowing back bar | Back-lit shelves, table lamps | Drink deliveries, a hidden clue in the library |
| **The Night Counter (shop)** | A cosy old gift shop: wooden shelves, a glass display case lit from inside, a striped awning over the counter, a roller shutter, a chalkboard | A lit display case holding the boosts | Display lighting, a neon OPEN/CLOSED sign | **Hotel Shop**, Robux reroll bell |
| **Old Ballroom (closed)** | Dust sheets, a fallen chandelier, a stage with a red curtain, a "New Year 1998" banner, stacked chairs | The fallen chandelier in the middle of the floor | Moonlight through tall windows, one work lamp | Restricted area, story events |

### Ground floor: staff wing
| Room | Theme and look | Signature piece | Gameplay |
|---|---|---|---|
| **Security Room** | Dark room, a wall of 12 CRT monitors, a control desk, a cork board with a camera map and red string, VHS tapes | The monitor wall glowing in the dark | **Full CCTV system**, anomaly reports |
| **Staff Room** | Lived-in break room: 7 class lockers with names, a sofa, a kettle and mugs, a rota board, a 1998 staff photo, a time clock | The time clock and punch-card rack | **Clock in**, **heal** (first aid, cot, water cooler) |
| **Kitchen** | Steel and white tiles, steam, hanging pans, an order ticket rail, a pass window to the restaurant | The ticket rail with live orders | **Room service** |
| **Laundry** | Rows of washers with spinning drums, steam, folding tables, linen trolleys, the laundry chute | The laundry chute hatch | **Towel and linen pickup**, the knocking chute event |
| **Maintenance** | Workbench with a pegboard of tools, a fuse box wall, pipes, spare bulbs | The big breaker panel | **Fix tasks**, power cut repair, tool pickup |
| **Manager's office** | Wood panelling, a big desk, a filing cabinet, a safe, a 1998 calendar, memos | The locked safe | Story clues, management phone calls |

### Floor 1: guest floor (rooms 101 to 116)
- **The corridor** is 12 wide, with a patterned carpet runner, a ceiling with coves and glowing panels, wall sconces between doors, framed mountain paintings, a console table with flowers at every bend, an ice machine alcove and a linen cupboard. Each door has a brass plaque, a peephole and a "Do Not Disturb" hanger option.
- **Rooms are themed, not copies.** There are 4 layouts (single, double, suite, family) with **6 decor themes** used across the 16 rooms, plus story props per guest:
  1. **Alpine Lodge**: wood beams, plaid, antlers, a fireplace.
  2. **Art Deco**: black and gold, a geometric headboard.
  3. **Royal Burgundy**: velvet, a four-poster bed.
  4. **Teal Retro 90s**: a CRT TV, a patterned bedspread.
  5. **Garden Room**: plants and floral wallpaper.
  6. **Writer's Room**: a desk with a typewriter and books.
- **Each room** has a proper bathroom (tiles, bath or shower, sink with a mirror and lights, towels) and a window with a view of the fog and pines. Rooms change between **clean and messy** states for the cleaning tasks.
- **Room 113** doesn't exist, but its door sometimes appears. The east wing past 112 is **closed for renovation**: plastic sheets, scaffolding, exposed lath.
- **Room 214** (Floor 2, later) is Daniel Mercer's room, frozen in 1998.

## Gameplay stays as designed (user 2026-10-25: guests do NOT give quests)
- "Quest room" describes the **look and feel** of the rooms (hand-built, detailed, explorable in first person), **not** a quest-giver system. There are **no quest-giver NPCs and no quest markers over guests**.
- Gameplay is the existing design: [[Shift Tasks]] (check-in, deliveries, cleaning, maintenance, CCTV, room calls), guest needs as described in [[Guests]], the [[Hotel Shop]] window, [[Strange Events]] and [[Anomalies]], and the [[End of Shift Inspection]].
- Mysteries come from the hotel itself (events, CCTV, clue props in rooms), logged in the Journal.
- Guidance: gold interact spots, room signs, and floor maps at reception and in corridors.

## Build order (v2)
1. **Wall, floor and ceiling kit v2**: clean modules with joint-covering trims; check them with zero gaps.
2. **Vertical slice**: the **Grand lobby, reception (with CCTV monitors) and entrance**, built to final quality. Review it in first person with the user.
3. After approval: the restaurant, lounge bar and shop.
4. The guest corridor and the 6 room themes.
5. The staff wing.
6. The ballroom, the renovation zone, Floor 2 and Room 214.
