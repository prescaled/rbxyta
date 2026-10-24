---
tags: [room0, spawn, level-design]
status: proposal
---

# Spawn Island

The first place every player sees. It is the game's **menu you can walk around**: start a lobby, look at [[Classes]], and get a first look at the [[Ashbourne Hotel]] before the shift begins.

## Concept (redesigned 2026-10-24, stylised)
**Ashbourne Quay**: a small harbour street on an island at night, where the hotel's night staff wait for the shuttle. The **Ashbourne Hotel** stands across the black water, huge and lit, with a gold neon name sign. One pale green-white window sits on a floor the hotel should not have, which is a quiet hook for [[Room 0]].

Built in the stylised Roblox look from the [[Art Bible]] (style reference: *Animal Hospital*'s spawn, style only). Layout, buildings and props are our own.

## Mood
**Dark night with bright, friendly accents. Not Halloween.** The island is the safe place; the fear starts in the hotel.
- **Yes**: navy sky, light fog, wet cobbles and asphalt, amber lamps with glow, warm string lights across the street, cream windows, gold neon rings on everything you can use, burgundy Ashbourne awnings and banners.
- **No**: pumpkins, cobwebs, spiders, gravestones, cartoon ghosts, orange and purple Halloween colours.
- Details in [[Spawn Mood and Lighting]].

## Layout (top view)
```
~~~~~~~~~~~~~~~~~~ black water ~~~~~~~~~~~~~~~~~~~~   [ ASHBOURNE HOTEL ]  (across the water, lit)
   [Lookout + telescope]     [Arrival Pier + docked staff ferry]  <- spawn
==================== QUAY STREET (cobbles, string lights, lamps) ====================
 [Security Hut]  [Staff House]        [Key Plaza]          [Staff Supplies]   [SHUTTLE TERMINAL]
  tutorial        lockers + classes    brass key statue     kiosk (shop)        6 glowing bays
                                       leaderboards                             road into fog -> hotel
```

## Zones
| Zone | Purpose | Look and key features |
|---|---|---|
| **Arrival Pier** | Spawn point | Chunky wooden pier with thick posts and rope rails, a docked little staff ferry (burgundy hull, gold stripe), lamp posts, life rings. You see the hotel straight away. |
| **Quay Street** | The spine | Wide cobbled street along the water. Strings of warm bulbs zig-zag between buildings, fat iron lamp posts, benches, bins, crates, barrels, planters with dark pines, a teal phone box, notice posters. |
| **Staff House** | View and pick [[Classes]] | Two-storey brick building, burgundy awning, gold "STAFF LOCKERS" sign. Out front, 7 mannequins in class uniforms stand on round gold-neon pedestals, each with a floating class name. Step on one to open the class card. |
| **Key Plaza** | Central hub, social | Small round plaza with a giant brass **hotel room key statue** (tag reads "0"). Two big wall boards: "Employee of the Month" (best grades) and "Most Shifts". Clock on the Staff House shows shift time. |
| **Staff Supplies** | Spawn shop (cosmetics, coins) | Wooden kiosk with a burgundy and cream striped awning, crates of uniforms and keys, gold neon pad in front. |
| **Shuttle Terminal** | Lobbies ([[Lobbies]]) | Dark asphalt lot with bold white road lines and a canopy sign "SHUTTLES TO THE ASHBOURNE". 6 bays, each a **gold neon pad** with a staff van behind it and a big floating `0/4` and timer. Bay 1 is SOLO. A departures board on the canopy. The road leaves into fog towards the hotel. |
| **Security Hut** | Tutorial | Small teal hut with a barrier arm and a glowing pad labelled "Tutorial". |
| **Lookout** | Story | End of the pier, coin telescope pointed at the hotel, notice board with update notes and "missing" posters ([[The Missing Guests]]). |
| **Hidden spots** | Discovery | 3 to 5 small secrets linked to video clues ([[Player Experience#The video-to-game bridge]]). |

## UI (stylised, matches the world)
- Left side buttons in the same style: **Shifts**, **Classes**, **Shop**, **Invite**, **Journal** (big serif labels, navy fill, gold border).
- Bottom left: coins counter with an Ashbourne key icon.
- Overhead tag on each player: best shift grade and class (like "Top Shift: 14 / Porter" in the reference, but ours shows grade and class).

## Player flow
1. Spawn on the **Arrival Pier**. The camera pans across the water to the hotel once (first visit only).
2. Walk onto **Quay Street**. Floating labels and signposts point to Lockers, Shuttles and Tutorial.
3. First-timers are nudged to the **Tutorial Booth**.
4. Visit the **Staff House** pedestals to view and pick a class ([[Classes]]).
5. Step on a bay pad in the **Shuttle Terminal** ([[Lobbies]]). When it fills or the timer runs out, the group teleports to the hotel.
6. After a shift ends, players come back here with their coins and progress.

## Size and performance
- Keep it **small and dense** (changed 2026-10-24: the first build was far too wide): about 260 x 150 studs, a 20 to 30 second walk from end to end. Every corner should have something to look at.
- Fog hides the island's edges and keeps the part count low.
- Use **StreamingEnabled**, and reuse modular pieces (lamps, fences, cobble tiles). Detailed textured meshes are reused as modular kit pieces to keep memory low.

## Models
See [[Blender Model List#Spawn island]].
