---
tags: [room0, gameplay, cinematics, cctv, design]
status: detailed-proposal
updated: 2026-10-27
---

# Cinematics and CCTV: Design Pack

Prepared for Rivin and Prescaled, 27 October 2026.

## Direction and status

Rivin requested a range of scenes including missing-guest glimpses, dark figures appearing and disappearing, and something approaching behind a player before vanishing. CCTV should develop the same atmosphere through detailed interactive ideas.

This pack expands that direction into 12 scene concepts and 12 camera encounters. They are a selectable design library, not a requirement to play all 24 in a shift. Some are paired versions of the same incident, not separate events to stack.

The named scenes, staging, durations, timings, rewards and technical approaches are proposals. No cinematic, model, camera system or Roblox script is implemented by this documentation update.

## Read the pack

- [[Cinematics - Direction and Pacing]]: kinds of scenes, player control, intensity, multiplayer, accessibility and story permissions.
- [[Cinematics - Scene Catalogue]]: 12 detailed scenes with triggers, shot/beat sequences, aftermath and production dependencies.
- [[CCTV - Encounter Catalogue]]: 12 surveillance encounters with observations, player decisions and outcomes.
- [[CCTV - Operation and Evidence]]: camera roles, live versus recorded views, report rules, evidence, classes, upgrades and implementation checks.

Existing references remain [[Cutscenes]], [[CCTV System]], [[Incidents]], [[Strange Events]], [[Anomalies]], [[The Security Archives]], [[Player Experience]] and [[Room 0]].

## Recommended signature experiences

1. **Someone Behind You:** a camera operator sees a figure behind a teammate who sees an empty corridor. Develops an existing canon incident.
2. **The Green Cardigan:** a brief Marnie-like crossing with a recognisable case and silhouette, only after her appearance is legitimately introduced.
3. **The Reflection Arrives First:** a glass reflection contains a figure before anything reaches the corridor.
4. **One Stop Closer:** a camera-only figure advances between observed positions, giving a fair reporting opportunity.
5. **Two Guests, One Empty Landing:** a paired Shaw-like sighting, preserving the two-person case without explaining its mechanism.
6. **The Door the Plan Refuses:** the camera shows an extra door; the physical route and working plan do not. Develops the existing camera/floor-plan contradiction.

These express fast movement, prolonged dread, spatial contradiction and co-op communication without making every event a loud face-in-camera jump scare.

## Two distinct questions

The fiction asks: "What did I just see, and what does it mean?"

The interface answers clearly: "Is this live or recorded? Did I save evidence? Was my report accepted? Do I still have control?"

Uncertainty belongs in the hotel's events, not in whether a button worked or a player's camera is stuck.

## Narrative and cast boundaries

The secret of Room 0 remains undecided. Story-linked scenes are candidates gated by narrative approval, not new explanations. A missing-guest likeness is not proof that the person is dead, escaped, hostile or presently occupying that location.

Daniel Mercer's detailed appearance remains open. Do not invent a canonical face, age or personal object for him through a cinematic. Marnie's and the Shaws' case dates remain open. Do not use an unapproved year on a tape.

Ordinary guests and [[Resident Staff]] remain accounted for. No regular employee is secretly made a predator or disappearance victim by this pack. In particular, Emil's and Ada's silence is not a scare cue.

## First implementation slice

Prototype S02 Service Crossing, S03 Someone Behind You, C01 One Chair Too Many and C02 Behind the New Hire on two useful camera views. S03/C02 share one incident identity. This tests staging, shared state, evidence and reporting before committing to identity-specific sightings, mirror effects or replay systems.

Continue with C07 The Last Few Seconds only if observed-state replay can be implemented faithfully. Build case-specific scenes after approved identity assets and narrative gates exist. The list order is not an instruction to touch another contributor's Roblox area; follow [[Collaboration Workflow]] and [[Work Board]].

## Shared Miro copy

[Open this chapter in Miro](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688642333618) | [Cutscenes and CCTV overview](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688642333914)
