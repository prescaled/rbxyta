---
tags: [room0, production, guests, art]
status: review
updated: 2026-10-29
---

# Guest concepts: the target look for the guest rebuild

**Asked for by the user on 2026-10-29:** the guest models built earlier weren't the look they want. The user wanted concept images of each guest, tailored to their [[Ordinary Guests - Character Sheets|character sheet]]. Once they approve them, they want asset render sheets so Codex can rebuild the guests in Blender.

## The look (the user's decisions, 2026-10-29)
- **Roblox figure proportions:**
  - the **default Roblox head**: a rounded cylinder, not a box;
  - a blocky body;
  - curled C-shaped hands that hold things;
  - a flat drawn face decal (dot eyes, simple brows, a smile line).
- **Clothes that look like real fabric, not matte plastic:** denim twill, knit with fuzz, nylon with soft creases and sheen, leather grain, cotton weave, tweed, cord, fleece and woven plaid. Buckles, pins and frames are real metal. Skin stays a soft, non-glossy toy finish.
- **Not the shiny "AI" look:** no bloom, glow or blur. A plain pale backdrop and soft three-point light.
- **Every guest is unique**, the way the user liked Martin Pike (suit, tie, suitcase): layered outfits and story accessories, never a plain T-shirt and trousers.
- **Hair is sculpted and chunky**, with a clear shape per style.

The user called round 2 "a good direction". The families (F01 to F04) are still **proposals** until the user approves them.

## Files (rbxyta-assets)
- **Renders:**
  - `reference/concepts/guests/round2/`: one image per guest (`S01_MartinPike.png` and so on), a group shot per booking (`P01_Ellis_pair.png`, `F01_OkaforLind_family.png` and so on), and `lineup_batch1.png` / `lineup_batch2.png`.
  - Round 1 (rejected as too plain) stays in `reference/concepts/guests/`.
- **Asset render sheets for Codex:** `reference/concepts/guests/sheets/<ID>_<Name>_sheet.png`. Each sheet has:
  - front, side and back views on a stud grid;
  - the beauty shot and the face decal;
  - the hair, outer layer and accessories shown separately;
  - every material's hex code and fabric;
  - the R15 scale values.
- **Parts as FBX:** `export/characters/guests/R0_Guest_<Name>_Concept.fbx`. The parts are named `R0_Guest_<First>_<part>_<piece>`, with the pivot at the feet.
- **Sources (Blender 5.2, run headless):** `characters/guests/concepts/`
  - `concept_guests.py`: fabrics, scene and the character sheet data;
  - `concept_guests_v2.py`: heads, hair, hands, outfits and poses;
  - `sheet_guests.py` and `compose_sheets.py`: the asset sheets;
  - `guests_batch1.blend` and `guests_batch2.blend`.

## Additions beyond the character sheets (cut any the user dislikes)
Accessories added for character in round 2, on the user's "unique feel" brief:
- **Leena:** binoculars.
- **Gwen:** a handbag and pearl earrings.
- **Arthur:** a flat cap, bow tie, pocket square and elbow patches.
- **Aisha:** gold hoops and a watch.
- **Tom:** headphones and a flannel shirt tied round his waist.
- **Nia:** a silk scarf, sunglasses on her head and a crossbody bag.
- **Beth:** hair clips, a pendant and a canvas tote.
- **Callum:** a skinny tie and a watch.
- **Dawn:** a hard hat on her belt, a radio and a folded hi-vis vest.
- **Pete:** a bobble hat and a thermos.
- **Ivo:** safety glasses and a utility belt.
- **Kelly:** a backwards cap, ear defenders and gloves.
- **Families:** Isla waves, and Ollie holds a wildflower.

Related: [[Guest Model Import]] · [[Ordinary Guests - Character Sheets]] · [[Art Bible]] · [[Work Board]]
