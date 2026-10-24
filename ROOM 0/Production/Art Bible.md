---
tags: [room0, production, art]
status: proposal
---

# Art Bible

The one art standard both AIs follow, so models from Claude and Codex look like the same game. Workflow: [[Collaboration Workflow]].

## Look (decided 2026-10-24: stylised Roblox look)
**Chunky, clean, bright-against-dark Roblox style.** The user's reference is the spawn of *Animal Hospital* (screenshots in `rbxyta-assets/reference/style/`). Copy the **style only**, never its layout, buildings, signs or Halloween decoration. Everything we build is the Ashbourne Hotel's own world.

What "the Roblox feel" means for us:
- **Simple, bold shapes.** Big readable silhouettes, slightly oversized proportions (thick lamp posts, fat kerbs, deep window frames, big signs). No fine realistic detail, no photo textures.
- **Flat colour, few materials.** SmoothPlastic and a few Roblox materials (Brick, Cobblestone, WoodPlanks, Slate, Metal, Glass, **Neon**). In Blender: flat colour materials or one small palette texture, no PBR maps.
- **Bright accents on a dark night.** Dark blue night and dark buildings, then strong warm light: amber lamps with visible glow, cream lit windows, gold Neon outlines on interactive spots.
- **Glowing interactables.** Anything you can use (lobby pads, class pedestals, shop counter) has a **gold Neon ring or outline**, so players can read the space from far away.
- **Big floating labels.** BillboardGuis in a chunky serif font (Merriweather / Garamond-style, gold fill, dark stroke) over every zone and pad: "Shuttles", "Staff Lockers", `2/4`, `0:20`.
- **Dense and busy.** Lots of small props (benches, bins, crates, planters, posters, signs) so every corner has something, like the reference.
- **Our identity, not Halloween:** no pumpkins, cobwebs, spiders, gravestones or orange-and-purple themes. Our signature colours are **Ashbourne burgundy, brass-gold and deep teal**.

Most models are **built from Parts in Studio** (fast, native Roblox feel, editable by both AIs). Blender is for curved or hero shapes only (shuttle van, lamp heads, mannequins, characters), exported low-poly with flat colours.

Older notes said "realistic, worn 1990s hotel". That still describes the *story setting* (1990s, a bit tired), but it is now drawn in this stylised way.

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

## Colour palette (stylised, decided 2026-10-24)
| Use | Colour |
|---|---|
| Night sky / fog | #121A2E |
| Dark asphalt / road | #23252E |
| Road paint | #E8E2D4 |
| Ashbourne burgundy (awnings, banners, uniforms) | #8C1C2B |
| Brass gold (signs, trims, Neon rings) | #F2C14E |
| Deep teal (doors, shutters, accents) | #1F5C63 |
| Warm brick | #9A5A3C |
| Cream lit window | #FFE7A8 |
| Lamp amber light | #FFB648 |
| Dark wood | #4A2E1F |
| Foliage (dark pine green) | #24402F |
| Stone / kerb grey | #8A8D93 |

Triangle budgets above stay, but stylised models should come in **well under** them.
