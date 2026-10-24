---
tags: [room0, spawn, multiplayer]
status: decided-core
---

# Lobbies

**Decided 2026-10-24:** spawn has places for players to start lobbies that show **0/4 players**.

## The shuttle lobby (proposal)
Each lobby is a **staff shuttle van** parked on the [[Spawn Island#Zones|Shuttle Road]]. Next to its sliding door is a **glowing yellow pad** on the pavement; standing on the pad joins the lobby. A **floating counter** above the pad (BillboardGui, Roblox style) shows the count and timer. (Changed 2026-10-24: pads instead of climbing inside the van, because they read better.)

| State | Board shows | What happens |
|---|---|---|
| Empty | `0/4  WAITING` | Doors open, headlights off |
| Filling | `2/4  LEAVING IN 0:20` | The countdown starts when the first player boards |
| Full | `4/4  DEPARTING` | Doors close, engine starts, everyone teleports |
| Leaving | `DEPARTED` | The van drives into the fog, and a new empty van rolls in |

## Rules
- **Max 4 players** per shift.
- **Countdown**: 20 seconds after the first player boards, reset to 10 seconds when someone new joins. It leaves when full or when the timer ends.
- **Leave**: step off the pad to leave the lobby.
- **Party host**: the first player in can set the van to **Friends only** or **Open**.
- **Solo shift**: one van marked `SOLO` leaves straight away with one player.
- **Class check**: you need a class picked before you can board. It defaults to Trainee ([[Classes]]).
- About 6 to 8 vans, so the bay never looks empty.

## Technical notes
- Each van teleports its group to a **reserved server** for the hotel place (TeleportService).
- Pass the party list and each player's class in the teleport data.
- When the shift ends, teleport players back to the spawn island.

## Models
Shuttle van, lobby board, bay shelter, road markings and so on: see [[Blender Model List#Spawn island]].
