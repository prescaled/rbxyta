---
tags: [room0, spawn, level-design]
status: proposal
---

# Spawn Island

The first place every player sees. It is the game's **menu you can walk around**: start a lobby, look at [[Classes]], and get a first look at the [[Ashbourne Hotel]] before the shift begins.

## Concept
**Ashbourne Staff Quay**: one busy little street on the waterfront where the hotel's night-shift staff wait for the shuttle. Across the water, close and huge, stands the [[Ashbourne Hotel]] with its lit sign. One lit window is on a floor the hotel should not have, which is a quiet hook for [[Room 0]].

Players arrive on the dock, walk down the quay street, pick a class in the Staff Quarters, and step onto a glowing pad next to a **staff shuttle** (the lobby). When it leaves, the screen fades and they travel to the hotel.

## Style (decided 2026-10-24)
**Roblox style**, using the *Animal Hospital* spawn as a style reference only (see [[Art Bible#Look (updated 2026-10-24: Roblox style)]]): chunky, warm, saturated, dense, readable. Our own street, buildings and hotel; never their layout.
- **Yes**: warm street lamps, lit windows, brick pavements, a real road with white lines, ornate iron railings, benches, bins, trees, planters, signs, glowing lobby pads with floating counters, the hotel's lit sign across the water.
- **No (except as timed events)**: pumpkins, skeletons, cobwebs, cartoon ghosts, slime.
- Lighting values: [[Spawn Mood and Lighting]].

## Layout (top view, about 280 x 160 studs)
```
                         N    ~~~ dark water ~~~     [THE ASHBOURNE HOTEL]  (its own island)
                                                            ^
[Arrival dock  ]  ==== Quay promenade: railing, telescope, benches, notice board ==== [Bridge]
[ + staff ferry] [pad][van] [pad][van] [pad][van] [pad][van] [pad][van] [pad][SOLO]    |
 players spawn   -------------------------- Shuttle Road ------------------------  [Gatehouse:
 here            ======================== south pavement =========================  Tutorial]
                 [Staff Quarters: CLASSES] [Clock square] [Night Owl Cafe] [Leaderboard wall]
                         S
```

## Zones
| Zone | Purpose | Key features |
|---|---|---|
| **Arrival Dock** | Spawn point | Short wooden dock, moored staff ferry, lamps, fog horn; you see the hotel straight away |
| **Quay Promenade** | View + story | Ornate railing along the water, coin telescope aimed at the hotel, benches, notice board with update notes and "missing" posters ([[The Missing Guests]]) |
| **Shuttle Road** | Lobbies | 6 staff shuttle vans parked at the kerb, each with a glowing yellow pad by its sliding door and a floating `0/4` counter. See [[Lobbies]] |
| **Staff Quarters** | View and pick [[Classes]] | Brick building with big lit windows, `CLASSES` sign, uniform mannequins on pedestals inside, lockers, mirror |
| **Clock Square** | Central hub | Clock tower (real shift time), benches, trees, planters, phone box (rings sometimes) |
| **Night Owl Café** | Life + future shop | Open, warm café front with an awning and outdoor tables; later a cosmetics or snack shop |
| **Leaderboard wall** | Social | Brass "Employee of the Month" boards: most shifts, best grades, most coins |
| **Gatehouse** | Tutorial | Security booth with a barrier at the start of the hotel bridge; short guided task |
| **Hidden spots** | Discovery | 3 to 5 small secrets linked to video clues ([[Player Experience#The video-to-game bridge]]) |

## Player flow
1. Spawn on the **Arrival Dock**. The camera pans across the water to the hotel once (first visit only).
2. Walk onto the quay. Signs point to Classes, Shuttles and Training.
3. First-timers are nudged to the **Gatehouse** tutorial.
4. Visit the **Staff Quarters** to view and pick a class.
5. Stand on a van's glowing pad ([[Lobbies]]). When it fills or the timer runs out: fade to black, engine sound, "Travelling to the Ashbourne Hotel..." card, then the hotel ([[Cutscenes]]).
6. After a shift, players come back here with their coins and progress.

## Size and performance
- **Small and dense** (changed 2026-10-24, the first version was far too wide): about 280 x 160 studs, a 20 to 30 second walk end to end.
- Use **StreamingEnabled** and reuse modular pieces (lamps, fences, benches).

## Models
See [[Blender Model List#Spawn island]].
