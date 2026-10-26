---
tags: [room0, gameplay, anomalies, enemies]
status: decided-core
---

# Anomalies and Predators

**Decided 2026-10-24:** there are **predators and anomalies**, and players can **kill** them. Each needs its own model.

Two kinds of threats:
- **Anomalies**: things that are *wrong* in the hotel. They do not attack, but they grow worse if nobody reports or fixes them.
- **Predators**: entities that *hunt* players. They deal damage ([[Health]]) and can be killed or driven off.

Rule from [[Player Experience#Uncertainty]] still holds: not everything strange is dangerous. Early nights are mostly anomalies; predators show up later in a run ([[Strange Events#Escalation across a run]]).

## Anomalies (non-hostile)
| Anomaly | What it looks like | How to clear it |
|---|---|---|
| Wrong room number | A door shows a number that does not exist | Report on CCTV |
| Duplicate | Two of the same painting, chair or guest | Report on CCTV |
| Moved furniture | A room is rearranged between camera checks | Report, or put it back |
| Camera-only figure | Someone standing still, only on CCTV | Report on CCTV |
| Voice on the radio | A teammate's voice says something they never said | Ignore it, or report |
| Extra corridor | A corridor that was not there last night | Report and avoid |
| Wrong guest | A guest whose face, ID or booking doesn't match their file (for example, the ID says 1998) | Refuse at the check-in terminal ([[Task Interfaces#1. Check-in terminal (build first)]]); report |

Unreported anomalies **escalate**: after a few minutes, some turn into a predator.

## Predators (hostile, can be killed)
| Predator | Behaviour | Weakness / how to kill | Night |
|---|---|---|---|
| **The Bellhop** | Tall, wrong proportions, old 1998 uniform. Only moves when nobody looks at it | Keep it in a flashlight beam, then hit it 3 times with a heavy tool | 2+ |
| **The Housekeeper** | Drags a cart; hunts by sound. Gets faster if you run | Stay quiet; lure it with a dropped item, then trap and kill it in the laundry room | 3+ |
| **The Vent Crawler** | Lives in vents in maintenance areas; grabs players near open vents | Close vents with the toolbox; stun it with the fire extinguisher, then finish it | 3+ |
| **The Faceless Guest** | Looks like a normal guest until you check them in; then it follows you | Spot it on CCTV first; kill it before it reaches the front desk | 4+ |
| **The Occupant** | Never seen. Knocks, footsteps, and doors opening near where [[Room 0]] might be | Cannot be killed, only escaped. Story boss | 5+ / story |

## Killing (proposal)
- Players use **hotel items as weapons**: a heavy flashlight, a mop handle, a wrench, the fire extinguisher (stun). No guns, to keep the tone.
- Typical fight: **stun** (light or extinguisher), then **hit** 2 to 4 times. Teamwork makes it much easier.
- Killed predators **fade into static** or **dissolve like old film**. No blood or gore, which keeps the dark-but-not-gory tone and fits Roblox rules.
- Killing a predator pays bonus coins and counts towards the [[End of Shift Inspection]].
- Classes help: Maintenance Tech kills Vent Crawlers faster, Night Security has the strong flashlight ([[Classes]]).

## Story link
Each predator should be a **clue** to [[Room 0#The secret]]. For example, the Bellhop could be a hotel worker from 1998, the year [[Daniel Mercer]] vanished.

## Open
- Can predators be killed for good, or do they return the next night? ([[Open Questions]])
- Weapon slot: does everyone carry one, or do they pick tools up in the hotel?

## Models
See [[Blender Model List#Anomalies and predators]].
