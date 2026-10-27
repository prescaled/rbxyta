---
tags: [room0, gameplay, guests, art, characters]
status: proposal
updated: 2026-10-26
---

# Ordinary Guests: Character Sheets

**Asked for by the user on 2026-10-26:** guest appearance descriptions for Codex to build the characters. Some guests arrive with friends or with kids, and **every guest must look clearly different from every other guest**.

This note turns the written looks in the booking notes into build specs: [[Ordinary Guests - Solo Bookings]], [[Ordinary Guests - Pair Bookings]] and [[Ordinary Guests - Group Bookings]]. Where a booking note already describes someone, **that text wins**. This sheet only adds the detail a modeller needs.

The **family bookings with children (F01 to F04) are new proposals** made for this request. They need the user's OK before they count as canon.

Work Board item: `R0_Char_Guests` (R+X). Style: the detailed stylised Roblox look from the [[Art Bible]], not flat blocks.

## How to make them all different

Every guest must differ from everyone else in **at least three** of these five things, so you can tell them apart at a glance, from the desk and on CCTV:
1. **Height and build:** use R15 scale values. Adults range from short to tall and from slim to broad. Children are clearly smaller (see the child rules below).
2. **Hair shape and colour:** bob, braid, curls, bald, cap, knot, fringe, swept back, and so on. No two guests share the same hairstyle in the same colour.
3. **Outer layer:** the shape and colour of the coat, jacket, jumper or cardigan. This is the biggest coloured area.
4. **Signature item:** the one prop or bag only they carry.
5. **Skin tone:** a wide, realistic range across the roster.

Rules:
- Give **each booking a colour story** so a party reads as a group. The members still keep their own pieces (the road crew shares worn blue workwear, but each member has their own accent).
- Use the hotel palette (burgundy, brass and teal) **sparingly on guests**, so staff uniforms stay recognisable.
- Use the shared rig, walk, sit, read, carry, phone and pack animations. Make people distinct through **posture and idles**, not custom rigs. Examples: Martin straightens his tie, Leena cleans her glasses, a child swings their arms.
- **File photo:** every guest needs a front-facing head-and-shoulders render against a cream backdrop for the check-in terminal. It must match the 3D model exactly; ordinary guests always match their file.
- **Anomaly versions** are built from a copy of a guest's model with one or two tells changed (see [[Task Interfaces#Ordinary versus anomaly]]). **Never** make anomaly versions of children, or of the families below.

### R15 scale guide (starting values, tune in Studio)
| Body type | BodyHeightScale | BodyWidthScale | HeadScale | BodyProportionScale |
|---|---|---|---|---|
| Short adult | 0.92 | 0.95 to 1.0 | 1.0 | 0.3 |
| Average adult | 1.0 | 1.0 | 1.0 | 0.3 |
| Tall adult | 1.08 | 0.95 | 1.0 | 0.4 |
| Broad adult | 1.0 | 1.1 to 1.15 | 1.0 | 0.2 |
| Teen (16 to 19) | 0.97 | 0.92 | 1.0 | 0.3 |
| Child (9 to 12) | 0.78 | 0.85 | 1.08 | 0 |
| Young child (5 to 8) | 0.66 | 0.82 | 1.15 | 0 |

## Starting set: 13 people (first build, from the Ordinary Guests Index)

### S01 · Martin Pike, 47 (solo)
- **Body:** average height, slightly soft build, upright "salesman" posture.
- **Skin and face:** light skin with ruddy cheeks, and a practised wide smile.
- **Hair:** sandy, flattened and damp from rain on one side.
- **Clothes:** navy suit jacket with an old lapel pin, a pale blue shirt, a loosened maroon tie, grey trousers and brown practical shoes. A sample brochure is folded into his breast pocket like a handkerchief.
- **Signature item:** a black wheeled case with one wobbling wheel.
- **Idle:** straightens his tie and mouths his presentation.
- **Read at a glance:** navy suit plus a wheeled case.

### S02 · Leena Shah, 31 (solo)
- **Body:** short, slim and quick-moving.
- **Skin and face:** medium-brown skin and an observant look.
- **Hair:** cropped dark hair.
- **Glasses:** round amber frames.
- **Clothes:** a rust waterproof jacket over a grey jumper, dark green field trousers and clean white indoor trainers. Muddy boots hang from a strap on her rucksack.
- **Signature item:** a small field notebook in a chest pocket.
- **Idle:** cleans her glasses, or glances at the window.
- **Read at a glance:** rust jacket plus boots on her pack.

### P01 · Gwen Ellis, 66, and Arthur Ellis, 68 (pair)
- **Colour story:** blue and brown, warm and smart.
- **Gwen**
  - **Body:** short and neat, with a light, brisk walk.
  - **Skin and face:** fair skin.
  - **Hair:** grey with a blunt fringe, chin length.
  - **Clothes:** a cobalt scarf, a camel wool coat, navy trousers and low heels.
  - **Signature item:** a compact silver camera on a wrist strap.
- **Arthur**
  - **Body:** tall, a slight stoop, broad shoulders.
  - **Skin and face:** fair skin and a big grey moustache.
  - **Hair:** balding with grey sides.
  - **Clothes:** a brown and cream checked jacket, a mustard knitted vest, brown cords and polished brogues.
  - **Signature item:** a bunch of flowers in increasingly battered paper.
- **Read at a glance:** a short woman in cobalt beside a tall man in checks holding flowers.

### P02 · Aisha Reed, 46, and Tom Reed, 19 (pair, mother and son)
- **Colour story:** green and faded navy.
- **Aisha**
  - **Body:** average height, sturdy build, purposeful walk.
  - **Skin and face:** dark brown skin.
  - **Hair:** tightly pinned black hair in a low bun.
  - **Clothes:** a practical green belted coat, black trousers and comfy flat boots.
  - **Signature item:** an overfilled patterned tote with a map sticking out.
- **Tom**
  - **Body:** teen build, tall and lanky (BodyHeightScale 1.05, width 0.9), shy posture with his hands in his pockets.
  - **Skin and face:** dark brown skin.
  - **Hair:** loose black curls.
  - **Clothes:** a faded navy astronomy sweatshirt with a small planet print, grey joggers and scuffed trainers.
  - **Signature item:** a backpack with a broken zip pull, held with a safety pin.
- **Read at a glance:** a green coat beside a tall, slouching teen with curls.

### T01 · Nia Brooks, 28; Beth Lane, 29; Callum Ross, 30 (trio, wedding guests)
- **Colour story:** dressy travel clothes, purple, floral and grey.
- **Nia**
  - **Body:** average height, poised.
  - **Skin and face:** deep brown skin.
  - **Hair:** a neat dark bob.
  - **Clothes:** a purple travel jacket, black jeans and ankle boots.
  - **Signature item:** a long garment bag over her shoulder, and a phone always in her hand.
- **Beth**
  - **Body:** short, bouncy and animated.
  - **Skin and face:** pale skin with freckles.
  - **Hair:** voluminous copper curls.
  - **Clothes:** a cream cardigan, a yellow T-shirt, blue jeans and bright white trainers.
  - **Signature item:** a floral dress carrier.
- **Callum**
  - **Body:** tall and thin, calm and upright.
  - **Skin and face:** light olive skin and a short neat beard.
  - **Hair:** short dark brown hair, side-parted.
  - **Glasses:** rectangular black.
  - **Clothes:** a grey zip jacket over a white shirt, dark chinos and smart shoes.
  - **Signature item:** a suit on a hanger in clear plastic, plus a tiny sewing kit.
- **Read at a glance:** a bob with a garment bag, copper curls with a floral carrier, and a tall man in glasses with a suit.

### Q01 · Dawn Keating, 44; Pete Nolan, 51; Ivo Novak, 37; Kelly Watts, 26 (quartet, road crew)
- **Colour story:** worn workwear in blue and grey, each with a hi-vis accent. Hi-vis vests come off before they sit in public spaces; they carry them.
- **Dawn**
  - **Body:** average height, solid and steady.
  - **Skin and face:** light-medium skin and a weathered look.
  - **Hair:** a compact brown braid.
  - **Clothes:** a weathered blue work jacket, cargo trousers and steel-toe boots.
  - **Signature item:** a clipboard with the job sheet.
- **Pete**
  - **Body:** broad and big-bellied (width 1.15), with a rolling walk.
  - **Skin and face:** fair skin, red cheeks and grey stubble.
  - **Hair:** a grey knitted cap.
  - **Clothes:** a padded navy gilet over a plaid shirt, and work trousers.
  - **Signature item:** a large dented lunch tin.
- **Ivo**
  - **Body:** tall and lean, careful movements.
  - **Skin and face:** fair skin and a close dark beard.
  - **Hair:** short dark hair.
  - **Clothes:** a charcoal softshell jacket, tidy dark work trousers and meticulously clean boots.
  - **Signature item:** a labelled tool roll.
- **Kelly**
  - **Body:** short and athletic, energetic.
  - **Skin and face:** brown skin.
  - **Hair:** short black curls.
  - **Clothes:** a grey hoodie under an open orange hi-vis vest, black work trousers and boots.
  - **Signature item:** a bright orange water bottle.
- **Read at a glance:** a braid, a broad man in a knitted cap, a tall bearded man, and a short woman with an orange bottle.

## New proposal: families with children (F01 to F04)

**Not canon until the user approves.** These follow the booking rules (1 to 4 people per booking, a suitable room and sleeping arrangement for every person) and the tone of [[Ordinary Guests - Design Bible]]: ordinary families who leave normally.

**Child rules (always):**
- Children are **never** targeted by horror events, predators, missing-person cases or anomaly versions.
- A child is never in a room or corridor without one of their adults nearby.
- Children's requests go through their adult.
- Children have their own idles (fidgeting, swinging their arms, sitting on the floor with a toy), and their own kid-sized luggage.

### F01 · Grace Okafor, 38; Henrik Lind, 40; Ada Okafor-Lind, 9; Leo Okafor-Lind, 5 (family of four)
- **Visit:** two nights on the way to see grandparents. They need a family room: a double plus two singles, or a double plus a bunk.
- **Colour story:** bright and outdoorsy, with yellow, red and denim.
- **Grace:** average height and slim. Dark brown skin, and black hair in long braids tied up in a yellow headwrap. A red puffer jacket, jeans and white trainers. She carries a wheeled family suitcase and a snack bag.
- **Henrik:** very tall (1.1), lanky. Pale skin and a blond beard, with his hair in a short ponytail. A dark green parka, grey jumper, brown boots and a big hiking rucksack. Leo's car seat hangs from his hand.
- **Ada (9):** child scale. Medium-brown skin and two puffy bunches tied with red bobbles. A yellow raincoat, purple leggings and wellies with frog faces. She holds a chapter book with her finger in it.
- **Leo (5):** young-child scale. Medium-brown skin and short curls. Dinosaur pyjama-style joggers, a green hoodie with spikes on the hood, and light-up trainers. He drags a toy dinosaur by its tail.
- **Possible requests:**
  - an extra blanket;
  - a night light or a working bedside lamp;
  - help finding Leo's dinosaur, which is left in the lounge. This uses request type 26 from [[Ordinary Guests - Activities and Encounters]].

### F02 · Sam Whitfield, 35, with Poppy and Finn Whitfield, 7 (single dad with twins, trio)
- **Visit:** one night on the way to a seaside holiday. They need a double plus a single, or a triple room.
- **Colour story:** matching holiday stripes.
- **Sam:** average height, broad build. Light skin, a ginger beard and a ginger messy top-knot. A navy and white striped long-sleeve top under an unzipped olive jacket, cargo shorts over leggings (a dad holiday look), and walking sandals with socks. He wears a big holdall across his body and a kids' backpack on one shoulder.
- **Poppy (7):** young-child scale. Light skin, freckles and long ginger hair in one plait. A matching striped top, a pink skirt over leggings, and red shoes. She carries a bucket and spade even though it's night.
- **Finn (7):** young-child scale. Light skin and short ginger hair sticking up. A matching striped top, blue shorts, a plaster on one knee, and trainers. He has a handheld game console on a lanyard.
- **Read at a glance:** three matching striped tops. The twins are the same height but clearly different: a plait and skirt against spiky hair and shorts.
- **Possible requests:** a spare pillow; quiet-room preference; a wake-up call for an early start.

### F03 · Marjorie Dunn, 64, and Jamie Dunn, 11 (grandmother and grandson, pair)
- **Visit:** two nights. Jamie has a chess tournament in town. Twin beds.
- **Colour story:** heather purple and school-uniform grey.
- **Marjorie:** short and plump. Fair skin and rosy cheeks. Short permed white hair, and big purple glasses on a chain. A heather-purple quilted coat, a floral blouse, a tweed skirt and sensible shoes. She carries a tartan shopping trolley bag and a tin of biscuits.
- **Jamie (11):** child scale. Light-brown skin, neat short black hair and a serious expression. A grey school-style blazer with a chess club badge, a white shirt, black trousers and black shoes that are too big. A folding chess board is under his arm.
- **Possible requests:** a table to practise chess on; an extra blanket; a taxi confirmation for the tournament.

### F04 · Priya Nair, 36, with Isla Nair, 8; Hannah Cole, 34, with Ollie Cole, 6 (two friends and their kids, quartet)
- **Visit:** two nights, a mums' weekend away with the kids for a wildlife park. They need a family room for four.
- **Colour story:** two families with clearly different palettes: Nair in teal and white, Cole in coral and denim.
- **Priya:** tall and slim. Brown skin and long, wavy black hair in a side ponytail. A white puffer gilet over a teal long-sleeve top, black leggings and trainers. She has a sling bag and is always holding coffee.
- **Isla (8):** young-child scale, the tallest of the two kids. Brown skin, and black hair in two plaits with teal ribbons. A teal tracksuit with a white stripe, and a wildlife-park cap with animal ears.
- **Hannah:** short, curvy build. Fair skin and a short blonde bob with a coral clip. A coral raincoat, a denim dungaree dress over a striped top, and yellow wellies. She carries a huge tote with a stuffed giraffe poking out.
- **Ollie (6):** young-child scale. Fair skin, white-blond hair in a bowl cut, and a gap-toothed grin. A denim jacket covered in patches, red trousers, and wellies on the wrong feet.
- **Possible requests:** extra towels after the rain; a jug for wildflowers the kids picked; help finding Ollie's other welly.

## Remaining roster (later)
The other 33 named guests keep the looks written in their booking notes. Turn them into full sheets like the ones above before each expansion stage, and run the five-point difference check against everyone already built.

## Related
[[Guests]] · [[Ordinary Guests - Index]] · [[Task Interfaces]] · [[Anomalies]] · [[Art Bible]] · [[Work Board]]
## Separate staff character reference

For the regular employees working alongside the players, see [[Resident Staff - Character Profiles]] and [[NPC Character Notes]]. Staff appearances are new character proposals; their inclusion does not overwrite the guest or family designs above. NPC employees are separate from selectable player [[Classes]].
