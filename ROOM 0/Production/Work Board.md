---
tags: [room0, production, workflow]
---

# Work Board

Claim an item **before** you build it, and push the claim. Rules: [[Collaboration Workflow]]. Models list: [[Blender Model List]].

Owners: **P+C** = Prescaled + Claude, **R+X** = Rivin + Codex.
Status: `todo` · `claimed` · `building` · `review` · `done`

## Areas
| Area | Owner | Status |
|---|---|---|
| Spawn place: pier, plaza, shuttle bay, locker hall, lighting | P+C | claimed |
| Hotel floor 1: reception, lobby, corridor, guest rooms, staff room | R+X | claimed |
| Modular corridor kit: straight wall, corner, door-frame wall, floor, ceiling, skirting, carpet runner, room door and swappable number plaque (digits 0-9) | R+X | building |
| Asset repo setup (rbxyta-assets: folders, LFS, rules) | P+C | done |

## Spawn kit (P+C, claimed 2026-10-24)
| Item | Owner | Status |
|---|---|---|
| R0_Spawn_Cobble_Tile (wet cobblestone, 8x8 studs) + kerb + drain | P+C | review (Blender done, spawn/R0_Spawn_Kit.blend) |
| R0_Spawn_Pier_Plank / Post / Railing (modular pier) | P+C | review (Blender done, spawn/R0_Spawn_Kit.blend) |
| R0_Spawn_StoneWall + R0_Spawn_IronFence (modular) | P+C | review (Blender done, spawn/R0_Spawn_Kit.blend) |
| R0_Spawn_Bench, R0_Spawn_Bin, R0_Spawn_Signpost | P+C | review (Blender done, spawn/R0_Spawn_Kit.blend) |
| Spawn place blockout + lighting (Roblox, Spawn place only) | P+C | replaced by the stylised rebuild below |
| Spawn island stylised rebuild (Ashbourne Quay, parts-built, Spawn place only) | P+C | in progress (2026-10-24) |
| Stylised remake of StreetLamp, ShuttleVan, spawn kit (flat colours, chunky) | P+C | in progress (2026-10-24) |

## Shared library items
| Item | Owner | Status | Used in |
|---|---|---|---|
| R0_Prop_StreetLamp | P+C | review (Blender done, 824 tris; Roblox import + Package pending) | Spawn, hotel exterior |
| R0_Spawn_ShuttleVan | P+C | review (Blender done, 1,688 tris; Roblox import + Package pending) | Spawn, arrival cutscene |
| R0_Char_Uniforms (7 classes) | P+C | todo | Spawn locker hall, hotel |
| R0_Char_Inspector | R+X | todo | Hotel, dawn cutscene |
| R0_Char_Guests (6 looks) | R+X | todo | Hotel, spawn background |
| R0_Prop_Flashlight | R+X | todo | Classes, hotel |
| R0_Prop_Toolbox | R+X | todo | Classes, maintenance |
| R0_Prop_LuggageTrolley | R+X | todo | Classes, deliveries |
| R0_Prop_HousekeepingCart | R+X | todo | Classes, cleaning |

Add rows as you claim things. One owner per row.
