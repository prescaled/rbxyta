---
tags: [room0, spawn, level-design]
status: proposal
---

# Spawn Island

The first place every player sees. It is the game's **menu you can walk around**: start a lobby, look at [[Classes]], and get a first look at the [[Ashbourne Hotel]] before the shift begins.

## Concept (redesigned again 2026-10-24: enclosed, no water)
**Ashbourne Hollow**: the hotel's staff village, tucked in a round hollow between mountains. Steep rocky slopes and dense pine forest close it in on every side, so the spawn feels like one **enclosed, roughly circular space**, not a street or a coast. There is **no sea, pier or ferry**.

The **Ashbourne Hotel** stands on a rocky rise at the north edge of the hollow, above the rooftops, behind tall iron gates. You can always see it, lit, with one pale green-white window on a floor it should not have (hook for [[Room 0]]). You can't walk to it: the staff shuttles drive there through a tunnel in the mountain.

Style: detailed stylised Roblox look ([[Art Bible]]), like the user's reference *Animal Hospital* (an enclosed square ringed by buildings, with glowing pads in the middle). Style only: our layout, our buildings, no Halloween.

## Mood
**Dark night with bright, friendly accents. Not Halloween.** The hollow is the safe place; the fear starts in the hotel.
- **Yes**: navy sky, light fog in the pines, mountains as dark silhouettes, wet cobbles and asphalt, amber lamps with glow, warm string lights between the buildings, cream windows, gold neon rings on everything you can use, burgundy Ashbourne awnings and banners.
- **No**: pumpkins, cobwebs, spiders, gravestones, cartoon ghosts, orange and purple Halloween colours. No water.
- Details in [[Spawn Mood and Lighting]].

## Layout (top view, about 200 studs across)
```
                  mountains + pines
          _______________________________
         /   [ASHBOURNE HOTEL on its rise] \
        /  iron gates      [Overlook terrace]\
       | [Staff House]            [Shuttle    |
 pines |  classes   ( ring road )  Terminal]  |== tunnel -> hotel
       |        [ Key Plaza: statue,  6 bays] |
       | [Supplies]   spawn, boards           |
        \ [Security Hut]   [Staff Canteen]   /
         \_________________________________/
                  mountains + pines
```
- **Centre**: round **Key Plaza** (spawn), cobbles, the giant brass key statue, benches, leaderboards.
- **Ring road**: an asphalt loop with bold white lines around the plaza, like the reference, with lamps on both kerbs.
- **Outer ring**: buildings and features all **face inward** to the plaza, with no gaps. Between buildings: fences, hedges, lamp posts and pine clusters, so the ring stays closed.
- **Behind the buildings**: rising rock and stylised mountains with dense pines and fog. No visible edge of the map.

## Zones
| Zone | Purpose | Look and key features |
|---|---|---|
| **Key Plaza** (centre) | Spawn, hub, social | Round cobbled plaza, giant brass room-key statue with a "0" tag, benches, planters, "Employee of the Month" and "Most Shifts" boards facing the centre. Spawn points around the statue. |
| **Staff House** (west) | View and pick [[Classes]] | Brick building, burgundy awning, gold STAFF LOCKERS sign. 7 class mannequins on gold neon pedestals in front, with floating names. |
| **Shuttle Terminal** (east) | Lobbies ([[Lobbies]]) | Canopy sign "SHUTTLES TO THE ASHBOURNE", 6 gold neon bay pads in a curve with a van behind each, big floating 0/4 and timer. Bay 1 is SOLO. The vans leave through a lit **stone tunnel** into the mountain. |
| **Hotel rise** (north) | Landmark, story | The hotel on rocks above the hollow, behind tall iron gates and a hedge, with a winding road up. More detailed than the first version (see below). |
| **Overlook terrace** (north-east) | Story | Raised terrace with a coin telescope aimed at the hotel and a notice board with update notes and "missing" posters ([[The Missing Guests]]). |
| **Staff Supplies** (south-west) | Spawn shop | Kiosk with a striped burgundy and cream awning, gold neon pad. |
| **Staff Canteen** (south-east) | Social, decoration | Small diner front with lit windows and outdoor tables (closed at night, warm lights inside). |
| **Security Hut** (south) | Tutorial | Small teal hut with a barrier arm and a glowing "Tutorial" pad. |
| **Fill buildings** (user 2026-10-24: "add more buildings to fill up the area") | Make the ring feel full and lived-in | All facing inward, detailed and from the building kit with their own signs: **Staff Dormitory** (two 3-storey blocks, lit windows, laundry lines between them), **Hotel Laundry** (steam vents, carts of linen outside), **Maintenance Garage** (roller door half open, tools, a parked utility cart), **Post and Parcels** room (mail sacks, pigeonholes in the window), **Uniform Tailor** (mannequins in the window), **Shuttle Depot Office** next to the terminal. |
| **Background depth** | Fill the view beyond the ring | Rooftops and chimneys of more cottages on the lower slopes behind the ring, with lit windows, a small chapel-less bell tower, a water tower, and a few lit cabins among the pines on the mountainsides. Cheap low-detail meshes; you see them, but can't reach them. |
| **Hidden spots** | Discovery | 3 to 5 secrets in the pines and behind buildings, linked to video clues ([[Player Experience#The video-to-game bridge]]). |

## The hotel (needs more detail)
Not too complicated, but more than a box with windows: a central entrance block with a porch, columns and a gold ASHBOURNE HOTEL sign; two wings; 4 to 5 floors with framed windows (lit and dark, some with curtains), balconies, cornices between floors, a mansard roof with dormers, chimneys, a rooftop sign; warm uplights on the facade; and the one wrong pale window on an extra floor.

## UI (stylised, matches the world)
- Left side buttons in the same style: **Shifts**, **Classes**, **Shop**, **Invite**, **Journal** (big serif labels, navy fill, gold border).
- Bottom left: coins counter with an Ashbourne key icon.
- Overhead tag on each player: best shift grade and class (like "Top Shift: 14 / Porter" in the reference, but ours shows grade and class).

## Player flow
1. Spawn in the **Key Plaza**, facing north towards the hotel on its rise (first visit: a slow camera pan over the hollow to the hotel).
2. Floating labels point to Classes, Shuttles, Shop and Tutorial around the ring.
3. First-timers are nudged to the **Security Hut** tutorial.
4. Pick a class at the **Staff House** pedestals ([[Classes]]).
5. Step on a bay pad at the **Shuttle Terminal** ([[Lobbies]]). The van drives into the tunnel, then the travel cutscene plays.
6. After a shift, players come back to the plaza with their coins and progress.

## Size and performance
- Keep it **small and dense** (changed 2026-10-24: the first build was far too wide): about 260 x 150 studs, a 20 to 30 second walk from end to end. Every corner should have something to look at.
- Mountains, pines and fog hide the map edge; the slopes are terrain plus low-poly rock and pine meshes.
- Use **StreamingEnabled**, and reuse modular pieces (lamps, fences, cobble tiles). Detailed textured meshes are reused as modular kit pieces to keep memory low.

## Models
See [[Blender Model List#Spawn island]].
