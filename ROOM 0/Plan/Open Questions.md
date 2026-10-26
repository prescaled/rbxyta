---
tags: [room0, plan, open]
status: open
---

# Open Questions

Ordered by priority. Move answers into the right note and mark them canon.

## 1. The secret of Room 0 (UNDECIDED, top priority)
Everything else depends on this ([[Room 0#The secret]], [[Principles]]).

### Candidate directions for the secret
Brainstorm only. **None of these are canon.** Each is tested against the requirements in [[Room 0]].
- **The ledger**: the hotel keeps a guest book that must always be full. Room 0 holds the guests it "keeps" so the books balance. Explains records changing and management hiding it.
- **The room between floors**: Room 0 exists in the space the building rearranges each night. Explains changing corridors and rooms that are on camera but not on plans.
- **The previous staff**: Room 0 is where the hotel puts people who learn too much, guests and employees alike. Raises the stakes for the players themselves.
- **The founder's arrangement**: the hotel's success depends on a bargain made when it was built, and Room 0 is the price. Gives [[Hotel Management]] a strong motive.

## 2. Story
- Who are the other [[Missing Guests]], and how do they link to [[Daniel Mercer]]?
- What does [[Hotel Management]] know, and why do they hide it?
- Why did Mercer's room number change from 214 to 0?
- Is [[The New Employee]] named, and related to the players?
- Where and when is the hotel? Is the game's present 2026 ([[Timeline]])?

## 3. Gameplay
- Is there real danger or a failure state, or is it pure investigation? ([[Incidents]])
- How long is one shift? (Ignored tasks: guests leave early and the grade drops, see [[Gameplay Loop]].)
- Roles in a team, or everyone does everything? ([[Night Shift Employees]])
- Is progression per player, per group, or server-wide? ([[Progression]])
- What happens after Room 0 is reached?

## 3b. Economy and guests (added 2026-10-24)
- Exact shop opening window (start of shift, or a window in the middle?) ([[Hotel Shop]])
- Robux reroll: check Roblox paid-random-item rules and show odds ([[Hotel Shop]])
- What happens at zero health? ([[Night Shift Employees]])
- Does guest satisfaction carry over between shifts? ([[Guests]])
- "NPC speed" boost: player speed, or NPC speed? ([[Hotel Shop]])
- Who is [[The Inspector]] really?

## 3c. Spawn, classes and health (added 2026-10-24)
- Can any class be bought with Robux, or are they all earned by playing? ([[Classes]])
- Exact unlock costs and stats for each class ([[Classes]])
- Is there a sanity / fear meter as well as health? ([[Health]])
- Knocked-out penalty: how harsh? ([[Health]])
- Can predators be killed for good, or do they come back the next night? ([[Anomalies]])
- Weapons: carried by everyone, or picked up in the hotel? ([[Anomalies]])
- Spawn island concept: is "Ashbourne Staff Quay" with shuttles the right fit? ([[Spawn Island]])

## 4. Content and business
- Visual identity: logo, colours, font, camera look ([[Content Strategy]]).
- Posting cadence and which platform first.
- How to label videos as fiction without killing the mood.
- Monetisation on Roblox (not discussed yet).

## First playable shift v3 — implementation questions (R+X, 2026-10-25)

The owner's v3 brief replaces the earlier timer-based brief. No invented guests, random
request generator, progress bars or hold-E timers. Claim: [[Work Board]].

1. **Marker contract and rooms:** `Production/Hotel Gameplay Markers.md` is not present
   after the latest pull. P+C needs to publish it, including approved room capacities/bed
   arrangements; room readiness; queue, arrival, exit, guest-only navigation and lounge
   activity points; keys; stock and carryable items; repair targets and tools; phone and
   transport records; checkout and turnover objects; and the staff clock. Current live
   scene inspection found seven tagged tasks, Room 101 only, and no R0_StaffSpawn.
2. **Ownership at runtime:** delivery/repair/cleaning must visibly affect objects, while
   HotelV2 is protected. Which P+C-owned runtime API or authored state variants should
   R0_Game use for lamps, towels, beds, traces, doors and keys? Proposed safe boundary:
   read HotelV2, clone explicitly approved portable props into a separate runtime folder,
   and invoke an agreed P+C state adapter; never reposition/delete building objects.
3. **Missing authored content and tuning:** the guest notes supply short example lines,
   but not every request/refusal/checkout line, the empty-room caller's words, an outing
   recommendation, exact wake-up/taxi times, inspection weights/grade thresholds/payouts,
   or finite stock counts. May existing text be shown with neutral functional UI labels,
   with absent dialogue omitted, and numeric balance values explicitly marked proposed?
   Otherwise please provide these values/text before those paths are enabled.
4. **Guest art:** where are the approved individual guest rigs, hair/clothing/prop assets
   and shared walk/sit/read/carry/phone/pack animations for the starting thirteen people?
   The code can retain the exact identities/looks from the notes, but should not substitute
   newly invented appearances or duplicate P+C's assets.
5. **Scope sequencing:** v3 specifies the three guest stages and the seven tasks. Roadmap
   Phase 2 also lists the shop, variable rewards, spawn lobbies, classes and health. Confirm
   these remain separate follow-up work unless already implemented by their owner; the
   current R+X claim covers the first-shift guest/task systems only.
6. **Miro access:** the linked private board requires sign-in in the available browser.
   The complete corresponding vault chapters were read; live Miro content has not been
   verified. Provide access or confirm the pulled vault is sufficient for this build.

### P+C answers (2026-10-26)

- **Q1, marker contract and rooms: answered.** [[Hotel Gameplay Markers]] is pushed and matches the live scene (layout check 0, smoke test all pass). It covers:
  - rooms 101-106 with `Capacity` and `BedType`. 104 is Twin for P02. **105 is a Triple (double + single) for T01. 106 is Family (four singles) for Q01**, so both larger bookings can be enabled;
  - room readiness (`State`) and turnover traces;
  - arrival, exit, three queue points and the guest route to every door;
  - lounge seats and tables, and the drying space;
  - key hooks per room, finite stock with counts, and fixables in every room;
  - the five reception points: computer, register, phone, wake-up log and transport log;
  - the staff clock-in.
- **Q2, ownership at runtime: answered.** The boundary Codex proposed is adopted. R0_Game reads HotelV2 and clones carry props from `ServerStorage.R0_PortableProps` into its own folder. It changes the hotel only through the P+C adapter, `ServerScriptService.R0_HotelAPI.HotelAPI`:
  - `SetFixable` for lamps, bulbs, curtains, the vent rattle and radiators;
  - `SetRoomState` for Ready, InUse, Messy and Turnover traces;
  - `TakeStock` and `ReturnStock` for visible shelf counts;
  - `GetKey` and `ReturnKey`;
  - `SetDoor` for open, close and lock;
  - `ClaimSeat` and `Route`.
  Full table: [[Hotel Gameplay Markers#Runtime API: R0_HotelAPI]]. Doors and fixables were checked in a live Play session.

### Owner answers and latest evidence

- **2026-10-25:** owner approved using written dialogue plus neutral functional UI labels,
  omitting unwritten story dialogue, and marking numeric balance choices as proposed.
  This resolves question 3 for the prototype; it does not turn proposals into canon.
- **2026-10-25:** owner delegated suitable guest rig/animation choices to Codex ("whatever
  you think"). Preserve the named characters' written looks, personalities and routines;
  distinguish temporary rig presentation from finished character art.
- **2026-10-25:** [[Hotel Gameplay Markers]] appeared locally while P+C continued building.
  It defines clock-in, reception, stock, fixables, seats, drying and rooms 101–104.
  Those rooms all have capacity two; 104 is Twin. No approved triple/four-person room
  exists yet, so T01/Q01 must be deferred rather than overfilling a room.
- Remaining integration decisions: an agreed runtime state adapter for protected props,
  safe guest routes/door access, approved sleeping arrangements for larger bookings,
  and room turnover targets outside Room 101. The live marker set must be rechecked
  after P+C's rebuild; the note alone is not proof those objects are in the scene.
- The first timer-based draft was never installed in Studio. It has been moved outside
  the asset repo into a local superseded-draft folder. Only v3 sources will be delivered.
- P+C's existing Play session has not been interrupted. Live Miro access remains
  unavailable; the owner approved continuing from the pulled vault with written lines
  and proposed tuning. See [[First Shift Implementation]] for evidence and status.
