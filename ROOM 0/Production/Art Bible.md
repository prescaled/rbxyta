---
tags: [room0, production, art]
status: proposal
---

# Art Bible

The one art standard both AIs follow, so models from Claude and Codex look like the same game. Workflow: [[Collaboration Workflow]].

## Look (updated 2026-10-24: Roblox style)
**Decided 2026-10-24:** the game should feel like a **Roblox game**, not a realistic render. The style reference is the spawn of *Animal Hospital* (screenshots in `rbxyta-assets/reference/style/`). Copy its **style**, never its layout, buildings or decorations: our spawn is our own hotel, quay and staff buildings.

What "Roblox style" means for every model and area:
- **Chunky and readable.** Big simple blocks, thick proportions, clear silhouettes you can read from far away. No tiny bevels or thin realistic detail. Ornate things (lamps, fences, signs) get **bold, oversized** scrolls and finials.
- **Warm and saturated.** Night scenes are a dark blue sky with **warm orange/yellow pools of light**, glowing windows and bright accents. Colours are clearly visible, not grey or washed out.
- **Roblox materials first.** Build with Parts and simple meshes using Roblox materials (Brick, Cobblestone, WoodPlanks, Asphalt, Concrete, SmoothPlastic, Metal, **Neon** for lights). Use SurfaceAppearance only where a material can't do it.
- **Built from parts where possible.** Buildings, roads, pavements, walls, signs and simple props are Part builds in Studio. Blender is for shapes Parts can't make well (vehicles, ornate iron, curved trims, characters).
- **Readable gameplay.** Big signs with bold text, **glowing floor pads** for things you can use (lobbies, shops), and **floating labels** (BillboardGui) such as `Classes` or `2/4  0:20`.
- **Dense, not wide.** Small areas packed with props: lamps, benches, bins, fences, trees, planters, signs, lit windows. Every view should have something to look at.
- **Our identity**: the 1990s Ashbourne hotel palette below (walnut, brass, deep red, green, cream).
- **Seasonal decorations** (pumpkins, cobwebs, snow) only as timed events in their own folder, never baked into base models.

## Scale (Roblox studs)
| Thing | Size |
|---|---|
| Grid | 1 stud; snap big pieces to 2 studs |
| Player height | about 5 studs |
| Door | 4 wide x 7.5 tall |
| Wall height (floor to ceiling) | 12 studs |
| Corridor width | 8 studs |
| Modular wall piece | 8 x 12 studs |
| Table height | 2.5 studs |

In Blender, set up one **template scene** with these reference sizes and a dummy player, and start every file from it.

## Export rules
- Apply all transforms (scale and rotation) before export.
- **Pivot** at the bottom centre of the object.
- Export **FBX**, check the scale on import in Roblox once, then never change the settings.
- Clean names for meshes and materials (no "Cube.001").

## Polygon and texture budget
| Type | Max triangles |
|---|---|
| Small prop (cup, key) | 500 |
| Normal prop (chair, lamp) | 2,000 |
| Furniture / large prop | 5,000 |
| Hero (shuttle van, predator, reception desk) | 10,000 |
| Hard limit per Roblox mesh | Check the current Roblox MeshPart limit |

- Textures: **1024 x 1024 max**; 512 for small props.
- Use **SurfaceAppearance** (colour, normal, roughness, metalness) for PBR detail.
- Reuse **shared trim sheets and materials** from `textures/`: wood, brass, carpet, wallpaper, tile.

## Naming
`R0_<Area>_<Object>_<Variant>`
- Areas: `Spawn`, `Lobby`, `Reception`, `Corridor`, `Room`, `Staff`, `Shop`, `Char`, `Prop` (shared), `FX`
- Examples: `R0_Lobby_Sofa_A`, `R0_Corridor_Wall_Straight`, `R0_Spawn_StreetLamp_Flicker`, `R0_Char_Bellhop`
- Roblox Packages use the same name.

## Colour palette (Roblox style, brighter than the first draft)
| Use | Colour |
|---|---|
| Wood (walnut) | #6B4430 |
| Brass / gold trim | #D4A24C |
| Hotel red | #B3262E |
| Hotel green | #2E6B4A |
| Wall cream | #F0E2C4 |
| Brick | #8A4B3A |
| Iron (fences, lamps) | #1E1E24 |
| Night sky | #141A2E |
| Lamp glow (Neon) | #FFB347 |
| Window glow (Neon) | #FFD27A |
| Lobby pad glow (Neon) | #FFD21F |
