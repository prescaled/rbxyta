---
tags: [room0, gameplay, classes, design]
status: detailed-proposal
updated: 2026-10-25
---

# Classes: Balance and Implementation

Design pack v1, 25 October 2026. Supporting specification for [[Classes]]. This is a design handoff, not evidence that any feature is coded, deployed or tested in Roblox.

## What remains universal

Every player can check in a booking, collect finite supplies, deliver an item, inspect and repair an eligible fault, use the security desk, read accessible records and discover the story through its normal routes.

Class items change convenience, capacity, coordination or limited recovery. None are necessary for the ending, the three missing cases or entry to Room 0. Ordinary guests retain their established identities and behaviours; class mechanics must not turn an ordinary guest into a disappearance case.

Maintain the actual physical work described in [[First Shift Implementation]]. "Faster" refers only to safe handling/animation portions of an action, not a replacement progress bar, hold-E timer or automatic objective completion.

## A precise speed convention

Use handling-speed bonuses, not interchangeable phrases such as "15% less time" and "15% faster." For an eligible baseline animation duration D and combined handling-speed bonus S, proposed adjusted duration is D divided by (1 + S).

Add relevant class, assistance and shop handling bonuses, then cap S at 0.35 for this first version. A Housekeeper's 0.15 plus Quick Hands' proposed 0.25 therefore caps at 0.35 rather than producing 40% or multiplying into a larger bonus. A 2-second eligible animation becomes about 1.48 seconds at the cap; choosing an item and walking to the room are unchanged.

Player-facing wording: "Eligible handling actions 15% faster." Display when a temporary boost is limited by the cap so a shop purchase is not misleading. Retune or replace an overlapping boost if it rarely provides meaningful extra value.

Do not speed up safety-critical collision/interaction validation, subtitles, dialogue choice time or required inspection decisions. Validate the actual task state after each action.

Loaded movement is a separate calculation. The Porter's relative reduction applies to the carrying penalty before any allowed ordinary movement boost, with a movement limit set by the movement system. The handling cap does not secretly govern walking speed.

## Patience and satisfaction

Use a common request/booking state so class effects do not create contradictory clocks:
- Operator acknowledgement is once per request, +15% of base patience up to 20 seconds.
- Liaison familiarity slows later ordinary waiting penalties by 10% for eligible known guests while the relevant class is present.
- Manager reception cover is one team-wide event per shift and affects only eligible new arrivals.
- Effective total waiting allowance from class effects cannot exceed 125% of the ordinary base window for that request or arrival.

Calculate the combined allowance from the original base, not from an already-extended value. Do not apply a full additional extension each time another role interacts. Promises do not extend patience and award their small extra satisfaction only on real on-time completion.

On a group request, store named beneficiaries. Group size does not multiply class bonuses, call charges, promise rewards or contribution. A single iron remains one shared item even if three people use it.

## Capacity, supplies and shared equipment

Class containers add only their explicitly allowed capacity. They cannot be nested inside one another for extra storage. A player owns one equipped class container/trolley entitlement per shift.

Suggested shop compatibility:
- Quick Hands combines through the handling-speed cap.
- Guest Charmer combines through the common patience limit.
- Trolley Upgrade adds its carry option only to ordinary hand-carry rules; it does not turn the Porter trolley into six slots or a Housekeeper caddy into arbitrary storage. Confirm the shop description before implementation.
- Healing items restore health under [[Health]], with no class-based free refills.
- Temporary master-key shop concepts never open story-gated doors.

Taking an item reserves/transfers a real stock unit. Installation or delivery settles it once. Loaned equipment is unavailable to another booking until legitimately returned. Class switching, deaths, disconnects and duplication of a prop cannot manufacture stock.

On departure from a server, put movable role equipment and its contents into a safe staff recovery location reachable within the same allowed area. Do not delete another player's carried item, transfer protected evidence or recover equipment across a locked story boundary.

## Charges and reliable state

Use a stable shift ID and player ID. Persist or recover the minimum shift state necessary to prevent refills through reconnect:
- Selected class, learned Relief Hand categories and consumed ability counts.
- Current known guest familiarity, promises and request-level acknowledgement flags.
- Inventory/trolley ownership and finite supplies.
- Fitter fault containment and absolute expiry.
- Watchman reference slots and monitor next-available time.
- Auditor observed copies and comparison allowance.
- Manager windows, task-target use flags and the shared reception-cover flag.

Validate ownership, distance, target eligibility, currency and task state on the server. Requests need idempotency so network retries cannot charge twice or create duplicates. Rejected activations spend nothing; successfully begun effects spend once. Use server time, not a client's clock, for expiry.

If state cannot be loaded safely, do not claim the class has fresh charges. Use the known server session state or offer a clear safe fallback before starting a new shift. These are requirements for future implementation, not a new persistence system being installed here.

## Cooperation and duplicate classes

Allow duplicates, as the existing class framework does. Duplicate specialities should divide work across different targets rather than multiply one target's reward.

- Two Housekeepers service different rooms.
- Two Porters each have one trolley, but a physical bag occupies only one location.
- Operators share a request's acknowledgement flag.
- Fitters share a fault's one-containment flag.
- Liaisons share a guest/request's active bonuses.
- Watchmen have separate observations and cooldowns without unlimited shared monitor access.
- Auditors may compare the same record but cannot earn credit for submitting the same correction repeatedly.
- Managers share one reception-cover event and a per-task All Hands use flag.

A useful four-player service-heavy example is Housekeeper, Porter, Operator and Fitter. An information-heavy example is Relief Hand, Liaison, Watchman and Auditor. These are playtest compositions, not required matchmaking slots. A group of free classes must still complete an ordinary shift.

## Contribution without farming

The existing inspection distributes coins by contribution plus a team bonus. Do not replace that with "the last interaction gets everything."

Prototype one fixed work-credit budget per resolved task. Reserve up to 30% for verified enabling contributions and leave at least 70% for the physical resolution steps. This is a proposed allocation for contribution weight, not a promise that 30% of every coin payout is paid directly to a support role.

Eligible support examples: transporting the actual item subsequently used; recording a useful answered call; successfully coordinating a fulfilled promise; participating in an active assistance step. Link these to the same task ID. A person doing both support and resolution can earn both portions without increasing the total budget.

Empty pings, opening a notebook, ringing a bell, standing in an aura or copying the same record repeatedly earn no work credit. Temporary mitigation receives a small provisional share of that task's budget, never a second full repair reward; settle actual work even if another player completes it later.

If a task is cancelled for legitimate server/guest reasons, preserve bounded credit for completed physical work already accepted. Do not reward deliberate fault creation, abandoned promises or repeated item handoffs. Class choice must not be a loophole for earning more coins while contributing less.

## Solo and accessibility

Solo play must have all tools needed for basic work. Each class's main signature remains useful alone; optional teammate-only features can be omitted from the solo card. The Manager's explicit 10% solo All Hands variant prevents a paid class from losing its main active ability.

Callers' words and responses are available as readable text. No class requires voice chat or recognising an audio cue alone. Provide clear item names, remaining charges, failed-activation reasons and distinguishable states without relying only on colour.

Use click/tap actions and controller equivalents. Long record views need readable text and scrolling; keep action prompts away from platform controls. Do not show vital instructions for less time merely because the player has a speed perk. Players can decline/mute coordination requests. Do not add markers over guest heads against the current production brief.

## Information and narrative rules

A system records what was legitimately observed, not the author's hidden truth:
- Calls identify what a caller claimed.
- Checklists show inspected conditions.
- Camera stills show a past observed view.
- Carbon copies show the record as it appeared when opened.
- Guest preferences come from permitted dialogue or observation.
- Manager summaries contain known work only.

Comparisons may help a player notice a contradiction, but never output "this is the missing guest," automatically explain Case 3, or expose a hidden room because its internal ID exists.

Keep the first-night empty-room call intact. Any additional class-specific story dialogue needs separate narrative review before becoming canon. Record retention must not remove the baseline route to any required clue.

## Production order and dependencies

This is a suggested order, not a Work Board claim or instruction to start editing Roblox.

1. Establish common class IDs, selection, finite stock, eligible action tags, charge state and contribution events. Confirm the current task implementation can support them.
2. Prototype Relief Hand, Housekeeper and Fitter on already-existing ordinary tasks. Use the book and parts/caddy systems before promising advanced cooperative interactions.
3. Add Porter after trolley navigation/loading works; add Operator after call/request logs and authored follow-up replies exist.
4. Add Liaison after per-guest memory, satisfaction and shared-equipment returns are reliable.
5. Prototype Watchman camera observation and Auditor immutable observed records before selling their unlocks.
6. Add Manager once shared work states, accepting assistance and bounded reception queues are testable.
7. Tune economy and unlock requirements after ordinary shifts produce representative data.

Dependencies that must not be assumed shipped: reliable camera stills, two-participant physical tasks, trolley recovery/navigation, persistent guest memory, per-request patience calculations, immutable record snapshots and support credit.

Reuse shared models and respect the Work Board before any actual modelling or Studio change. This note does not claim a collaborator's folders or assets.

## Acceptance scenarios

Required tests before declaring the class system ready:
1. Finish an ordinary shift solo as each free class using normal tools.
2. Run four free classes together; no required service or story path is locked.
3. Compare each paid role against a free role on representative work; verify a useful benefit and a real limit.
4. Combine class speed, Quick Hands and All Hands; verify the cap and every physical task step.
5. Try duplicate Operators/Liaisons/Managers on one request; verify the patience budget and once-per-target rules.
6. Reconnect after spending an ability, while holding stock and during a temporary repair; no refill, duplication or lost expiry.
7. Contain a fault, let it expire, then repair it; inspection credits the lasting repair only once.
8. Make and fulfil a Liaison promise through another player; both receive appropriate bounded credit.
9. Copy a record, alter the live record through a legitimate event, then compare; the prior observation remains unchanged.
10. Observe a changed camera scene without the Watchman; the normal security desk still allows a valid report.
11. Test a group leaving in waves: all members remain registered until actual checkout.
12. Test invalid activation, simultaneous purchase, insufficient currency and a repeated network request; state stays consistent.
13. Try controller/touch, muted audio and a coordination decline; the role remains playable.
14. Complete the intended story clue path without buying an advanced class.

## What to measure and decide next

Measure task handling time separately from travel, wrong-supply journeys, stock waste, guest outcomes, actual support contribution, observed ability use, repeated-class stacking, deaths and ordinary shift earnings.

A good expensive class should make a difficult shift easier without making every cheaper class feel like a mistake. If a role is rarely chosen, distinguish unclear presentation from weak mechanics before increasing power. Watch for the Auditor having too little ordinary work, the Operator becoming tied to one desk, or the Manager receiving credit for suggestions nobody used.

Open decisions: calibrated coin values; final ability windows; which physical tasks support help; supported temporary faults; camera-still implementation; persistence lifetime for evidence and familiar guests; and final shop stacking descriptions. This pack contains the full proposed direction while keeping those dependencies explicit.

## Miro copy

[Open this chapter in Miro](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688383994257) | [Class overview on the ROOM 0 board](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688383994882)
