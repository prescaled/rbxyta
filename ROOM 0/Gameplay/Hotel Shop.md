---
tags: [room0, gameplay, economy, monetisation]
status: decided-core
---

# Hotel Shop

**Decided 2026-10-24:** a shop **inside the hotel** where players spend coins (from the [[End of Shift Inspection]] and [[Variable Rewards]]) on **small boosts**. It has a **Robux reroll** to refresh its stock, and it is **only open for part of the shift**.

## How it works
- **Location**: a small staff shop or vending room in the hotel (could be a staff canteen counter). See [[Blender Model List#Shop]].
- **Opening window**: open for one part of each shift, for example the first quarter, or a short window in the middle of the night. Then it shuts for the rest of the shift. Players must decide when to leave their tasks to go shopping.
- **Stock**: 3 to 5 random items from the item pool each shift.
- **Reroll**: pay Robux to replace the current stock with a new random set. (Optionally one free reroll per day to show it off.)

## Item pool (proposal)
| Item | Effect | Duration |
|---|---|---|
| Quick Hands | Tasks finish 25% faster | One shift |
| Comfy Shoes | Walk speed +15% | One shift |
| Energy Drink | Short sprint burst | 30 seconds, single use |
| First Aid Kit | Recover [[Health]] | Single use |
| Steady Nerves | Slower health / sanity loss from scary events | One shift |
| Master Key (temp) | Skip one locked-door step | Single use |
| Coffee Thermos | Stamina refills faster | One shift |
| Lucky Charm | Slightly higher chance of a random reward ([[Variable Rewards]]) | One shift |
| Guest Charmer | Guest satisfaction drops slower | One shift |
| Trolley Upgrade | Carry two delivery items at once | One shift |

"NPC speed" from the brief is read as **player movement speed**. If it meant making NPC guests or staff faster or slower, add it as its own item.

## Front desk upgrades (user, 2026-10-26)
The reception desk starts with **one monitor**. Extra desk monitors are bought here as **permanent hotel upgrades** (an exception to the one-shift rule): a CCTV feed, an arrivals board and a room status board. See [[Task Interfaces#The desk]]. Prices are undecided.

## Design rules
- Boosts are **small**. They help, but never replace playing well.
- No boost should skip a story clue or unlock [[Room 0]].
- Items last one shift at most, so coins keep mattering.

## Roblox rules to check before launch
- A paid reroll gives a random result, so it likely counts as a **paid random item** under Roblox policy. That usually means **showing the odds** of what can appear and following age rules. Check the current Roblox rules before shipping. ([[Open Questions]])
- Health implies there is **some danger** in the hotel. That answers part of the "real danger?" question in [[Open Questions]]. Decide what happens at zero health.
