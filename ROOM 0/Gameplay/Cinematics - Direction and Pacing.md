---
tags: [room0, gameplay, cinematics, cctv, design]
status: detailed-proposal
updated: 2026-10-27
---

# Cinematics: Direction and Pacing

Design proposal, 27 October 2026. Index: [[Cinematics and CCTV - Index]].

## Three scene formats

**World sighting:** approximately 1-6 seconds, staged inside normal play. The player keeps movement, look and ordinary HUD. A corridor crossing is not a reason to force a five-second camera turn. Optional sound and composition attract attention; missing it is acceptable.

**Interactive discovery:** approximately 6-15 seconds if the player chooses to investigate. Looking at a monitor, lifting a found record or opening an ordinary authorised door creates the framing. The player can exit safely. Keep relevant captions, controls and accessibility aids.

**Chapter cinematic:** approximately 10-30 seconds, with 40 seconds as an occasional upper bound. Use for arrival, major transitions and inspection. Short camera paths and optional letterboxing suit these deliberate pauses. The earlier 10-40 second rule in [[Cutscenes]] remains for chapter scenes, not every apparition.

Most new scares should be world sightings. A player who spots something while freely looking has made a discovery; a camera that constantly grabs their head teaches them to wait for the next animation.

## Variety in what makes the moment unsettling

- **Fast crossing:** a readable silhouette passes behind a doorway before the player reaches it.
- **Slow approach:** a distant figure is slightly nearer on the next check.
- **Near presence:** a figure stands just behind a person who cannot see it directly.
- **Occlusion:** a column or closing door hides the figure, but it does not emerge where it should.
- **Reflection:** glass shows a person whose physical counterpart is absent.
- **Routine interrupted:** a receipt, lift arrival or service corridor behaves wrongly during ordinary work.
- **Quiet absence:** the expected second sound or second person never arrives.
- **Recorded contradiction:** observed footage and a later observation disagree in a specific, reviewable way.

Do not default to a scream, red screen and running silhouette for every variation. The hotel supplies its own sounds: carpeted footsteps, a case latch, a lift relay, a door closer, a trolley wheel. Avoid strobe effects and rapid full-screen white flashes.

## Proposed intensity ladder

**Night 1:** preserve the canon empty-room call and believable work. At most one additional low-intensity environmental moment, with no named apparition or first-night predator introduced by this pack.

**Nights 2-3:** introduce a clearly wrong but non-damaging sighting or reportable feed discrepancy. Do not treat every incident as a chase.

**Later nights:** combine an established rule with a stronger presentation or a story-gated likeness. Actual predator incidents use the separately approved threat system and readable danger signals.

Existing [[Anomalies]] notes contain their own proposed predator night gates; this pack does not silently change them. The exact combined schedule remains a balancing decision.

Initial test envelope for a proposed 15-minute shift: zero or one chapter scene beyond the necessary arrival/inspection, one prominent sighting, and one or two eligible CCTV incidents. This is a test envelope, not a fixed shift length or a demand for three scares. Allow quiet shifts and test longer silence before increasing frequency.

After a prominent event, leave at least 90 seconds of ordinary work without another high-intensity incident as a starting value. A clearly dangerous encounter blocks cosmetic scares entirely. Do not count opening a menu or random flicker as an obligation to spawn the next event.

## Fair triggers

A scene needs a valid stage, a safe location, an eligible narrative state and a plausible attention opportunity. A line-of-sight check determines whether a world sighting can be framed; it should not guarantee that every player notices.

Do not trigger a near-body scare while a player is falling, carrying an item through a dangerous edge, typing, handling a critical choice or exiting another camera interaction. Delay the event rather than yanking control away.

A scene should not teleport an ordinary guest, displace a staff job or change a checked-in roster. Use a distinct apparition instance with separate identity and collision rules. Players must not be able to check an apparition in, steal its props or accidentally hurt a regular guest through a shared hitbox.

Missing a sighting spends no coins and removes no required clue. If an event contains mandatory information, give it an accessible later record or a replayable discovery through the normal progression system. Do not repeat the exact scare every time someone crosses the trigger.

## Gaze and disappearing without a trace

A figure may pass behind a real occluder and be gone when the player reaches it. That satisfies "without a trace" without a loud dissolve, dropped key or glowing footprint every time.

For look-away events, distinguish an intended disappearance rule from rendering bugs. The server commits the incident state and supplies a consistent state to eligible clients. Do not despawn a shared figure merely because one distant player rotates their camera.

If a figure is camera-only, all people watching that same live feed at that time see the same incident state. A field player can see no figure in the world; that difference is intentional and documented. A camera still captures what the selected feed showed, not what a different layer would have shown.

## Player control, skipping and recovery

All chapter scenes should offer an accessible exit; the existing promise of repeat-view skipping remains. Recommendation: permit first-view skip too, with important factual information available afterward. This is a proposed usability refinement, not an already deployed rule.

Use one final restoration path for completion, skip, damage interruption, disconnect and scene failure: restore movement, camera type/target, interaction ownership, visible UI, audio state and item state.

If a scripted camera takes control, protect that player from unrelated damage and do not penalise an unavoidable service deadline while they are locked. Prefer scenes at naturally safe handovers. If making that protection fair in co-op is not practical, remove the camera lock.

A knocked-out scene follows [[Health]] and the actual revival outcome. Never always show waking on a cot if a teammate revived the player where they fell.

## Co-op and solo

Up to four players can have different roles in one incident: observer at the monitor, colleague in the corridor, person arriving too late and person still dealing with reception. Do not cut all four to the same dramatic shot whenever one encounters a figure.

Use shared incident IDs, phase times and per-player eligibility. One player's skip only exits that player's presentation; it cannot erase evidence or restart the event for everyone.

Solo versions do not require a second player to generate the scary composition. A corridor camera may show a figure behind the player's recorded recent route, or a camera covering the security entrance may show a presence outside. These are explicit variants, not fake recordings labelled live. No first-person cinematic should require a real stranger to stand in exactly one spot.

## Case-specific sightings

A recognisable missing guest is a stronger story beat than a generic shadow. Introduce a case through its proper evidence first; otherwise the scene becomes an unexplained character advertisement.

Marnie can be suggested by the uneven bob, green cardigan and battered tool case. Vincent and Audrey can be suggested as a pair, with silhouette and clothing details already established. A Mercer-labelled variant waits for approved appearance assets.

Do not animate Marnie solving the piano mystery or show the earlier Shaw separation as a random scare. Those would settle or disclose narrative material. The case echoes here reveal only a likeness and an impossible observation.

## Audio and access

Use positional sounds at controlled volume, with captions for information-bearing cues. Avoid requiring players to distinguish precise musical notes or hear a whisper to progress.

Reduced-effects mode removes flicker, scanline intensity, abrupt zoom and unnecessary shake while preserving the same objects, timings needed for decisions and story facts. A motion-reduced variant can leave the camera stationary and let the actor move.

For a very brief visual effect, widen the presentation opportunity or offer a later non-punitive observation. Accessibility should not remove all interesting events or label every figure before the player identifies it.

## Production notes

The current [[Art Bible]] is detailed stylised Roblox, not photorealism. Stage serious, restrained horror inside that visual world. The older wording "realistic mood" refers to tone, not a mandate to replace the approved art style.

A separate clean capture mode can record scene footage for [[The Security Archives]] and [[Content Strategy]]. It should not require intrusive letterboxing or hidden controls during ordinary gameplay.

Technical requirements are design targets: camera restoration, per-player presentations, authoritative event phases and faithful evidence capture must be prototyped. This document does not claim a working CutsceneService or live video recorder.

## Shared Miro copy

[Open this chapter in Miro](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688642333614) | [Cutscenes and CCTV overview](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688642333914)
