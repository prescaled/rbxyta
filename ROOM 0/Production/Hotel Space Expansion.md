# Hotel space expansion — 2026-10-29

User approved keeping detailed hotel materials and widening spaces, using the reference screenshots for spaciousness only.

Applied in Edit to Hotel 133290122655457:
- Guest corridors 12 → 18 studs wide.
- Guest rooms 28 × 24 → 34 × 24 studs.
- Staff corridor 8 → 12.2 studs.
- Reception and central lobby stay in place. Original materials, furniture proportions and room themes retained.
- Architecture, door pivots/hinges, navigation markers/volumes, CCTV coordinates and outer scenery follow the expansion.
- No objects deleted; original transforms stored in R0_SpaceBase attributes for rollback.

Source: rbxyta-assets/tools/studio_hotel/v2/ExpandSpaces.lua. Installed at ServerStorage.HotelV2.ExpandSpaces. Rebuild and rollback instructions: adjacent EXPANDED_LAYOUT.md. This is a post-build migration: the old Plan is intentionally the base; run migration after rebuilding. Do not run the original coordinate checks unchanged against the migrated layout.

Verification: measured 18-stud corridor and 34 × 24 Room 102; checked furniture sizes unchanged; corridor wall-ray gaps match gallery arches. All six corridor-to-room paths passed. Reception-to-room tests passed for all six with Room 102's door open through its existing door system; restored its prior closed state. MCP screenshots inspected Room 102 and guest corridor.
No new alcoves or lighting overhaul in this width pass. Full two-night NPC acceptance is still pending.
User began Play during validation; left their Play session running. Save Hotel using File > Save to Roblox afterward.
