---
tags: [room0, production, guests]
status: building
---

# Guest model import — 2026-10-27

R+X imported all 13 starting guests into Hotel 133290122655457 using the approved Studio importer UI. HotelV2 and the other team's scripts were untouched.

Installed at `ServerStorage/R0_Guests/<BookingID>/<Name>`:

- S01: MartinPike
- S02: LeenaShah
- P01: GwenEllis, ArthurEllis
- P02: AishaReed, TomReed
- T01: NiaBrooks, BethLane, CallumRoss
- Q01: DawnKeating, PeteNolan, IvoNovak, KellyWatts

All passed structural checks: 15 MeshParts with permanent mesh and texture IDs and 16 bones each. Colours survive import through embedded 512px atlases. Importer's 100x unit conversion was corrected; heights are approximately 4.95–5.80 studs.

Sources, FBXs, portraits, lineup, import scripts and `roblox_assets.json` live in the private asset repository under `characters/guests/`. Textured master: `R0_Guests_Textured.blend`. Use 3D Importer; the older CreateAssetAsync route is unavailable.

These are visual skeleton templates with AnimationController/Bones, not yet validated R15 Humanoid NPCs. Gameplay spawner and animation integration, portrait upload and shared Packages remain pending. Families and anomaly variants were not added. Full first-shift two-night acceptance remains pending.

User should save Hotel using **File > Save to Roblox**.

Related: [[Work Board]], [[Ordinary Guests - Character Sheets]], [[First Shift Implementation]].
