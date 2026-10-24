---
tags: [room0, gameplay, guests, design]
status: detailed-proposal
updated: 2026-10-24
---

# Ordinary Guests: Scheduling and Production

Proposed implementation and writing reference for the ordinary guest catalogue. This chapter supports the fiction; it does not replace character detail with task counters. No gameplay code, models or place changes are included in this notes delivery.

## Scheduling the hotel

Build the night around available rooms, continuing stays, current guest population and a manageable set of visible activities. Do not begin by independently rolling a request for every NPC.

A booking plan contains arrival window, expected nights, room requirements, individual occupants, shared outings, possible requests and a normal exit plan. Each individual also has a current activity and short-term intention.

For the first prototype, one scheduler may choose a booking's broad plan while individual behaviours handle walking, sitting, waiting and interacting. The design needs consistent outcomes, not a different bespoke controller for every personality.

Use broad phases: arrivals and settling; evening activity; quiet night; morning preparation; departures and turnover. Exact minutes depend on the still-undecided shift length.

No character should be required to complete a six-hour outing inside a ten-minute real-time shift. Represent appropriate in-world time passage consistently, or have them remain offsite across shift boundaries.

Do not compress so aggressively that someone checks in, eats, sleeps and leaves in the same short visible minute. A continuing stay can make the hotel feel occupied without constant new arrivals.

## Population and room capacity

Count current residents before adding arrivals. Guests offsite still occupy their room unless they have checked out. Closed, dirty, broken or unsuitable rooms are unavailable for a new booking.

Illustrative capacity example: a pair and solo continue from the previous night. Adding one solo and one trio creates four occupied bookings and seven residents, not four residents. Only do this if four suitable rooms and the active-guest budget exist.

Proposed visible public-space target for an early test: roughly 3–6 guests when the layout supports it. This is an ambience target, not a promise that six complex NPCs always fit the performance budget.

Other guests may be plausibly resting in their own rooms or offsite. They remain accounted for. Never visibly pop a person out of existence to reduce crowding.

A busy lobby needs brief bursts followed by settling. Prevent permanent queues by postponing arrivals and choosing spare waiting positions.

## Three example nights

### Quiet working night

Continuing booking: Leena, second night. New booking: Martin, one night.

Leena returns with wet boots and quietly uses the lounge. Martin arrives later, handles his receipt and practises tomorrow's pitch. One request for drying towels and one morning call are enough.

Their optional overlap is a short comment about the weather. Leena goes upstairs first; Martin finishes his paperwork. Both leave through normal routines in the morning unless Leena has a confirmed work extension.

Purpose: prove that two distinctive people can create atmosphere without a constant stream of tasks.

### Social weekend

Continuing booking: Gwen and Arthur. New bookings: wedding trio and Ruth.

The anniversary pair prepare for dinner while the trio use the iron in an agreed order. Ruth occupies a different lounge table. The couple go out, the trio leave for the wedding and Ruth enjoys the resulting quiet.

Later returns occur in waves. Beth and Callum may return before Nia, with her later return accounted for by the same ordinary event. A group member being offsite is recorded, not treated as missing.

Purpose: test shared equipment, independent party movement, quiet alternatives and normal reunions.

### Early-start work night

Continuing booking: road crew quartet. New bookings: Felix and Aisha with Tom.

The crew return early and request towels as one group need. Felix wants rest. Aisha and Tom check tomorrow's route, then settle. The lobby can become quiet rather than being repopulated solely to stay busy.

If loud conversation interferes with rest, the crew respond reasonably when reminded. Morning departures are staggered, with the crew regrouping and Felix leaving independently.

Purpose: test four-person occupancy, several early departure plans, noise response and normal group checkout.

## Multi-night memory example

Night one: Denise arrives nervously, borrows a blanket to cushion a box and spends time pricing mugs.

Night two: she returns from the fair. If the previous request was fulfilled, she thanks the appropriate familiar person once. If not, she solved the packing another way and does not replay the original request forever.

Departure: she returns the blanket, counts her boxes and leaves. Her sales result is authored separately from the hotel's service score.

Later visit: a brief line mentions the previous fair. She may bring fewer boxes, different stock or more confidence. Do not reset her to an identical first introduction.

## Minimal continuity record

For each booking, preserve: named roster; party size; room and required bed capacity; arrival and expected departure; who is present or offsite; active service request; loaned items; satisfaction or service memory; extension eligibility; checkout status.

For each person, preserve: appearance; relationship role; current location category; intended next activity; preferred activity slots; relevant dialogue flags; whether they have already left.

For the hotel, preserve: room readiness; available equipment; occupied seats or interaction spots; scheduled arrival windows; outstanding requests; lost property and its ordinary owner.

A brief memory should be about an event that really happened. Do not thank someone for an iron that was never delivered or complain about a call that was never requested.

The booking's lead guest can change for an interaction without changing the roster. A quiet companion may be the person who asks for towels.

## Movement and interaction rules

Walk to valid room and public-space destinations. Give doorways, reception queues and seating approach points enough space. If the route is temporarily blocked, wait or choose a valid alternate path.

Never send ordinary guests into closed renovation rooms, Room 0 or staff-only areas because a route is shorter.

When two people approach a narrow point, one yields. A suitcase needs clearance too. If a route repeatedly fails, recover at a plausible safe point out of view and retain the correct state; do not leave the booking permanently queued.

Reserve a chair, table position or mirror interaction before walking there. If the desired object becomes unavailable, choose another appropriate activity.

Pause ambient chatter during the booking's service conversation. Avoid several guests speaking over the same interaction.

Do not require every personality to have a unique animation rig. Reuse sitting, reading, talking, carrying, phone use, packing and pointing; distinguish characters through timing, prop choice, posture and words.

## Dialogue structure

Give each booking a small set of lines for first arrival, waiting, a request, thanks, a mild disappointment, ordinary chatter, departure and return visit.

Lines should reflect the speaker, not narrate the entire biography. Most conversations are one or two exchanges. Save a longer story for a willing listener.

Track recently used lines. A memorable joke becomes annoying if spoken every thirty seconds. Prefer silence to immediate repetition.

Companion responses should require the companion to be close enough and available. Do not play a reply from someone currently offsite.

Keep personal details gradual. The first visit shows a habit; a second interaction explains something small; a return can acknowledge familiarity. None of this requires every NPC to reveal trauma.

## Guest-facing room details

Use a small set of interchangeable room dressing: suitcase at a designated location, coat on a hook, a book, toiletries, a pair of shoes, papers or a garment bag.

Place belongings according to occupancy and available room space. A four-person room should visibly feel more used without filling every walkway.

Track which items are hotel stock, guest property, consumables and ordinary lost property. Do not clean away someone's open luggage while the booking is active.

After checkout, remove possessions that left with the guests, then generate only the appropriate cleaning traces. Preserve explicitly logged lost property.

## Recommended build stages

**Stage 1: ordinary stay proof.** Build Martin and Leena with one complete arrival-to-departure path, one room requirement each, basic lounge use, one request type each and coherent checkout. Verify that a content guest can complete a stay without requesting anything.

**Stage 2: pair behaviour.** Add Gwen and Arthur, then Aisha and Tom. Support a spokesperson, independent short activities, shared room records, reunion and two-person checkout. Test twin versus double preferences against actual rooms.

**Stage 3: larger bookings.** Add the wedding trio and road crew. Support shared equipment, separate returns, group requests, capacity checking and all members being accounted for.

**Stage 4: richer stays.** Add request cancellation, extensions, carry-over memory, polite alternatives and normal lost property.

**Stage 5: roster expansion.** Add the other fourteen bookings using the same working behaviours, plus a small number of compatibility-based encounters. Choose additions by the variety missing in playtests.

This list recommends what to build, not permission to modify another collaborator's owned area. Before model or Studio work, use the Work Board and production workflow to claim the relevant work.

## Acceptance checks

- A booking of four appears as four distinct named people with a suitable room and sleeping arrangement.
- Every registered member is accounted for during temporary outings, separate returns and checkout.
- A guest can be present for a full night with no service request and still feel alive.
- A fulfilled, cancelled or declined request does not restart immediately or survive a completed checkout.
- A borrowed iron cannot be loaned to two bookings simultaneously.
- A content guest with a fixed onward journey leaves as planned instead of extending automatically.
- A legitimate extension respects room availability and the agreed stay cap.
- A quieter guest still has visible identity and does not become invisible to the design.
- A group member can act independently without losing their booking or being mistaken for a disappearance.
- Guests respect closed areas, other people's belongings and occupied seats.
- The same named guest is never simultaneously instantiated as two different bookings.
- A normal checkout closes the bill correctly and removes departing luggage.
- Simple interruptions and blocked paths recover without duplicating requests, guests or keys.
- Ordinary guest behaviour remains coherent when a separate horror event interrupts hotel service.
- Stored context distinguishes a completed departure from being asleep or offsite.
- The missing-case scripts never accidentally target a booking in this ordinary roster.

## Decisions still requiring testing or approval

Confirm final room capacities and facilities; the intended time compression and shift length; arrival numbers and public-space population; final names and looks; satisfaction weights; extension limits; how long memory survives between visits; the amount of voiced dialogue; which services exist in the first build.

The proposed 40/30/20/10 booking mix, 0–2 requests per booking, three active requests and 1–3 night stays with a four-night cap are starting hypotheses. Tune the whole system together; do not treat every number as independently locked.

The three missing cases are developed in their own notes. This catalogue does not add a fourth disappearance or settle Room 0's secret.


## Navigation

- [[Guests]]: guest system hub
- [[Ordinary Guests - Index]]: all six detailed chapters
