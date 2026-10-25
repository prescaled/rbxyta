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
| Shift loop v1 (game code) | R+X | claimed (2026-10-25: scripts only in R0_Game folders; sources rbxyta-assets/game; no HotelV2, lighting or Hotel_* build changes) |
| Spawn place: pier, plaza, shuttle bay, locker hall, lighting | P+C | claimed |
| Hotel floor 1: reception, lobby, corridor, guest rooms, staff room | P+C | review (2026-10-25: ground floor + F1 built in the Hotel place from Codex's layout; 30 rooms furnished, 71 task spots, 12 CCTV, doors, plaques, lighting zones; handed over from R+X at sxdf's request) |
| Modular corridor kit: straight wall, corner, door-frame wall, floor, ceiling, skirting, carpet runner, room door and swappable number plaque (digits 0-9) | R+X | building |
| Hotel interior kit | P+C | review (2026-10-25: R0_Hotel_F1_Import.fbx, 143 models + Codex's library; build script tools/studio_hotel/src/HotelBuild.lua) |
| Grand Lobby + Vestibule + Grand Staircase | P+C | building (handed over from R+X at sxdf's request 2026-10-25; reuses Codex's library models) |
| Asset repo setup (rbxyta-assets: folders, LFS, rules) | P+C | done |
| Hotel place (second place in the experience; move hotel out of the Spawn place) | P+C | review (2026-10-25: place 133290122655457 built; Spawn place cleared of the hotel draft; HotelPlaceId set in the spawn Config) |

## Spawn kit (P+C, claimed 2026-10-24)
| Item | Owner | Status |
|---|---|---|
| R0_Spawn_Cobble_Tile (wet cobblestone, 8x8 studs) + kerb + drain | P+C | review (Blender done, spawn/R0_Spawn_Kit.blend) |
| R0_Spawn_Pier_Plank / Post / Railing (modular pier) | P+C | review (Blender done, spawn/R0_Spawn_Kit.blend) |
| R0_Spawn_StoneWall + R0_Spawn_IronFence (modular) | P+C | review (Blender done, spawn/R0_Spawn_Kit.blend) |
| R0_Spawn_Bench, R0_Spawn_Bin, R0_Spawn_Signpost | P+C | review (Blender done, spawn/R0_Spawn_Kit.blend) |
| Spawn place blockout + lighting (Roblox, Spawn place only) | P+C | replaced by the stylised rebuild below |
| Spawn island stylised rebuild (Ashbourne Quay, detailed textured meshes, Spawn place only) | P+C | review (redesigned as Ashbourne Hollow 2026-10-24: enclosed round hollow, 34 new models imported and placed, tunnel lobbies, graveyard; scripts in rbxyta-assets/tools/studio) |
| Detailed stylised remake of StreetLamp, ShuttleVan, spawn kit + new Quay models | P+C | review (83 textured models incl. the Hollow set; combined imports R0_Spawn_ALL_Import.fbx + R0_Spawn_Hollow_Import.fbx; renders in reference/renders) |

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
| R0_Prop_LuggageTrolley | R+X | building | Classes, deliveries |
| R0_Prop_HousekeepingCart | R+X | todo | Classes, cleaning |

Add rows as you claim things. One owner per row.
