---
tags: [room0, production, gameplay, status]
status: building
updated: 2026-10-26
---
# First Shift Implementation

## Current owner brief

Owner's **v3, 2026-10-25** replaces both earlier briefs. Claim on [[Work Board]]:
**First shift: guests, requests and shift tasks (game code)**, R+X. Revised claim
pushed as `9911e8c` before v3 implementation.

- Hotel place **133290122655457**; script folders named `R0_Game` only.
- Sources: `rbxyta-assets/tools/studio_hotel/shift/`.
- P+C owns `Workspace.HotelV2`, its build scripts and lighting. Never rebuild/move/delete
  its content from game code. Read [[Hotel Gameplay Markers]] before binding gameplay.
- Physical tasks: booking record → correct key → handover; finite stock pickup → carry
  → knock → delivery; inspect → appropriate tool/part → hands-on repair; camera watch
  and report; answer/log/call/transport records; checkout-only turnover; group accounting.
- No progress bars or hold-E timers; no quest markers over guests.
- Keep the ordinary roster separate from missing cases. Night 1 uses the canon empty-room call.
- Preserve residents, offsite occupancy, loaned equipment and relevant memory between
  nights. Full checkout and turnover are distinct from leaving temporarily.

## Approved clarifications

Owner explicitly approved written dialogue plus neutral UI labels, omitted unwritten
story lines, and balance numbers marked **proposed**. Owner delegated reusable guest rig
and animation choices to Codex; character identities/looks still follow the booking notes.
Owner also asked for these notes to be updated. Unresolved questions remain in [[Open Questions]].

## Build stages

1. S01 Martin Pike and S02 Leena Shah: full ordinary stay, lounge use, one request type
   each, plus a content/no-request path.
2. P01 Gwen/Arthur Ellis and P02 Aisha/Tom Reed: independent members, shared room records,
   twin confirmation, reunion and complete checkout.
3. T01 Nia/Beth/Callum and Q01 Dawn/Pete/Ivo/Kelly: shared equipment, separate returns,
   group requests and approved three/four-person capacity. Defer if rooms are unsuitable.

Refer to [[Ordinary Guests - Scheduling and Production]] for the full acceptance list.

## Integration evidence / outstanding

### Latest checkpoint — 2026-10-26

- Owner approved stopping Play and installing R0_Game. Fourteen script sources are
  now installed under the allowed script folders; all pass Studio syntax validation.
- P+C's new markers and HotelAPI are verified in the live Hotel. Startup reports zero
  missing dependencies. Studio API access is enabled and the coin profile loads as Saved.
- Client GUI receives server state. A client-remote clock-in (test player positioned
  at the clock) started Night 1; Martin spawned and moved toward reception.
- Subsequent Play restarts/stops interrupted testing. No full shift, two-player run,
  two-night acceptance run or requested screenshot set has passed.
- Pure Luau domain tests pass: continuity, no-request checkout, capacity/twin checks,
  group stock, exclusive loans, disconnect recovery and idempotent coin receipts.
- Game code now calls P+C's API for stock/refunds, keys, doors and room states, uses
  shared portable props and follows authored guest routes with blocked-area costs.
  Inspect/fit/test repair actions are implemented for a genuinely broken fixture.
- Remaining implementation: full check-in selections, lounge activities and authored
  guest appearance, loan retrieval/return, physical turnover steps, camera reporting,
  contextual requests, complete inspection inputs and visual/audio polish. API integration
  does not mean these tasks are finished. See the source folder's README for the backlog.
- Room 105 is now triple capacity (double + single); Room 106 has four singles. The
  draft T01 separate-bed requirement needs reconciliation before Stage 3 is enabled.
- Existing unrelated Wall Jump Kit errors remain in Output. No P+C scripts were edited.
- Keep Work Board **building**, not review. Owner should use **File > Save to Roblox**
  to preserve the installed scripts.

### Earlier evidence (superseded where the checkpoint above says otherwise)

- Read all requested vault chapters, Roadmap Phase 2, CCTV, incidents and Night 1 rules.
- Miro is private and requires sign-in; live board content has not been verified.
- Initial live scene: seven R0_Task models, Room 101 only, no staff clock marker.
- P+C subsequently added a local marker-contract note describing rooms 101–104,
  reception, staff clock, finite stock, fixables, lounge and drying targets. Live rebuild
  and navigation still need verification. There is no suitable triple/quartet room yet.
- Studio was already in P+C's Play session; no R0_Game scripts have been installed,
  and no play session has been interrupted or started by R+X.
- Earlier timer-based draft is superseded and archived locally outside the asset repo.
  Its ten files compiled, but that result is **not** evidence for the v3 implementation.
- One-player/two-player, two-night tests, persistence failure tests, and requested actual
  check-in/delivery/repair/phone/inspection captures are **pending**.

## Completion protocol

Commit/push v3 sources and relevant notes, preserving P+C's local changes. Mark the
claim review only with an honest test report and explicit remaining blockers. Ask the
owner to use **File → Save to Roblox** after verified installation. Do not claim a
finished playable shift or completed screenshots before the actual interactions work.
