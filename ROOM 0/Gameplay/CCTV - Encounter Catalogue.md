---
tags: [room0, gameplay, cinematics, cctv, design]
status: detailed-proposal
updated: 2026-10-27
---

# CCTV: Encounter Catalogue

Twelve proposed camera encounters, 27 October 2026. Index: [[Cinematics and CCTV - Index]]. Shared evidence rules: [[CCTV - Operation and Evidence]].

Tags have specific meaning:
- **Actionable anomaly:** persists long enough to inspect and report; uses a validated incident ticket.
- **Transient sighting:** atmospheric or optional observation; no failure penalty for missing it.
- **Story discrepancy:** discovery requiring narrative approval; filing evidence does not magically resolve the mystery.
- **Ordinary explanation:** genuine everyday activity, with no anomaly reward.

## C01: One Chair Too Many

**Type:** actionable anomaly. Suggested first camera tutorial; 45-60 second readable window as a starting value.

**Baseline:** the lounge camera covers a distinctive group of chairs and a clear doorway. Players can see the ordinary arrangement during service.

**Change:** an extra copy of one chair appears in an otherwise clear part of the room, after a natural camera change or occlusion. It has the same small visible wear detail as its original. It must not be a chair a real guest or staff member legitimately moved.

**Player action:** inspect, save a frame and report Object discrepancy. The report does not demand an exact pixel click on the chair.

**Outcome:** a verified report clears the duplicated instance at a natural transition and rewards the ticket once. If missed, this introductory variant quietly expires without becoming a predator.

**Why it works:** teaches comparison without teaching players to report every moving person.

## C02: Behind the New Hire

**Type:** transient camera-only sighting. Paired incident with S03, not an additional independent spawn.

**Baseline:** the operator sees a teammate in a corridor.

**Change:** a dark figure appears several steps behind them and approaches once. The physical player sees nothing when turning. The event lasts about 8-12 seconds, with a target full-figure opportunity of at least 3 seconds for a watcher already on that feed.

**Player action:** warn the teammate and optionally capture a frame. After the sighting, the operator can submit that captured observation as an incident log. It is not a disappearing actionable ticket with a late penalty.

**Outcome:** captured evidence remains accessible; no reward for repeatedly triggering the same scene, and no automatic damage or chase.

**Solo version:** the security-entry feed shows a presence just outside the player's room. It does not fabricate a live image of the player elsewhere.

## C03: One Stop Closer

**Type:** actionable camera-only anomaly. Nights 2+.

**Baseline:** an empty distant end of a corridor.

**Change:** a stationary figure occupies a distant marked position. On a later valid feed observation, it stands at a nearer authored position. Use three positions with clear spacing. A minimum phase dwell prevents rapid camera cycling from accelerating it.

**Player action:** recognise the approach, capture a frame and report Unidentified presence before the last phase expires. Proposed total observation opportunity: 60-90 seconds, not three arbitrary clicks.

**Outcome:** a correct report ends this anomaly. A missed incident can raise the encounter scheduler's tension state, but this first version does not cause an unavoidable attack at the desk.

**Later hostile variant:** only after separate predator design, with an explicit warning and escape window. Do not silently turn the harmless version into instant damage.

**Implementation condition:** all viewers of the same feed see the same phase. It does not move once per viewer independently.

## C04: The Door the Plan Refuses

**Type:** story discrepancy. Develops the canon camera/floor-plan contradiction.

**Baseline:** a known corridor and an accessible working floor plan.

**Change:** the feed contains an additional door at a specific wall position. The plan contains no opening there. A colleague at the physical location sees ordinary wall panelling.

**Player action:** preserve the camera observation, compare the plan and optionally inspect the physical location. Solo players can save a frame before walking over; the discrepancy remains discoverable long enough to do both.

**Outcome:** an evidence entry records three bounded observations. A report says "Recorded for investigation," not "False report" merely because the field view differs.

**Limits:** no new room number is assigned by this concept. Do not automatically label the door Room 0, open it or decide where it leads.

**Dependencies:** approved corridor geometry and narrative permission. The false door cannot become an accidental walk-through route.

## C05: The Reflection Has Company

**Type:** actionable camera-only anomaly; technically deferred if reflection staging is unreliable.

**Baseline:** a fixed camera includes both a small mirrored surface and the corresponding visible part of the lounge.

**Change:** a seated reflected figure appears, while the matching chair in the direct view is empty. It stays still long enough to compare both areas.

**Player action:** save a readable frame and report Reflection discrepancy. Do not require identifying the figure's face.

**Outcome:** a verified report clears this incident once. The camera remains functional; the player is not punished with a forced blackout for being correct.

**Variation:** the real chair is occupied by an ordinary guest, but the reflection contains a different anonymous silhouette. Keep this variant later and never alter that guest's booking identity.

**Dependencies:** a clear designed reflection, not a cheap global mirror filter that makes ordinary movement inconsistent.

## C06: The Clerk Has Already Left

**Type:** story discrepancy involving an anonymous staff-like likeness, not an accusation against a named regular.

**Baseline:** a real employee has visibly completed an ordinary handover and left their desk. Their departure is recorded normally.

**Change:** a camera shows a distant staff-uniform silhouette continuing a small desk action. The live physical desk is empty. The silhouette's face is not identifiable.

**Player action:** compare the observed departure time with the feed's live status; capture the discrepancy. If the feed is genuinely recorded, this is an ordinary explanation instead and should not become a reportable anomaly.

**Outcome:** archive a qualified observation: "Staff-like figure visible at empty desk." Do not mark Evelyn, Ada or another employee as secretly present, dead or missing.

**Dependencies:** accurate live/recorded labels, departure state and narrative approval for this ambiguous recurrence.

## C07: The Last Few Seconds

**Type:** transient sighting supported by a proposed short replay buffer.

**Baseline:** an operator changes to a corridor feed just after a brief crossing.

**Change:** a small local recording indicator shows that the feed has recent buffered material, without announcing "anomaly detected." Rewinding about 10 seconds reveals a single anonymous silhouette passing a doorway.

**Player action:** switch deliberately from LIVE to RECORDED, review, save an observed frame and return to live. A late-arriving teammate can understand what the first observer saw.

**Outcome:** optional archived sighting. No camera rewind should create a new report reward each time the figure passes through the recording.

**Dependencies:** faithful recorded-state playback. This must not be implemented as live actors plus a fake older timestamp. If replay is unavailable, omit this encounter or stage a longer live crossing; never imply a working recording system.

## C08: Between Camera Two and Three

**Type:** story discrepancy; anonymous actor unless a case-specific version is separately approved.

**Baseline:** two overlapping cameras cover a continuous, physically understandable route.

**Change:** the figure leaves the first view towards the second. The second view stays empty even though the route has no intervening exit. The event does not relabel feeds or secretly switch their time modes.

**Player action:** compare feed IDs, timestamps and the observed route. Co-op players can watch different screens; solo players use a valid saved observation or a sufficiently slow authored sequence.

**Outcome:** archive what was actually observed. Seeing only one camera means partial evidence, not a complete confirmed contradiction.

**Limits:** do not require an upgrade or the Night Watchman class for an essential clue. If the baseline single-view setup cannot observe both, reserve this for optional content until a fair alternate record exists.

## C09: The Empty Lift Holds Its Weight

**Type:** actionable anomaly only if the lift has a trustworthy weight/occupancy indicator; otherwise defer.

**Baseline:** the camera shows the open lift car, with the full floor visible and an established ordinary occupancy indicator.

**Change:** the indicator registers an occupied car while the visible lift is empty. A shallow floor shadow may move, but no real guest or player is hidden outside the camera's coverage.

**Player action:** compare the two visible facts and report Equipment discrepancy. A normal damaged sensor belongs to maintenance and is an ordinary explanation, not an anomaly ticket.

**Outcome:** report verification is based on the authored incident, not on a player's guess about invisible bodies. Clear the anomaly or refer a real fault to maintenance; communicate the difference honestly.

**Dependencies:** functioning lift states, real visibility coverage and a previously introduced indicator. Do not add an unexplained "ghost weight meter" just to support the scare.

## C10: The Window in the Closed Wing

**Type:** transient sighting or story discrepancy, selected before the event begins.

**Baseline:** a camera legitimately covers a window or glazed doorway looking towards an inaccessible wing.

**Change:** a distant figure appears, disappears behind a curtain and returns in an adjacent pane without a visible crossing. Use a small number of slow positions; no flashing montage.

**Player action:** record the view from authorised space. The encounter does not ask the player to trespass through a currently locked floor.

**Outcome:** optional observation. If used as a required story discrepancy later, a permitted record or later revisit must carry the same information.

**Identity:** anonymous by default. A missing-guest variant requires approved likeness and case progression. No promise that the figure is a prisoner waiting to be rescued.

## C11: The Helpful Colleague

**Type:** ordinary explanation.

**Baseline:** a player remembers a lounge chair, trolley or basket in one location.

**Change:** it is elsewhere on the next camera check. In reality, Nell, Sadie, Benny or Emil legitimately moved the object during a visible bounded duty.

**Player action:** inspect the live scene, ask the employee a normal work question or consult a relevant accessible work entry. A valid recording may show the move if recording actually exists.

**Outcome:** no anomaly ticket. A reasonable mistaken report returns "No anomaly verified; ordinary service activity" where the system can verify that fact. No humiliating message and no substantial coin loss.

**Why it matters:** employees must be allowed to do real work. The player should distinguish an unexplained duplication from ordinary human movement.

## C12: Two at the Landing

**Type:** case-gated transient sighting; paired with S05 only if designed as one shared event.

**Baseline:** a landing camera covers an approved column and the route beyond.

**Change:** two figures resembling Vincent and Audrey stand together, take hands and pass behind the column. Neither appears at the next visible opening.

**Player action:** preserve a frame if watching. The interaction is optional and can support a later recollection, without demanding a timed identification quiz.

**Outcome:** record "Two figures" until the player has legitimately learned the pair's identities. No automatic author-only explanation of repeated stays.

**Limits:** never use the ordinary wedding trio as substitute actors; never leave one of the two figures behind; never change the actual guest ledger. The scene does not prove the pair escaped or that one abandoned the other in the current appearance.

## Variety and reuse

C02/S03, C08/S11 and C12/S05 can be paired presentations of the same incident. Select one event ID and compatible viewer layers rather than counting them as two random scares.

Start with C01 and C02. Add C03 once timing and report validation work. C04 and C08 need careful story/geometry approval. C05 and C07 need extra rendering/replay work. C09 should be cut if its physical indicator adds complexity without improving the actual hotel.

## Shared Miro copy

[Open this chapter in Miro](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688642333613) | [Cutscenes and CCTV overview](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688642333914)
