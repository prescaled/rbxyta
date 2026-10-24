---
tags: [room0, production, art]
status: proposal
---

# Art Bible

The one art standard both AIs follow, so models from Claude and Codex look like the same game. Workflow: [[Collaboration Workflow]].

## Look (decided 2026-10-24: detailed stylised Roblox look)
**Stylised like a popular Roblox game, but detailed.** The user's reference is the spawn of *Animal Hospital* (screenshots in `rbxyta-assets/reference/style/`). It shows the *kind* of object models we want: readable, slightly chunky, warm, clearly "Roblox". Copy the **style only**, never its layout, buildings, signs or Halloween decoration. Everything we build is the Ashbourne Hotel's own world.

**Not flat blocks.** Plain coloured boxes are only for blockout. Every finished model, wall, floor and ceiling must have real detail. The hotel is full of tasks and props, so it needs lots of things to look at.

What that means:
- **Shapes**: stylised proportions (a bit chunky, easy to read from a distance), but real modelled detail. Bevels, frames, trims, mouldings, panels, handles, hinges, bolts, cushions, folds, and wear on the edges.
- **Walls and buildings**: never one flat part. Use layers: skirting board, dado rail, wainscot panels, wallpaper above, crown moulding, door and window frames with sills, pilasters, brick with stone quoins and lintels outside, gutters and pipes, signs, awnings, lit windows with curtains.
- **Floors and ceilings**: patterned carpet with borders, tiles with grout, wooden boards, rugs, ceiling coves, light fittings, vents.
- **Textures**: hand-painted or stylised textures (not photos), 512 to 1024 px. Use colour plus normal maps through SurfaceAppearance where it helps, or Roblox MaterialVariants for walls and floors (brick, wallpaper, carpet, tiles, planks). Shared trim sheets live in `textures/`.
- **Models come from Blender** (via MCP or headless), textured, as MeshParts. Studio Parts are only for blockout, collisions and simple glowing bits (Neon rings, light strips).
- **Lighting and readability** (from the reference): dark blue night outside, strong warm lamps with glow, cream lit windows, a **gold Neon ring or outline** on anything you can use (lobby pads, class pedestals, shop counter, task spots), and **big floating serif labels** (gold fill, dark stroke) over pads and zones.
- **Dense**: every corner has props (benches, bins, crates, planters, posters, trolleys, carts, signs).
- **Our identity, not Halloween**: no pumpkins, cobwebs, spiders, cartoon ghosts or orange-and-purple themes. Old, weathered **gravestones are allowed** (user 2026-10-24) as long as they look real and worn, not cartoony. The signature colours are **Ashbourne burgundy, brass gold and deep teal**.

The story setting is still a 1990s hotel that's a bit tired. It's drawn in this detailed stylised way.

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

Triangle budgets above stay. Spend them on silhouette and detail you can see, not on hidden faces.
