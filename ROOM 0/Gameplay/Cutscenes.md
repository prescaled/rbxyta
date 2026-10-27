---
tags: [room0, gameplay, cinematics]
status: decided-core
---

# Cutscenes

**Decided 2026-10-24:** cinematic **POV cutscenes**, like arriving at the hotel.

## Style
- **First-person POV** wherever possible, so the player feels like they are *there*.
- Letterbox bars, no UI, slow camera moves, real sound (engine, rain, footsteps).
- Same dark, realistic mood as the [[Spawn Mood and Lighting|spawn island]]. Never cartoony.
- **Skippable** after the first time, and short (10 to 40 seconds).
- Every cutscene doubles as **footage for TikTok/Shorts** ([[Content Strategy]]).

## Cutscene list (proposal)
| # | Cutscene | When | What you see | Priority |
|---|---|---|---|---|
| 1 | **Arrival** | First shift of a run | POV in the staff shuttle: wipers, fog, the hotel appears out of the dark, gates open, the van stops, walk through the doors into the lobby | P1 |
| 2 | **Clock-in** | Every shift (short) | Punch card into the time clock, the clock reads 11:58 p.m., lights hum | P1 |
| 3 | **Midnight** | Clock hits 12:00 | Quick shots of empty corridors from the CCTV cameras, one feed glitches | P2 |
| 4 | **First anomaly** | First time a type appears | Short reveal of a predator or anomaly ([[Anomalies]]) | P1 |
| 5 | **3 a.m.** | Night 3+ | Lights dim floor by floor, the lift dings with nobody inside | P2 |
| 6 | **Knocked out** | 0 HP ([[Health]]) | Blurred POV, fall to the floor, black, wake on the staff-room cot | P1 |
| 7 | **Dawn and inspection** | End of shift | Sunrise through the lobby windows, [[The Inspector]] walks in with the clipboard | P1 |
| 8 | **Departure** | Back to spawn | POV from the shuttle's back window: the hotel shrinks into the fog, and one window stays lit | P2 |
| 9 | **Room 0 reveal** | Endgame | Depends on [[Room 0#The secret]] | P3 |

## How to build (Roblox)
- Camera paths with **CFrame tweens** or Moon Animator; character and prop animation in Moon Animator or Blender.
- One **CutsceneService** module: plays a cutscene by name, hides UI, handles skip, and syncs all players in the server.
- Record the same paths in high quality for the videos.

## Models
Shuttle interior, gate, time clock and others: see [[Blender Model List#Cutscenes]].

## Detailed expansion (27 October 2026)

See [[Cinematics and CCTV - Index]], [[Cinematics - Direction and Pacing]] and [[Cinematics - Scene Catalogue]] for the requested range of sightings and cinematic scenes. The 12 concepts are proposals, not implemented content or settled missing-case explanations.

The newer design distinguishes short world sightings (normal control/HUD), interactive discoveries (voluntary entry/exit), and longer chapter cinematics. Letterboxing, hidden ordinary HUD and 10-40 second lengths apply to chapter presentation, not every apparition. Accessibility captions and essential exit controls remain available. Per-player scenes do not cut every teammate away from their work. The current Art Bible is detailed stylised Roblox; the older realistic-mood wording describes tone, not photorealistic art.
