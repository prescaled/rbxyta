---
tags: [room0, production, ui, gameplay]
status: decided-direction
updated: 2026-10-26
---

# Task Interfaces: every task feels different

**Decided 2026-10-26 by the user:**
- The first in-game task UIs looked scrappy. Every task must **feel special in its own way, with its own UI and animations**. No shared generic popup, and no progress bars ([[Shift Tasks]]).
- **The reception desk starts with 1 monitor.** More monitors are bought later in the [[Hotel Shop]].
- **Check-in is a custom PC screen.** Some arrivals are anomalies that only look like guests. The player compares the person at the desk with the **photo on file** and the other details, then lets them in or rejects them.

The visual language follows the existing [[README|Ashbourne interface suite]] (Rivin, 2026-10-24) and the [[Art Bible]]:
- brass `#F2C14E`, deep teal `#1F5C63`, burgundy `#8C1C2B`;
- terminal `#102529`, cream paper `#EDE4CF`;
- engraved brass headings, monospaced register text, paper with shadows;
- one brass primary action per screen.

## Shared rules for all task interfaces

- **Diegetic first.** Where possible the UI lives *on the object*. The camera eases to the desk PC, the phone, the fuse box or the clipboard, so the player is looking at the thing itself, not a floating window. A flat screen overlay is only used when the object would be unreadable.
- **Enter and exit.** A short camera tween (0.35 s, ease out) moves into the object, and E or Esc leaves. Character movement is locked only while inside.
- **Each task has its own signature motion and sound.** For example: a stamp thump, a rotary dial click, a bulb squeak, a breaker clunk, a sheet snap.
- **Feedback is physical, not a bar.** The object visibly changes: the key leaves its hook, the lamp lights, the stamp ink appears.
- **No quest markers over guests.** Guests never give quests; guidance is the gold interact outline on objects.
- **The server decides the outcome.** The client only shows it ([[README#Review and handoff]]).
- **Settings respected.** Reduced effects turns off grain and scanlines; there is a larger-text option.

## 1. Check-in terminal (build first)

### The desk
- **One CRT monitor** on the curved desk at the start, with a keyboard, the guest register book, a bell, a stamp pad with APPROVED and REFUSED stamps, and the key wall behind.
- **Upgrade slots** for monitors 2 to 4 are built into the desk but stay empty until bought. Proposed shop items, all permanent hotel upgrades rather than one-shift boosts (team-owned, saved):
  - **Second monitor:** a live CCTV feed at the desk, so you can watch cameras while checking in.
  - **Third monitor:** the arrivals board, showing the queue and expected arrivals.
  - **Fourth monitor:** the room status board, showing ready, occupied and to clean.
- The current 6-monitor CCTV bank is removed from reception. Full CCTV stays in the Security Room ([[CCTV System]]).

### Flow
1. A guest or party walks to the desk queue. The bell dings when they arrive at the counter.
2. The player clicks the monitor. The camera eases into the CRT, the screen powers on (a brief scanline roll), and the **ASHBOURNE FRONT DESK** software opens.
3. **Booking file** (left of the screen). Booking reference, lead guest and every party member by name, party size, nights, bed needs, arrival date, home town and a **photo on file for each person** (a ViewportFrame render of their approved look).
4. **The guest at the desk** (right of the screen, or look up from the monitor). A live ViewportFrame or close camera of the person standing there, which the player can zoom. The guest also **slides an ID card** onto the desk. It can be picked up and turned over: photo, name, date of birth, issue date, signature.
5. **Compare.** The player clicks a field on the file and the matching field on the ID or the person to **mark a discrepancy**. A red pencil circle draws on both, with a scratch sound. Correct marks are recorded; wrong marks cost a little time.
6. **Ask.** Up to 3 short questions from a list ("Name on the booking?", "How many in your party?", "How long are you staying?"). Answers come from written dialogue. Anomalies may answer wrongly, too fast, or repeat the question back.
7. **Decide.**
   - **APPROVE:** the stamp slams the register page with an ink splat. Assign a room on a mini floor plan. Rooms that are too small, occupied or not ready are greyed out. Take the key off the hook (it animates off the wall into the player's hand), and hand it over.
   - **REFUSE:** a burgundy stamp. The guest's reaction plays: an ordinary person leaves upset, while an anomaly stares, glitches or walks off the wrong way.
8. The screen logs the result and powers down to the desk idle screen.

### Ordinary versus anomaly
- **Ordinary bookings** (the [[Ordinary Guests - Index]] roster) always match their file. Their small mundane slips are written in the guest notes: Martin's company spelling on a crumpled note, a misheard room number. These are **not** anomalies. They are fixed by checking, not by refusing.
- **Anomaly arrivals** are separate from the ordinary roster ([[Anomalies]]: Wrong guest; the Faceless Guest from night 4). Possible tells, starting subtle and getting stronger over the run ([[Strange Events#Escalation across a run]]):
  - the face differs from the file photo: eyes too far apart, smile too wide, no pupils, wrong hair colour;
  - the ID issue date or date of birth reads **1998**;
  - the name isn't on the booking, or the booking already shows as checked in;
  - the party count is wrong (one extra person in the group);
  - no reflection in the desk glass, or no shadow;
  - clothes match the file exactly, down to the same creases;
  - an answer repeats the question, or the voice lags.
- **Consequences** (proposed, tune in testing):
  - Approving an anomaly gives it a room key. It later causes an incident, and from night 4 the Faceless Guest follows players.
  - Refusing a real guest upsets them, costs the booking and lowers the inspection grade.
  - Correctly refusing an anomaly gives an inspection bonus and a Journal entry.
- Exact tells per night, rates and rewards are **proposals**. Which anomaly arrivals tie to [[Room 0#The secret]] is still open.

## 2. The other tasks, each with its own feel

| Task | Signature interface and animation |
|---|---|
| **Reception phone** (room calls, wake-up calls) | The camera drops to the brass phone. You lift the receiver and the caller's words type onto a **message pad** in handwriting. Wake-up call: dial the room number on a **rotary dial**, by dragging each digit round to the stop, with clicks and a return whirr. |
| **Taxi and wake-up logs** | A ledger opens flat. Pick the time on brass roller wheels, then sign with a pen stroke animation. |
| **Deliveries** (towels, pillow, iron, vase) | Take the item from a shelf: it lifts into first-person hands, and the shelf count drops. At the door, **knock** with a short rhythm, then the door opens a crack and the guest takes it with a line of thanks. Loans show a **loan tag** that ticks when returned. |
| **Reading lamp or bulb** | Close view of the lamp. Unscrew the old bulb by dragging in a circle (squeak, glass tink), screw in the new one, and it flickers on warm. |
| **Noisy vent** | Close view of the grille. Undo 4 screws in any order with a screwdriver spin, pull out the loose rattling clip, and refit. |
| **Stuck curtain** | Drag the curtain along its rail. It catches at a bent runner, which you pinch straight, then the curtain glides through with a satisfying slide. |
| **Cold radiator** | Turn the bleed key with a mouse twist until the hiss turns to a water spit, then close it before it drips. A small temperature dial needle rises. |
| **Fuse box** (power fault, later) | The panel door swings open. Find the tripped breaker by its colour or the label card, then flip the breakers in order. The lights come back zone by zone with a clunk. |
| **Cleaning after checkout** | In first person: pick up rubbish and drop it in the bag (paper rustle), toss used towels into the laundry bag, then **make the bed**: drag the sheet corners until it snaps flat, and place pillows that click into their spots. Toiletries snap into the bathroom tray slots. |
| **Group bookings** | The register shows a **party card** with each person's name and a present or offsite tag, so you can see who's in and who's out. |
| **CCTV at the desk** (once bought) and in the Security Room | As in the interface suite: CRT knobs to change channel, capture a frame, then a report form with a category and a stamp ([[CCTV System]]). |
| **Inspection at dawn** | The cream inspection sheet slides in. Scores are written in ink line by line, the grade stamp slams D to S, and coins drop into the tray. |

## Build order

1. Check-in terminal and the 1-monitor desk, to final quality. **Review with the user.**
2. Phone and logs, then deliveries.
3. The repair set: bulb, vent, curtain, radiator.
4. Cleaning, then the inspection sheet.
5. Shop monitor upgrades.

## Ownership

The user asked P+C (Claude) on 2026-10-26 to redo the task interfaces. See the [[Work Board]].
- **P+C:** the interfaces, animations and desk model.
- **R+X (Codex):** the shift logic. It keeps the game rules and exposes events or functions for the interfaces to call.
- Codex's existing UI scripts stay until each replacement is ready, then they're removed with Codex's knowledge.
