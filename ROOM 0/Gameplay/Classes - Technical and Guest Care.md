---
tags: [room0, gameplay, classes, design]
status: detailed-proposal
updated: 2026-10-25
---

# Classes: Technical and Guest Care

Design pack v1, 25 October 2026. Detailed proposals, not implemented mechanics. Index: [[Classes]].

## C05: Maintenance Fitter

**Pitch:** "It will hold until morning. Probably."

Middle unlock: proposed 7 completed shifts plus 5B coins. 100 HP, normal regeneration. Best for practical problem-solving and choosing between immediate relief and a lasting repair.

### Look and equipment

Work overalls over a heavy cardigan, an analogue tester, neatly worn tools and a labelled parts tin. Useful details include different bulb/fuse compartments and a clear clipped-on temporary-fix tag. Avoid combat armour or magical repair effects.

### Practised Hands

Eligible repair handling is 15% faster. This can improve tool preparation, fitting and packing away; it cannot skip diagnosis, selecting the correct component, acquiring stock, operating a switch or verifying a repair.

The player still performs the hands-on sequence required by [[First Shift Implementation]]. No hold-to-fill repair bar should be introduced to make a speed statistic easier to implement. If a sequence has no reducible safe handling animation, the perk gives no speed gain on that step.

### The Parts Tin

Dedicated capacity for one approved bulb and one approved fuse, taken from finite hotel stock. Start empty unless the shift's stock system visibly reserves and transfers those parts into it. An equipment entitlement is not a source of infinite consumables.

A teammate can hand over the needed part through the normal item-transfer system. Installed components are consumed or attached according to the repair's existing rules. Picking up and dropping the tin does not refresh its contents.

### Make It Hold

Two temporary fixes per shift. Proposed duration: 90 seconds from successful installation. Before applying one, inspect the fault and confirm it has an authored temporary-fix mode.

Initial candidates:
- An approved lamp fault gets a clip-on battery work light, restoring usable local light while the failed lamp remains visibly tagged.
- A minor drip uses a temporary catch arrangement, reducing the immediate nuisance without fixing the pipe.

Only implement a candidate if its real physical interactions exist. A broken fuse does not become safe because a player bypasses it; use designed replacement/work-light behaviour rather than teaching or animating a dangerous improvised electrical short.

Temporary equipment is a finite per-shift class kit with two use entitlements. Each successful placement spends one. Restocking normal bulbs does not restore temporary-kit charges. Recovering the temporary prop after use does not replenish its charge during that shift.

### State and expiry

A fault moves from reported to inspected, then either temporarily contained or properly repaired. Temporary containment leaves the original job open, records its owner and expiry time, and grants only limited mitigation credit.

The guest sees an honest status such as "Temporary light provided; repair pending." The service does not count as a completed lasting repair for inspection. A final repair before expiry replaces/removes the temporary prop and settles the real objective.

Expiry returns the original unresolved condition; it must not create additional damage, delete a guest's belongings or trigger a fabricated anomaly. One temporary fix per fault instance. Repeated Fitter players cannot chain 90-second extensions on that same fault.

### A shift moment

A light fails while the Porter is guiding a load upstairs. The Fitter supplies temporary lighting, tells the team the repair is still pending and collects the correct bulb. The Porter can continue safely; the Fitter returns to finish the actual job.

Solo, this buys time to collect stock without leaving every other duty unattended. In co-op, it creates a meaningful handover: "It is lit for now. I still need the bulb."

### Why the class is worth more

It can stop an ordinary problem from disrupting several people. The strength is a controlled recovery option, not raw speed on every task. It remains worse than the Porter at bulk transport and worse than the Housekeeper at turnover.

### Limits and acceptance

No repair of scripted supernatural blackouts, story locks, predator events or anything not tagged as an eligible routine fault. No evidence skip. A disconnect leaves the temporary repair and expiry intact.

Verify: invalid targets spend nothing; successful placement spends once; two Fitters cannot double-contain one fault; expiry survives reconnect; proper repair removes the temporary tag; inspection does not count a temporary fix as final completion.

## C06: Guest Liaison

**Pitch:** "Remember the request. Remember who asked."

Middle unlock: proposed 7 completed shifts plus 6B coins. 100 HP, normal regeneration. Best for people who enjoy guest personalities, group coordination and keeping promises.

### Look and equipment

Deep teal waistcoat, discreet lapel pin and a small leather guest book with individual entries. A booking can hold several named people; do not collapse every member's needs into the lead guest.

The book contains ordinary preferences learned during play, not private biographies downloaded at check-in. The authored notes know Leena's interests; the player-facing book does not unless a legitimate conversation reveals them.

### A Familiar Face

After personally completing that guest's first genuine request during the current stay, the Liaison earns a modest familiarity benefit for later ordinary requests from that guest. Proposed effect: a 10% reduction to the normal waiting-penalty rate while this Liaison is on duty.

One familiarity benefit per guest, regardless of multiple Liaison players. It does not retroactively erase penalties, increase the guest's maximum satisfaction or guarantee a positive outcome. For a shared group request, apply to the named beneficiaries rather than every person in the room by default.

Store the fact that the guest recognises helpful staff across a continuing stay, consistent with existing stay memory. Apply the mechanical bonus only while a matching Liaison is present; never let sequential staff departures permanently accumulate it.

### The Guest Book

Records observed preferences, open commitments and service context. Examples: an agreed wake-up time, which named member borrowed an iron, or a request for a quieter ordinary room if room changes exist.

A factual entry identifies its source: guest said, staff observed, or verified booking record. No private dialogue between NPCs is revealed remotely. Teammates can read relevant service entries in a shared handover, while the Liaison's book provides an organised view.

### Let Me Arrange That

Two promises per shift. A promise selects one existing ordinary request, checks that it is feasible to attempt and states a specific deadline. The initial deadline is 90 seconds or the existing remaining deadline, whichever is shorter. This is proposed and must be calibrated to hotel travel time.

A promise does not extend patience by itself and cannot be used after a request is already completed. No promises on unscripted transport guarantees, unavailable services or story outcomes.

On-time completion earns a proposed +3 satisfaction points on a 0-100 design scale, capped at the guest's maximum. If the actual guest system uses another scale, map the value before implementation. This is a small recovery above the normal service reward, not payment for selecting dialogue.

Any teammate may fulfil the promise. The ordinary completion credit goes to the people doing the work; the Liaison can earn bounded coordination credit. Missing the promise loses the extra reward and produces a polite authored acknowledgement where available. It does not create a new punitive satisfaction spiral in this first version.

### Guardrails and the global patience budget

Only one active promise per request. Multiple Liaisons cannot attach separate bonuses. The combined familiarity/acknowledgement effects from all classes may not make the effective ordinary waiting window exceed 125% of its base value. Implementation must calculate and display one consistent deadline/rate state.

If a request is cancelled because the guest checks out or the server invalidates it, close the promise without blaming the player. Refund its charge only if the promise had not been delivered to the guest; do not permit repeated promise/cancel exploits.

### A shift moment

Omar needs an iron, while the wedding trio still has the shared one. The Liaison confirms the return arrangement, promises a realistic delivery and asks the Porter to collect it. Omar receives the same physical iron after its legitimate return; the class cannot conjure another or promise it simultaneously to two rooms.

A second example: Gwen requests a vase. The book records Gwen's request rather than assuming Arthur asked. The service feels attentive because it remembers a person.

### Why the class is worth more

It improves recovery and clarity across a stay, especially when groups have overlapping needs. It cannot replace actual service, command NPC feelings or change an ordinary guest into a mystery case.

Verify: learned facts have legitimate sources; group beneficiaries are explicit; completing someone else's promise works; repeated promises do not stack; the global patience limit survives multiple roles; continuing-stay memory is kept without permanent bonus accumulation.

## Miro copy

[Open this chapter in Miro](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688383994250) | [Class overview on the ROOM 0 board](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688383994882)
