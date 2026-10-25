---
tags: [room0, gameplay, classes, design]
status: detailed-proposal
updated: 2026-10-25
---

# Classes: Core and Progression

Design pack v1, 25 October 2026. Current detailed proposal; linked index: [[Classes]].

## The class fantasy

Players are employees of an ageing hotel. Class identity should come from equipment, knowledge, movement and responsibility that belong there. A trolley bell, a carbon copy or a patched lamp can become memorable because it changes what the player does.

Each class needs:
- A readable job and silhouette.
- A small, dependable personal advantage.
- A signature item that changes a normal decision or journey.
- A limit that leaves room for teammates.
- An ordinary success moment before its tool becomes useful in an unsettling situation.

Expensive classes are stronger through reach, flexibility and recovery tools. They should improve the team's chance of handling a difficult shift, while a specialist still wins at sustained work in their own department. Do not make the final purchase the fastest cleaner, fastest runner, best repairer and best observer simultaneously.

## Shared baseline

- One selected class per player per shift. Choose before boarding the shuttle; changing a mannequin preview does not equip it.
- Ordinary flashlight, basic interactions, reception, hotel records, security desk and appropriate communal tools remain available to every role.
- Proposed baseline: 100 HP and the normal regeneration rules in [[Health]]. Only the Night Watchman starts at a proposed 115 HP in this pack. Other roles do not inherit the old extra HP or regen multipliers.
- Skills do not unlock restricted story rooms, identify the true culprit, mark the correct anomaly or skip evidence.
- Classes are permanent earned unlocks. Class equipment is a reusable role entitlement; bulbs, fuses, towels and loaned irons remain physical hotel stock with their normal lifecycle.
- Charges reset once per new shift identity. Dying, reviving, changing devices or reconnecting to that same shift does not refill them.
- A player can leave or play solo without a required role preventing completion.

## Unlock bands and initial requirements

All values below are proposed. Completed shifts count only after a valid settled shift result with meaningful participation; raw time spent connected does not qualify.

- **Relief Hand:** free from the first shift.
- **Housekeeper:** free from the first shift.
- **Hall Porter:** 3 completed shifts, then an early-price coin purchase.
- **Switchboard Operator:** 4 completed shifts, then an early-price coin purchase.
- **Maintenance Fitter:** 7 completed shifts, then a middle-price coin purchase.
- **Guest Liaison:** 7 completed shifts, then a middle-price coin purchase.
- **Night Watchman:** 10 completed shifts, then an advanced-price coin purchase.
- **Night Auditor:** 12 completed shifts, then an advanced-price coin purchase.
- **Night Manager:** 25 completed shifts, then the highest-price coin purchase.

These are independent purchases, not a chain requiring every earlier class. Unlocking the Manager does not grant all other classes. Failed shifts with a valid result and genuine participation may count; do not demand only perfect grades. Repeated deliberately abandoned sessions do not count.

## Price calibration instead of invented fixed coin prices

The current economy does not yet establish a reliable normal coin payout. Do not silently reuse UI demonstration balances or assume the previous 500/1,000/2,500 proposals are final.

Measure **B**, the median coins a normally participating player retains from one representative completed shift after buying one ordinary shop boost. Use a mixed sample of solo and co-op players without class purchase spending. If B is zero or negative, fix payout/boost affordability before pricing class progression.

Suggested initial savings costs:
- Porter: 2B.
- Operator: 3B.
- Fitter: 5B.
- Liaison: 6B.
- Watchman: 9B.
- Auditor: 10B.
- Manager: 16B.

Illustration only: if B were 120 coins, these would be 240, 360, 600, 720, 1,080, 1,200 and 1,920 coins. These examples are not final prices. Savings may accumulate before the shift requirement is reached; the two requirements apply together rather than adding two sequential grinds. Cost should be shown as a plain fixed coin amount after calibration, never as B in the game UI.

Higher prices must buy observable value. Test more successful recoveries, better coordination and less wasted travel, not only a longer tooltip. If an advanced role rarely helps, improve its tool before raising its numbers.

## Staff Locker Hall presentation

Keep the established walkable mannequin displays and uniform mirror. Each pedestal gets the same information order:
1. Role name and one-sentence job fantasy.
2. Signature equipment and a short demonstration.
3. Passive benefit.
4. Limited ability, charges and reset period.
5. Important limit.
6. Exact unlock cost and completed-shift progress.
7. Separate try-on, purchase and equip actions.

Suggested demonstrations: Housekeeper packs the caddy; Porter rings the bell; Operator tears a call slip; Fitter clips in a temporary work light; Liaison writes a promise time; Watchman compares a saved frame; Auditor stamps a copy; Manager moves a task ticket. These are animation briefs, not newly created model assets.

Try-on never spends currency. Buying needs one explicit confirmation containing the price and remaining balance. Prevent duplicate charges and check eligibility on the server. A successful purchase can offer equip, but never silently change a class after the shift has started. If the hotel system cannot safely equip the chosen class, explain it before boarding and offer a free class.

## Mastery and personal attachment

Start with cosmetic mastery: embroidered name badge, repaired trolley covering, additional handbook annotations, a neat stamp case or a veteran uniform. Mastery goals should reward meaningful tasks and support, not repetitive button presses.

Example milestones: complete successful group deliveries, make accurate call handovers, finish proper repairs after temporary fixes, honour guest promises. Do not count deliberately creating mess/faults or repeatedly registering the same event.

Stat upgrades within classes are deferred. Combining class unlocks, mastery stats and temporary shop boosts immediately would make balance hard to read. A new player should understand what the purchased class actually gives them.

## Names and migration from the earlier roster

- Trainee becomes **Relief Hand**, gaining a useful learning identity.
- Housekeeper remains **Housekeeper**; proposed 25% cleaning speed becomes a more modest 15% handling-speed bonus plus the caddy/checklist.
- Porter becomes **Hall Porter**; general +10% walking speed becomes reduced loaded slowdown and a physical trolley.
- Maintenance Tech becomes **Maintenance Fitter**; old 110 HP/30% repair speed are not carried forward.
- Concierge becomes **Guest Liaison**; global satisfaction slowing and extra regen are replaced by earned guest familiarity and specific promises.
- Night Security becomes **Night Watchman**; proposed 125 HP becomes 115 and portable feed access is bounded.
- Night Manager keeps its name; old 120 HP, +50% regen, healing aura and master key are replaced by deliberate work-coordination tools.
- Switchboard Operator and Night Auditor are new roles.

This mapping is for documentation and future compatibility. No assumption is made that the earlier classes were shipped. If players already own an old class when implemented, preserve their ownership through the mapped role, explain changed perks and decide any refund policy before release.

## Decisions still requiring playtests

Final costs, completed-shift gates, duration tuning, handling-speed caps, portable monitor duty cycle, patience budget and support contribution allocation. Robux class sales remain undecided; this pack only specifies earned coin purchases. Story progress and class ownership remain separate systems.

## Miro copy

[Open this chapter in Miro](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688383994252) | [Class overview on the ROOM 0 board](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688383994882)
