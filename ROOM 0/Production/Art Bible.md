---
tags: [room0, production, art]
status: proposal
---

# Art Bible

The one art standard both AIs follow, so models from Claude and Codex look like the same game. Workflow: [[Collaboration Workflow]].

## Look
- **Realistic, slightly worn 1990s hotel.** Not cartoony, not Halloween ([[Spawn Mood and Lighting]]).
- Warm wood, brass, deep red and green fabrics, cream walls, patterned carpet. Everything a little old and tired.
- Detail comes from **many props**, not from very heavy single meshes.

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

## Colour palette (starting point)
| Use | Colour |
|---|---|
| Wood (dark walnut) | #4A2E1F |
| Brass | #B08D57 |
| Carpet red | #6E1F24 |
| Fabric green | #2F4A3A |
| Wall cream | #D9CBB0 |
| Night fog blue | #2B3440 |
| Lamp sodium orange | #E8A04A |
