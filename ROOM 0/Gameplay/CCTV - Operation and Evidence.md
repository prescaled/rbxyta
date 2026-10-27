---
tags: [room0, gameplay, cinematics, cctv, design]
status: detailed-proposal
updated: 2026-10-27
---

# CCTV: Operation and Evidence

Design proposal, 27 October 2026. Index: [[Cinematics and CCTV - Index]]. This expands the current CCTV concept into a playable observation loop; it is not a deployed feature report.

## The experience at the desk

The player should have a useful job even when no anomaly is active: see an arrival approaching, check an ordinary passage before a delivery, notice a real guest movement and coordinate with a colleague. Most feed time should show a believable hotel.

The security desk remains the baseline observation station available to every class. Reception begins with its established single check-in monitor; the proposed extra reception CCTV monitor in [[Task Interfaces]] is an upgrade, not a retroactive replacement of that rule.

The reception screen is the approved modern ultrawide. The older CRT/security-bank idea concerns the separate security station and recorded-footage treatment. Do not replace the reception monitor with a CRT because the surveillance feed has a grain effect.

## Camera coverage

Keep 8-12 as an eventual coverage goal, not a requirement to render twelve live full-detail views simultaneously. Start with two useful cameras:
- Reception/lobby approach: arrivals and a clear portion of ordinary service.
- Main corridor/security approach: route observation and the figure-behind-player incident.

Expand as physical rooms and sightlines exist: lift landing, lounge, service corridor, back entrance and staff work area. These are location roles, not fixed camera numbers or promises that the current map has every zone.

Avoid cameras inside guest bathrooms or private bedroom interiors. Corridor doorways, authorised communal areas and service spaces provide enough information for these proposals. A camera name should tell a player where it looks.

Document blind spots. An incident relying on "no possible exit" requires verified geometry and observation, not a blind corner the writer overlooked.

## Core controls

Select feed, zoom within the available picture, toggle night vision where the camera supports it, capture an evidence frame, ping a visible location and file a report. Exiting always returns the player's camera and movement safely.

Night vision improves a dark feed; it does not see through walls, restore an offline camera or automatically reveal every hidden figure. Zoom crops/magnifies the captured view and cannot invent unreadable detail.

Camera switching may have a brief settling effect, but reduced effects removes distracting static. Persistent camera-ID and time labels remain readable. Use accessible categories and clear confirmation rather than a generic floating task popup.

## Separate live, recorded and unavailable states

LIVE shows the current server-authorised scene state for that feed. RECORDED shows a specific recorded timestamp and is visibly distinguished. OFFLINE gives a truthful unavailable state.

A feed is never secretly labelled live while actually showing a replay unless a separately authored story explicitly concerns a compromised label. That story would need a discoverable indication and cannot invalidate ordinary report rules without warning. No such compromised-label incident is approved by this pack.

A temporary signal failure may have an ordinary maintenance cause. It is not proof of a monster, and restoring power should restore the correct feed.

## Capture and preservation

A snapshot retains feed ID, server capture time, incident association where applicable and the actual observed visual state. It must not re-render the current room later and pretend that it was the saved image.

The scene may leave no physical trace while a correctly captured image remains. Do not silently erase a player's evidence for dramatic effect. A future story about corrupted evidence needs explicit narrative design and a fair retained observation route.

Initial design target: a small bounded caseboard of saved frames, with an explicit replace/archive choice if full. Exact storage size and cross-session lifetime remain open; do not silently claim infinite permanent screenshots.

If the platform cannot capture true image data in the required way, prototype a faithful rendering from recorded observed state. Verify occlusion, character poses, clock and camera-only actors. Do not advertise photographs or replay while storing only an approximate current-state picture.

## Proposed replay extension

A short 10-15 second per-feed observed-state buffer is an optional later feature. It can make a missed crossing recoverable and gives camera play an investigative rhythm.

It must not require a full video stream stored indefinitely. A proposed implementation can record relevant transforms, animations, visibility layers and event phases at bounded intervals and reconstruct them, but correctness and performance need testing.

A baseline alternative is longer live incident staging plus captured stills. Implement that first. Essential progression cannot require a replay feature that has not been built.

Returning from playback must clearly return to LIVE. An advancing recorded figure cannot attack the viewer from the recording or spawn a second incident.

## Report types and verification

**Report anomaly:** select a feed, capture a relevant observation and choose a category. Initial categories: Object discrepancy, Unidentified presence, Reflection discrepancy, Equipment discrepancy and Spatial discrepancy. Keep labels stable; do not require naming a specific missing person.

**Save sighting:** archive an optional transient event without pretending it is a timed task. A missed sighting incurs no failure penalty.

**Record story evidence:** retain the observation and its uncertainty. An accepted filing means the evidence was recorded, not that the story interpretation is correct or the extra door has vanished.

**Report ordinary maintenance:** route a verified equipment problem to the normal task system. A broken lamp is not automatically a supernatural report.

The previous broad proposal that "correct reports remove anomalies" applies only to actionable incidents explicitly designed to clear. It does not erase a story door, resolve a missing person or remove a real guest from the building.

## Fair timing and duplicates

Actionable incidents provide a reasonable observation/report opportunity, initially around 45-90 seconds depending on complexity. Exact values need testing with the real work load, camera switching time and solo play.

Validate the incident at capture time as well as submission time. A short submission grace after expiry, proposed 10 seconds, lets a player finish filing a frame captured while the ticket was valid. Define the rule consistently; never show "false" merely because a correctly captured figure vanished during form entry.

One resolved incident ticket pays once team-wide. A second player who submits the same valid evidence gets "Already recorded" rather than a false-report penalty. Preserve meaningful observation/assistance contribution without multiplying the coin award.

Invalid reports do not give coins. A reasonable mistake receives a clear result. The earlier small-time-cost proposal should be a short filing cooldown for repeated baseless submissions, initially about 5 seconds, not a hidden confiscation of time or currency. Never punish someone for exiting a report or for observing a transient event.

Coin amounts remain undecided; use the existing economy calibration. Replaying footage, copying an image or reconnecting cannot refresh a resolved ticket.

## Escalation into danger

Some existing anomaly designs may lead to predators. This pack does not remove that direction, but it requires an explicit mapping and a fair transition.

Most new catalogue events are non-damaging. For any later hostile version, specify the originating incident, warning, delay, spawn position, reachable escape and counterplay. Do not turn every missed chair or silhouette into a predator.

No unavoidable attack can spawn inside a locked camera interaction. Warn and let the player exit; suspend or cancel escalation when a safe counterplay state cannot be created. Keeping an operator at a desk should be a choice, not a requirement to sacrifice them.

Use the existing predator models/rules where approved. A transient missing-guest likeness is not automatically a valid weapon target.

## Classes, upgrades and colleagues

Night Watchman retains the proposed 8-second portable checks, 20-second recharge and two reference stills from [[Classes - Security Records and Leadership]]. The desk supports sustained work for everyone. This pack does not increase portable access or grant it replay without a separate decision.

Night Auditor can organise legitimately accessible records; it does not gain hidden camera events. Night Manager sees known work, not a list of undetected anomalies.

An extra reception monitor makes simultaneous watching convenient. It must not gate essential evidence or correct reporting. Solo players need a save-and-review route or a long enough incident window to inspect sequentially.

Regular NPC staff remain legitimate moving scene occupants. Their identities, work reservations, carried objects and breaks are not overwritten to produce a scare. A staff-like apparition is a separate staged actor, not a modified employee record.

## Shared incident model

Proposed fields for future implementation: unique incident ID, encounter template, eligible story state, allowed cameras/areas, world or camera-only presentation, start/phase/end times, active participants, capture history, report status, optional escalation link and once-per-run eligibility.

Server state decides what happened. Clients present the appropriate view. Report validation checks permissions, capture state, category compatibility and whether the ticket has already been settled.

A camera-only figure is deliberately absent from the physical-world layer. It must still appear consistently on all equivalent live viewers and correctly saved frames. A world figure cannot disappear because one unrelated player switched channels.

Clean up actors, borrowed props, camera effects and reservations on completion, cancellation and failure. Keep legitimate evidence if capture succeeded. Do not leave an invisible collider or change the real guest population.

## Pacing with hotel work

The scene scheduler considers available attention, unresolved work and recent intensity. It should not trigger a major camera incident during a mandatory chapter scene or require a first-time player to choose between a tutorial and an essential clue.

Allow shared information without requiring voice chat: location ping, short text observation and evidence sharing. An experienced player cannot spam pings to farm contribution.

If the whole team is busy, an optional sighting may happen unnoticed; that is acceptable. An actionable incident with an unfair or impossible observation window should be deferred, cancelled without penalty or offer an alternative fair route.

## Acceptance checks

Before claiming implementation:
1. Each feed identifies its location and whether it is live, recorded or offline.
2. A world-view player and camera observer see the intended different layers, not accidental desynchronisation.
3. A snapshot stays faithful after the room changes.
4. Optional sightings can be missed without penalty or lost mandatory progression.
5. Actionable reports validate a captured event during the documented grace period.
6. Duplicate correct reports settle one reward, with no false-report penalty for the second observer.
7. Ordinary staff movement does not become an anomaly just because an object changed position.
8. Every scene can exit or interrupt without stuck controls, lost items or hidden UI.
9. Reduced effects retains equivalent readable facts and counterplay.
10. A solo player can complete every required observation without buying a class or monitor upgrade.
11. Apparitions do not alter bookings, ordinary guest count, staff rota or missing-case outcomes.
12. Replay, if built, shows actual recorded state and cannot duplicate incidents.
13. Unapproved case likenesses, dates and secret explanations cannot trigger.
14. Performance is tested at the intended player count and actual camera complexity.

## Recommended build sequence

Start with two camera views, ordinary movement, reliable select/exit and saved observations. Add C01 plus correct/incorrect/duplicate-report states. Add the shared S03/C02 figure-behind-player scene. Test solo/co-op, disconnects and accessibility. Only then add phased approaches, story discrepancies, extra feeds and optional replay.

Model/scene ownership remains governed by [[Work Board]]. The production acceptance items are requirements for future work, not passed tests.

## Shared Miro copy

[Open this chapter in Miro](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688642333617) | [Cutscenes and CCTV overview](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688642333914)
