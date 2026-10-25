---
tags: [room0, gameplay, classes, design]
status: detailed-proposal
updated: 2026-10-25
---

# Classes: Starter and Service Roles

Design pack v1, 25 October 2026. All numbers are proposed. See [[Classes - Core and Progression]] for unlocks and [[Classes - Balance and Implementation]] for shared limits.

## C01: Relief Hand

**Pitch:** "They gave you a badge. Nobody gave you a proper induction."

Free. 100 HP, normal regeneration. Best for learning the hotel, solo flexibility and players who enjoy changing jobs. This replaces a perkless Trainee.

### Look and equipment

Borrowed waistcoat, slightly mismatched sleeves, handwritten badge and a pencil behind one ear. The pocket induction book has crossed-out instructions and small practical annotations. Keep the same stylised Ashbourne art standard as every other role; being junior should not mean an unfinished model.

An example non-canon flavour annotation: the printed "Contact the duty supervisor" has been amended to "Try the cupboard beside the stairs." This is environmental flavour, not a claim about a story character.

### Pick It Up

After one valid completion in a routine task category during the current shift, the player's eligible handling actions in that category become 8% faster. Categories initially: housekeeping, maintenance and deliveries. It activates once per category, never stacks per repeated task and resets with the shift.

This is action speed, not an 8% shorter whole delivery journey. It can shorten a towel-folding or tool-return animation; it cannot skip walking, choosing the correct part, knocking, dialogue, stock collection or returning loaned equipment. Completing a category means the server's real objective state is satisfied, not that the player clicked its first interaction.

### The Induction Book

One successful consultation per shift. At a known ordinary task, the player opens the book and learns which routine supply or tool is required and the named normal cupboard where it belongs. It gives a written direction, not a glowing quest marker over a person or a hidden path.

If the cupboard is empty, say so when current stock is legitimately known; otherwise describe the normal location without promising stock. The book never creates a spare part. A cancelled consultation before information is revealed spends nothing; after the useful answer is revealed the charge is spent.

### Another Pair of Hands

On tasks explicitly built for two participants, the Relief Hand can accept a helper position. Proposed additional handling-speed benefit: 5%, subject to the global cap. Assistance requires an actual assigned physical step; standing near another player earns nothing.

If two-person tasks are not implemented, omit this feature from the playable class card rather than simulating it with a hold timer. The core learning passive and book make the class complete without it.

### A shift moment

Martin's reading lamp needs attention. The new player consults the handbook, finds the bulb stock and completes the actual repair sequence. Later, Leena needs a different ordinary lamp repaired; the player recognises the equipment and their handling is slightly more efficient. Learning and usefulness happen together.

### Boundaries and mastery

No combat perk, supernatural answer, global job tracker or free stock. Retain access to every ordinary job. A cosmetic mastery reward could add annotations from tasks actually learned, without revealing story answers.

Acceptance: a task in one category unlocks only that category's 8%; repeating it does not increase the bonus; reconnecting retains learned categories for that shift; a new shift resets them.

## C02: Housekeeper

**Pitch:** "You know what this room looked like before they arrived."

Free. 100 HP, normal regeneration. Best for room turnover, supplies and players who notice small changes.

### Look and equipment

Practical teal workwear, folded cloth, key clip and a caddy with clearly separated clean-supply compartments. Hands look occupied when carrying the caddy. Dirty towels travel to the laundry stream, not back into clean stock.

### A Proper Finish

Eligible housekeeping handling runs 15% faster: folding, fitting clean linen, placing toiletries and bagging routine rubbish where those actions exist. It does not erase mess at a distance or allow turnover before the booking has checked out.

Occupied-room servicing still requires the normal guest request, knock and access rules. A guest leaving for an offsite event is not a checkout.

### The Linen Caddy

Two dedicated housekeeping supply slots in addition to ordinary personal equipment. One slot holds one configured supply unit, such as a towel set or a toiletries refill. Collect each unit from finite stock. Do not quietly convert a slot into infinite towels.

The caddy does not carry quest evidence, players or general bulky luggage. Where the base system supports collecting used linen, return it using the normal separate dirty-linen rules. Do not give free extra return capacity until that lifecycle is defined.

### Final Inspection

After personally completing a legitimate service or checkout-turnover task, the player may record a short checklist for that room: known lamp state, serviced linen, cleared rubbish and other implemented ordinary conditions. Maximum three current room checklists per Housekeeper per shift; recording a fourth asks which to replace.

On a return visit, manually open the checklist beside a current observation. The player sees their prior recorded facts, not a red highlight showing the answer. Only record conditions actually inspected. Do not infer occupants behind doors or detect story events from internal state.

A fresh guest can use a towel or fill a bin. A difference is not automatically paranormal. Checklists retain room, booking context and timestamp so a normal turnover is not mistaken for unexplained activity. An explicit "record new condition" creates a newer version; it does not silently overwrite evidence of what was recorded before.

### A shift moment

Leena comes back wet and asks for dry towels. The Housekeeper prepares a proper service visit rather than starting an unauthorised full room clean. Later, after checkout, they record the finished room. If the room looks different on the next visit, they have something concrete to compare.

### Why keep playing it?

Its sustained supply and turnover efficiency remains valuable even after advanced classes unlock. A Manager can briefly help one job; the Housekeeper is consistently prepared for this department.

Acceptance: empty stock cannot fill a caddy; clean and dirty supplies do not duplicate; a room's checklist survives normal reconnect; guest use is not labelled an anomaly; fourth-checklist replacement is explicit.

## C03: Hall Porter

**Pitch:** "Four guests. Six bags. One working lift."

Early unlock: proposed 3 completed shifts plus 2B coins. 100 HP, normal regeneration. Best for logistics, group arrivals and reducing repeat journeys.

### Look and equipment

Burgundy jacket, worn gloves and a brass luggage token. The trolley has a slightly rattling empty wheel, a luggage rail and readable attachment points. The same shared trolley asset should serve the class and ordinary hotel where appropriate, with approved cosmetic differences rather than duplicate models.

### Know the Corners

Reduce the normal loaded movement penalty by 25% relative to that penalty; do not grant +25% walking speed. Example only: if carrying makes ordinary speed 80% of baseline, the Porter retains 85%. Empty-handed speed remains unchanged.

The benefit applies to eligible luggage and delivery loads. It does not remove collision, squeezing restrictions, knockback or scripted movement limits.

### The Porter's Trolley

Three slots for eligible bulky objects: registered luggage, approved boxes or ordinary delivery containers. Each physical item has one owner/location state; loading transfers it onto the trolley rather than leaving a duplicate in hand.

The trolley turns more slowly than an unladen player and uses accessible routes. Park it before stairs or narrow passages. A reachable service bay allows recovery if it becomes stuck; recovery preserves the load and does not teleport it past a locked route.

Only one trolley per Porter. The player can park it to do other work. Loading guests, blocking doorways deliberately or carrying protected story objects is unsupported. A teammate may unload an item for a legitimate task through the shared handover rules, with credit retained for the transport already done.

### Coming Through

Ring a courtesy bell to ask nearby ordinary NPC guests to make a brief gap where a valid free position exists. Proposed local radius: 10 studs; response lasts at most 3 seconds; 12-second cooldown. Values need testing against actual corridors and navigation.

Guests are not pushed, teleported or made submissive. A seated guest need not stand, a protected dialogue need not interrupt and a predator does not respond. If there is nowhere safe to step, the Porter waits. Repeated ringing cannot generate satisfaction or contribution.

### A shift moment

Denise's pottery and the wedding trio's luggage arrive close together. The Porter loads a sensible route, leaves shared passages open and makes one coordinated trip. Their value is visibly physical: fewer journeys and less abandoned luggage.

### Trade-off and mastery

A loaded trolley is less manoeuvrable. Path planning matters more than sprinting. Cosmetic mastery may repair its upholstery or add a luggage-label collection; it never removes its physical limits.

Acceptance: simultaneous loading cannot duplicate an item; a disconnect parks the trolley safely for that shift; the bell does not affect threats; recovery cannot bypass closed floors.

## C04: Switchboard Operator

**Pitch:** "Every room has a number. Some of them keep calling."

Early unlock: proposed 4 completed shifts plus 3B coins. 100 HP, normal regeneration. Best for communication, request clarity and reducing wrong-supply trips.

### Look and equipment

Rolled sleeves, a coiled headset lead and a message pad with room numbers, caller words and timestamps. Initially the headset belongs to the existing reception phone position; do not quietly add a hotel-wide wireless phone system.

### Taken Seriously

Personally acknowledging a valid ordinary request gives it a one-time allowance of 15% of its original patience window, capped at 20 seconds. The actual deadline is extended, not repeatedly paused. The allowance is attached to the request, not to each Operator.

Acknowledgement is not completion. The caller still needs their item or service. Repeated callbacks, duplicate Operators and promises cannot refresh the same allowance; the global patience budget is defined in the balance chapter.

### The Message Pad

Three pinned active call slips. A slip records the caller's stated identity/room, request wording, call time and known follow-up answer. Unpinning a slip does not delete the underlying shared reception log.

Use "Caller stated: Room 104" where verification has not occurred. Never present a room number from a voice as a trusted booking lookup. Ordinary request details can be shared as text with teammates without requiring voice chat.

### Hold the Line

Two follow-up questions per shift. An eligible call offers one or more authored contextual questions. Asking one spends a charge once the reply is delivered. It improves precision, not the number of tasks the guest generates.

Examples of proposed ordinary dialogue:
- "Is the whole room dark, or just the bedside lamp?" Answer: "Just the lamp. The bathroom light works."
- "How many towels do you need?" Answer from a three-person booking: "Two. Callum brought his own."

The reply must reflect actual request state. Do not roll random answers that make the player bring the wrong item. If no meaningful authored follow-up exists, do not show a charge-spending action.

Story calls use explicitly authored handling. In particular, preserve the established first-night empty-room call. This class may retain its claimed details; it must not turn the call into a verified real guest or change its outcome.

### A shift moment

The Operator clarifies which lamp failed and sends a precise call slip. The Fitter brings a bulb instead of making an unnecessary trip with plumbing tools. The Operator gets legitimate enabling credit when that linked request is resolved.

### Trade-off and mastery

Communication is valuable only when acted on. The class does not perform remote deliveries or stop every waiting penalty. Solo players benefit from fewer wasted trips; co-op players benefit from accurate handovers.

Acceptance: all Operators share the same per-request acknowledgement flag; a slip does not certify a caller; cancelled/unavailable questions do not spend charges; story calls cannot leak hidden identities.

## Miro copy

[Open this chapter in Miro](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688383994253) | [Class overview on the ROOM 0 board](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688383994882)
