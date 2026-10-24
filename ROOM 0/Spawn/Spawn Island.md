---
tags: [room0, spawn, level-design]
status: proposal
---

# Spawn Island

The first place every player sees. It is the game's **menu you can walk around**: start a lobby, look at [[Classes]], and get a first look at the [[Ashbourne Hotel]] before the shift begins.

## Concept (proposal)
**Ashbourne Staff Quay**: a small, foggy island where night-shift staff wait for the shuttle to the hotel. The hotel stands across the dark water, with its windows lit. One lit window is on a floor the hotel should not have, which is a quiet hook for [[Room 0]].

Players arrive at the pier, walk through the staff plaza, choose a class in the Staff Locker Hall, and board a **staff shuttle** (the lobby) that drives them to the hotel.

## Mood (decided 2026-10-24)
**Darker and spookier, but not Halloween.** It should feel like a real place at 2 a.m., not a theme park.
- **Yes**: night sky, moonlight through low fog, wet cobblestones, old sodium street lamps (warm orange pools of light), wind, waves against the pier, a distant fog horn, a flickering sign.
- **No**: pumpkins, skeletons, cobwebs, cartoon ghosts, green slime, purple "spooky" lighting.
- Details in [[Spawn Mood and Lighting]].

## Layout (top view)
```
                 N
        [Lookout + Notice Board]
                 |
[Staff Locker Hall]--[Staff Plaza]--[Shuttle Bay: lobbies]  ~~ water ~~  [Ashbourne Hotel]
     (classes)     |   clock tower   |
        [Tutorial Booth]   [Leaderboards]
                 |
            [Arrival Pier]  <- players spawn here
                 S
```

## Zones
| Zone | Purpose | Key features |
|---|---|---|
| **Arrival Pier** | Spawn point | Wooden pier, mooring posts, lamp posts, fog horn sound, short walk to the plaza so new players see the hotel straight away |
| **Staff Plaza** | Central hub | Cobbled square, clock tower (shows real shift time), benches, café front with lights off, public phone box (rings sometimes) |
| **Shuttle Bay** | Lobbies | A row of staff shuttle vans, each with a 0/4 board. See [[Lobbies]] |
| **Staff Locker Hall** | View and pick [[Classes]] | Uniform mannequins on pedestals, lockers, class info cards, mirror to preview |
| **Tutorial Booth** | Teach new players | Old security booth; a short guided task (check in one guest, fix one light) |
| **Lookout + Notice Board** | Story and updates | Telescope pointing at the hotel; notice board with update notes, "missing" posters that match the videos ([[The Missing Guests]]) |
| **Leaderboards** | Social | Brass "Employee of the Month" boards: most shifts, best grades, most coins |
| **Hidden spots** | Discovery | 3 to 5 small secrets linked to video clues ([[Player Experience#The video-to-game bridge]]) |

## Player flow
1. Spawn on the **Arrival Pier**. The camera pans across the water to the hotel once (first visit only).
2. Walk up to the **Staff Plaza**. Signposts point to Lockers, Shuttles and Tutorial.
3. First-timers are nudged to the **Tutorial Booth**.
4. Visit the **Staff Locker Hall** to view and pick a class ([[Classes]]).
5. Board a shuttle in the **Shuttle Bay** ([[Lobbies]]). When it fills or the timer runs out, the group teleports to the hotel.
6. After a shift ends, players come back here with their coins and progress.

## Size and performance
- Keep it **small and dense**: a 60 to 90 second walk from end to end. Every corner should have something to look at.
- Fog hides the island's edges and keeps the part count low.
- Use **StreamingEnabled**, and reuse modular pieces (lamps, fences, cobble tiles).

## Models
See [[Blender Model List#Spawn island]].
