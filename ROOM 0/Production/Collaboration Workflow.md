---
tags: [room0, production, workflow]
status: proposal
---

# Collaboration Workflow (two people, two AIs)

How **Prescaled + Claude** and **Rivin + Codex** build ROOM 0 at the same time without clashing, while sharing one set of models so everything looks like one game. Both AIs use **Blender MCP** and **Roblox Studio MCP**.

## The 5 rules
1. **Split by place and area, not by task.** Each AI owns whole areas. Nobody edits an area they do not own.
2. **One shared model library.** Every model is built once, by one owner, and then reused by both sides. No duplicates.
3. **One art standard.** Both AIs follow the [[Art Bible]], so models from either side match.
4. **Claim before you build.** Put your name on an item in the [[Work Board]] and push it *before* starting.
5. **Pull, work, push, often.** Pull before every session, push small changes when done.

## 1. Who owns what (starting split, change any time)
| Owner | Owns | Why it is safe |
|---|---|---|
| **Prescaled + Claude** | **Spawn place**: [[Spawn Island]], [[Lobbies]], class hall ([[Classes]]), spawn lighting, arrival/departure [[Cutscenes]] | The spawn island is its own Roblox **place**, so nothing overlaps |
| **Rivin + Codex** | **Hotel place, floor 1**: reception, lobby, guest corridor, guest rooms, staff room, [[Shift Tasks]] | Separate place in the same experience |
| **Shared, one owner per item** | Shared library: shuttle van, uniforms, guest NPCs, [[The Inspector]], props used in both places | Built once, then reused as Packages |

Next split, once the first areas are done: Claude takes [[Anomalies]] (predators) and the in-hotel cutscenes, Codex takes the [[CCTV System]], [[Hotel Shop]] and [[Guests]] logic.

## 2. Roblox: Team Create + Packages
- Create a **Roblox group** that owns the experience (both of you as admins). Turn on **Team Create** for every place.
- The experience has **separate places**: `Spawn` (start place) and `Hotel`. Lobbies teleport between them. Each AI only opens its own place.
- **Shared models = Roblox Packages.** When a shared model is ready, convert it to a Package owned by the **group**, with **AutoUpdate on**. Both places insert the same Package, so an update shows up everywhere.
- Inside a place, keep each owner's work in its own folder:
  - `Workspace/Spawn_<Zone>`, `Workspace/Hotel_F1_<Room>`
  - `ServerScriptService/<System>`, `ReplicatedStorage/Shared/<System>`
- **Scripts**: keep them in Git with **Rojo** if you can, so code merges like the notes do. If not, give each system one owner, just like areas.
- Tell the Roblox MCP session which folder it owns at the start of every session ("You own Workspace/Spawn_*. Do not touch anything else.").

## 3. Blender: one file per area, one shared library
- Keep Blender sources in a **separate private asset repo** (with **Git LFS** for `.blend` and textures), or a shared cloud folder. Do not put them in this public vault.
- Folder layout:
  ```
  rbxyta-assets/
    library/      R0_Library.blend (shared props, one owner per object)
    spawn/        R0_Spawn_*.blend      (Prescaled + Claude)
    hotel_f1/     R0_Hotel_F1_*.blend   (Rivin + Codex)
    characters/   R0_Char_*.blend
    textures/     shared materials and trim sheets
    export/       .fbx files ready for Roblox
  ```
- Area files **link** shared assets from `R0_Library.blend` (File > Link), never copy them. Change the library object once and every file updates.
- `.blend` files cannot be merged. Only the claimed owner edits a file. If two people need the same file, take turns.

## 4. Session checklist (for both AIs)
Give this to Claude or Codex at the start of every build session:
1. Pull the vault and the asset repo.
2. Read [[Art Bible]] and [[Work Board]].
3. Only work on items claimed by your side. Claim new ones first and push the claim.
4. Name everything with the [[Art Bible#Naming]] rules.
5. Export to `export/`, import into Roblox, and make shared items Packages.
6. Mark the item done on the [[Work Board]], then commit and push.

## 5. Avoiding clashes
- If the board shows someone else claimed it, **do not touch it**. Ask instead.
- Shared items get a **review**: the other side checks it fits their area before it is marked done.
- A short daily check-in: what you finished, what you claim next.
