---
tags: [room0, gameplay, classes, design]
status: detailed-proposal
updated: 2026-10-25
---

# Classes: Security Records and Leadership

Design pack v1, 25 October 2026. Advanced-role proposals; index: [[Classes]]. Limits and values require playtests.

## C07: Night Watchman

**Pitch:** "Walk the route. Check it twice."

Advanced unlock: proposed 10 completed shifts plus 9B coins. Proposed 115 HP, normal regeneration. Best for observation, patrol and supporting a teammate through poor visibility.

### Look and equipment

Worn security jacket, substantial torch and a portable video receiver with a small screen. It is hotel equipment, not a weapon or military loadout. The earlier "security radio with camera feeds" becomes a clearly readable receiver; a voice-only radio should not inexplicably display video.

### Steady on Your Feet

115 maximum HP instead of 100. No fear immunity, automatic revival, damage aura or accelerated regeneration. The extra margin makes patrol slightly more forgiving without making a threat harmless.

### Portable Monitor

Select one existing unlocked camera and view it away from the desk for up to 8 seconds per check, followed by a proposed 20-second recharge from the moment the check ends. Movement is limited to a slow walk while the screen is open. Stowing it restores ordinary movement.

A camera that is offline, blocked or outside the player's legitimate access remains unavailable. The receiver does not generate a clean alternate view through static or bypass a story-controlled feed failure.

The main security desk retains sustained viewing, its larger multi-camera controls and the normal report workflow. The portable monitor is for a short check and coordination; final anomaly reports still use the established reporting system. Basic camera pings remain available to all desk users, as in [[CCTV System]].

### Reference Frame

Save up to two stills from a camera legitimately viewed at the desk or on the receiver. Record camera ID, capture time and the observed image. Replacing a still requires an explicit choice.

Open saved/current views side by side. Do not draw a box around the anomaly or calculate a "correct answer" overlay. Ordinary movement can explain a difference. Reports remain subject to ordinary verification and wrong-report consequences.

If true image capture is not feasible in Roblox, the team must prototype an equivalent observed-state rendering and assess its accuracy before advertising saved images. A text summary can be a temporary development aid but is not an honest substitute for the promised visual comparison.

### Stay With Me

Invite one nearby teammate to an escort pairing. The teammate accepts or declines. Proposed invitation distance: 12 studs; pairing ends at 30 studs separation, cancellation or shift end.

The benefit is a mutually visible, non-directional companion indicator when the other player is in line of sight and a simple nearby/separated status. It does not render a silhouette through walls or provide hidden-room coordinates. It grants no damage immunity or movement teleport.

Solo play uses the HP and observation tools; no artificial NPC escort is required to make the class useful.

### A shift moment

The Watchman notices that a chair may have moved, checks a previously saved corridor frame and asks the desk player to investigate. Later they accept an escort pairing with a teammate carrying supplies through a dark passage. Useful teamwork still leaves uncertainty.

### Limits and tests

Portable checks cannot be chained by opening/closing the screen to evade recharge. Two Watchmen cannot share a cooldown, but each keeps their own finite evidence slots. Saved observations may be shared as evidence without granting the recipient unrestricted camera access.

Verify: closed cameras remain closed; saved data predates later changes; no automatic difference detection; escort declines are respected; monitor movement penalty ends on every close/disconnect path; the desk remains useful in playtests.

## C08: Night Auditor

**Pitch:** "The numbers balance. The names don't."

Advanced unlock: proposed 12 completed shifts plus 10B coins. 100 HP, normal regeneration. Best for organised investigation, booking accuracy and players who notice discrepancies.

### Look and equipment

Sleeve garters, reading glasses, a date stamp and a carbon-copy folio. Small paper-handling animations communicate the role: align the pages, stamp the time, file a copy. An unattended calculator printing a line is optional authored ambience, not a class mechanic or confirmed story event.

### Clear Handover

When the Auditor personally finishes a valid check-in, the booking's known named roster and issued room are attached to its ordinary service tickets. Existing information is organised automatically; unknown guests are not identified.

Everyone can read the original reception records and manually make the same association. The passive removes clerical friction, not access to knowledge. Offsite group members remain registered; leaving for an event does not remove them from the roster.

### The Carbon Folio

Retain up to three immutable copies of records actually opened and legitimately readable by the player during the shift. Each copy carries record type, observed fields and capture timestamp. It contains no undiscovered author-only fields.

Copies preserve what the player saw at that moment. Later corrections to the live record do not rewrite them. If a record itself states an unverified claim, its copy retains that status. A forged or strange record is copied as observed, not certified as true.

Ordinary players retain manual access to source records and any baseline journal function. Story-critical past records must remain discoverable through the normal narrative route, not exclusively through a purchased class's folio.

### Reconcile

Two structured comparisons per shift. Select two legitimately accessible records or retained copies and open a side-by-side comparison. The player identifies the mismatching field and submits a proposed clerical correction or evidence note.

The tool does not highlight the answer. Choosing "guest name" or "issued room" is a human judgment, not a supernatural detector. Ordinary verified corrections follow the reception workflow; a suspected story discrepancy becomes a note and cannot overwrite a protected narrative record.

A comparison charge is spent when the paired view is revealed, not every time a field is clicked. Cancelling before reveal spends nothing; repeatedly closing/reopening the same revealed comparison does not refill the allowance. The game should distinguish the active comparison view from a saved result.

### A shift moment

An ordinary iron-return record is attached to the wrong group. The Auditor compares the loan log and the verified booking, proposes the correction and helps the next delivery reach the right guest.

Later, a register contains a name absent from an earlier observed copy. That discrepancy is compelling because the player kept a record. It does not identify the culprit or reveal what "again" and "this time" mean in the author-facing Case 3 notes.

### Why it earns its price

It makes information more reliable and shareable across a busy team, while giving investigation-minded players a recognisable role. Its value must also exist during ordinary nights; if it only matters during rare scripted mysteries, it is not ready for an expensive unlock.

### Limits and tests

No hidden database search, inaccessible room lookup, exclusive evidence or automatic correct-answer marking. Corrupt or unavailable source records should give a clear unavailable state, not invented fallback contents.

Verify: a captured record cannot silently change; the original text is accessible to other roles where intended; incorrect clerical edits cannot erase story evidence; four-copy replacement asks explicitly; duplicate record submissions cannot farm contribution.

## C09: Night Manager

**Pitch:** "You are responsible for everything you cannot personally reach."

Highest unlock: proposed 25 completed shifts plus 16B coins. 100 HP, normal regeneration. Best for prioritisation, recovering a backlog and players who enjoy making the team more effective.

### Look and equipment

A well-kept version of the staff uniform, an engraved duty badge and a compact task board. The identity is responsibility, not a crown, combat armour or glowing rank aura. Its demonstration should show choosing a real task, not commanding other avatars.

### Proper Handover

A concise summary of already-known open work by reception, housekeeping, maintenance and security. Show state, existing assignee where known and urgency the normal request system already exposes.

Do not include hidden anomalies, unseen guests, private NPC plans or story clues nobody has discovered. Other players still retain ordinary shared task information; the Manager gets a better consolidated view.

### The Duty Board

Suggest a priority task with an optional short preset message. A teammate accepts or declines. Only one active priority recommendation per Manager. Rate-limit repeated invitations and provide a mute option.

This is coordination, not assignment authority. It cannot seize a player's current task, teleport them, block their input or penalise them for declining. No quest markers appear over guests.

### All Hands

Two activations per shift. Select one existing routine task designed to accept assistance. Open a 45-second window in which at most two distinct accepting participants receive +15% eligible handling speed on that task. The Manager may be one participant.

The benefit only applies while participants are performing valid task actions in its normal interaction area. A player running elsewhere receives no speed bonus. The window does not auto-complete work or add progress for standing nearby.

Only one All Hands window can affect a task instance across the whole team. For a new target, the Manager must spend a separate activation; cancelling after the window begins spends the charge. If activation fails before beginning, do not spend it.

Solo: apply +10% eligible handling speed to the Manager's own work on one ordinary task for the same 45-second window, twice per shift. It still requires all physical steps. The co-op participant limit should not accidentally disable the solo version.

### Cover the Desk

Once per shift, open a proposed 30-second reception-cover window. New ordinary arrivals join an organised waiting queue instead of immediately suffering the normal unattended-reception penalty. Reception is still unattended and nobody is checked in automatically.

Per booking, additional allowance is capped by the shared maximum of 125% of its original waiting window. Guests already waiting do not have their accumulated dissatisfaction erased. No reservation, key or room allocation is created until a player actually handles check-in.

One shared desk-cover event per team per shift. Multiple Managers see the same used status; they cannot cover reception indefinitely. This is an intentional exception to ordinary per-player charge ownership, because the target is one shared desk.

### A shift moment

A light fault delays a supply run while new arrivals gather. The Manager briefly organises the reception queue and offers All Hands to the Housekeeper on a suitable room-preparation task. They create breathing room; the Housekeeper still does the physical work, and somebody still checks the guests in.

### Why it is the most expensive

The player gains two distinct recovery options plus a broad known-work view. It can help several colleagues in a difficult moment, but has no trolley, temporary repair kit, carbon archive or superior sustained housekeeping speed.

The earlier healing aura, master key and extra HP/regen are not part of this version. If later playtests add another benefit, budget it against these tools rather than stacking everything from the earlier roster.

### Limits and tests

No forced commands, unattended credit, deadline resets, stacking Managers or bypassed story locks. If the Manager disconnects, an already-started window ends at its original expiry; reconnecting cannot restart it.

Verify: a third participant gains no All Hands bonus; ineligible targets do not spend charges; one task cannot receive consecutive All Hands windows from different Managers; Cover the Desk is consumed once team-wide; solo mode remains useful; accepted assistance earns bounded contribution.

## Miro copy

[Open this chapter in Miro](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688383994254) | [Class overview on the ROOM 0 board](https://miro.com/app/board/uXjVEVisZSo=/?moveToWidget=3458764688383994882)
