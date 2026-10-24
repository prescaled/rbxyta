---
tags: [room0, gameplay, economy, design]
status: decided-core
---

# Variable Rewards

**Decided 2026-10-24:** use a **variable-ratio schedule**: players get rewarded **at random**, for **certain actions**, so they never know which one will pay out.

## How it works
- Pick a set of **reward actions**. Each time a player does one, there is a small chance of a bonus.
- Average out at about **one bonus every N actions** (for example N = 6), but random each time.
- Add a **pity counter**: after, say, 12 actions with nothing, the next one is guaranteed. This stops bad luck streaks.

## Reward actions (proposal)
| Action | Possible reward |
|---|---|
| Finish a guest request | Guest leaves a **tip** (coins) |
| Clean a room | Find a **lost item** (coins or a small boost) |
| Fix a maintenance fault | **Spare parts**: a free single-use boost |
| Answer a room call | A **thank-you note** with coins |
| Check a camera | Rare: spot a **hidden clue** (story discovery, not coins) |

## Rules
- The random rewards are **coins, small boosts or clues only**. They never cost Robux, and Robux never buys better odds. (Important with a young Roblox audience.)
- A reward has a clear sound and pop-up, so it feels good every time.
- Some random finds should be **story clues** that link to the videos ([[Player Experience#The video-to-game bridge]]).
