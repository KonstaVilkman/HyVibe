# Fame System

**Purpose:** Social status that rewards active, social players.
**Status:** Concept Phase
**Last Updated:** January 2026

---

## Core Concept

Fame measures how **known** and **active** a player is. It's not a currency — it's a reputation score that unlocks benefits and shows status.

**Key Principles:**
- Fame must be earned continuously (decay exists)
- Active players rank high, casual players stay middle
- No hard cap, but diminishing display returns
- Leaderboard rank matters more than raw number
- Decay is gentle, not punishing

---

## Why Players Want Fame

| Incentive | How Fame Delivers It |
|-----------|---------------------|
| **Status** | Visible rank/title that others see |
| **Passive Income** | Higher fame = better hosting bonuses |
| **Exclusivity** | Fame-locked cosmetics and areas |
| **Recognition** | Leaderboard presence, being "known" |
| **Lootboxes** | Rare Lootbox reward on tier promotion |
| **Aspiration** | Seeing high-fame players creates goals |

---

## Earning Fame

| Action | Fame Gained | Notes |
|--------|-------------|-------|
| Daily login | +10 | Shows up every day |
| **Emote sync (2 players)** | +1 | Click someone's emote to join |
| **Emote sync (3-5 players)** | +2 | Group emotes |
| **Emote sync (6-10 players)** | +3 | Dance floor moments |
| **Emote sync (11+ players)** | +5 | Flash mob energy |
| Someone visits your apartment | +2 | Encourages good apartments |
| Someone likes your apartment | +5 | Quality over quantity |
| Hosting party (per guest per 5 min) | +1-3 | Core fame engine (scales with party tier, requires Crystals) |
| Guest plays minigame at your party | +2 | Encourages fun parties |
| Winning public minigame | +5 | Skill reward |
| Job task completed | +1 | Standard jobs |
| Entertainment job task | +2-3 | Social jobs give more |
| Achievement unlocked | +10-50 | Milestone spikes |
| Event participation | +10-30 | Engagement reward |

*Emote sync Fame has a cooldown - only triggers once per emote session to prevent spam.*

**Design Note:** Fame sources are varied so players can earn through different playstyles.

---

## Fame Decay — Gentle Threshold Model

### The Problem to Solve
- Active players should rank high
- Casual players should stay in middle tiers (not punished)
- Inactive players should gradually fall
- Nobody should "retire" at the top permanently

### How It Works

**Daily Threshold:** Minimum fame to earn that day to avoid decay. Thresholds are LOW to be friendly to casual players.

| Current Fame | Rank Tier | Daily Threshold | Easy to Hit? |
|--------------|-----------|-----------------|--------------|
| 0 - 999 | Newcomer | 0 (Protected) | Always safe |
| 1,000 - 2,999 | Local | 10 | Login = done |
| 3,000 - 5,999 | Known | 15 | Login + 1 activity |
| 6,000 - 11,999 | Popular | 20 | Login + few tasks |
| 12,000 - 24,999 | Celebrity | 30 | ~30 min playtime |
| 25,000 - 49,999 | Star | 40 | ~45 min playtime |
| 50,000+ | Icon | 50 (Capped) | ~1 hour playtime |

**Key Change:** Daily login gives +10 Fame, so most thresholds are easily met just by logging in and doing minimal activity.

---

### Decay Rules

| Scenario | What Happens |
|----------|--------------|
| **Hit threshold** | No decay, fame grows |
| **Miss threshold (Day 1-2)** | Grace period, no decay |
| **Miss threshold (Day 3)** | -3% fame |
| **Miss threshold (Day 4+)** | -5% fame per day |
| **Return and hit threshold** | Decay stops immediately |

### Why Gentler Decay?

**Problem with harsh decay:** Players feel punished for real life (vacation, busy week, etc.)

**Solution:** 2-day grace period + lower percentages. Players who take a break come back without devastating losses.

---

### Decay Math Examples

**Example A: Celebrity goes on vacation (1 week)**

```
Day 0: 15,000 Fame (Celebrity, threshold 30)
Day 1: Earns 0 fame — MISS (grace)
Day 2: Earns 0 fame — MISS (grace)
Day 3: Earns 0 fame — MISS (-3%) = 14,550
Day 4: Earns 0 fame — MISS (-5%) = 13,823
Day 5: Earns 0 fame — MISS (-5%) = 13,132
Day 6: Earns 0 fame — MISS (-5%) = 12,475
Day 7: Returns, earns 40 fame — HIT, stops at 12,475

Lost ~17% over a week. Recoverable in a few days of active play.
```

**Example B: Casual player (plays every other day)**

```
Day 0: 4,000 Fame (Known, threshold 15)
Day 1: Earns 25 fame — HIT = 4,025
Day 2: Earns 0 fame — MISS (grace)
Day 3: Earns 30 fame — HIT = 4,055
Day 4: Earns 0 fame — MISS (grace)
Day 5: Earns 20 fame — HIT = 4,075

Casual player maintains and slowly grows. System doesn't punish them.
```

**Example C: Active grinder**

```
Day 0: 8,000 Fame (Popular, threshold 20)
Day 1: Earns 80 fame — HIT = 8,080
Day 2: Earns 100 fame — HIT = 8,180
Day 3: Earns 90 fame — HIT = 8,270
...consistently grows, climbs leaderboard
```

---

## Fame Display — Rank Over Number

### Why Hide Raw Numbers?

- Prevents "number go big" obsession
- Focuses on relative position
- Makes leaderboard rank meaningful
- Reduces intimidation for new players

### Display Format

Instead of: `Fame: 47,832`

Show: `** Star #12`

| Component | Meaning |
|-----------|---------|
| ** | Tier icon |
| Star | Tier name |
| #12 | Leaderboard position within tier (or global) |

### Tier Titles

| Fame Range | Title | Icon |
|------------|-------|------|
| 0 - 999 | Newcomer | . |
| 1,000 - 2,999 | Local | o |
| 3,000 - 5,999 | Known | * |
| 6,000 - 11,999 | Popular | + |
| 12,000 - 24,999 | Celebrity | # |
| 25,000 - 49,999 | Star | ** |
| 50,000 - 99,999 | Icon | *** |
| 100,000+ | Legend | @ |

### Tier Promotion Rewards

**Every time you reach a new tier:**

| New Tier | Reward |
|----------|--------|
| Local | 1 Common Lootbox |
| Known | 1 Rare Lootbox + 25 Gems |
| Popular | 1 Rare Lootbox + 50 Gems + Cosmetic |
| Celebrity | 1 Epic Lootbox + 100 Gems + Title |
| Star | 1 Epic Lootbox + 200 Gems + Exclusive Cosmetic |
| Icon | 1 Legendary Lootbox + 500 Gems + Unique Effect |
| Legend | 1 Legendary Lootbox + 1,000 Gems + Monument Option |

---

## Fame Benefits

### Hosting Bonus (Primary Benefit)

When you host a party, you earn a percentage of what guests earn:

| Tier | Hosting Bonus |
|------|---------------|
| Newcomer | 0% |
| Local | 0.5% |
| Known | 1% |
| Popular | 1.5% |
| Celebrity | 2% |
| Star | 2.5% |
| Icon | 3% |
| Legend | 3.5% |

**Example:** You're a Star hosting 15 guests. They collectively earn $10,000 Cash playing minigames. You get $250 Cash (2.5%) as hosting bonus.

### Other Fame Benefits

| Tier | Unlocks |
|------|---------|
| Local (1,000) | Can host Small parties (1 Crystal + $500) |
| Known (3,000) | Apartment featured in "Rising" list |
| Popular (6,000) | Exclusive cosmetic set, Big parties (2 Crystals + $2,000) |
| Celebrity (12,000) | VIP lounge access, Mega parties (4 Crystals + $5,000) |
| Star (25,000) | Exclusive title colors, rare cosmetics |
| Icon (50,000) | Legacy cosmetics, permanent recognition |
| Legend (100,000) | Ultimate flex items, monument in city |

**Note:** Boosted parties require both Cash AND Crystals. Casual Hangouts remain free for all players. See [Housing_System.md](Housing_System.md) for full party details.

---

## Competitive Balance

### Preventing Permanent Domination

**Problem:** Rich player hosts 24/7, stays #1 forever.

**Solutions:**

1. **Threshold still applies** — Even #1 must earn 50 fame daily
2. **Diminishing hosting returns** — After 4 hours/day, hosting fame gains reduce by 50%
3. **Guest diversity bonus** — Same guests = normal fame; new guests = +50% fame
4. **Leaderboard resets** — Weekly/monthly competitive leaderboards alongside lifetime

### Catch-Up Mechanics

**Problem:** New player can never reach old player.

**Solutions:**

1. **Decay equalizes over time** — Inactive veterans fall
2. **Events spike fame** — Limited-time high-fame opportunities
3. **Tier-based competition** — Compete within your tier, not globally
4. **Seasonal rankings** — Fresh starts for competitive players

---

## Open Questions

| Question | Considerations |
|----------|----------------|
| Exact threshold numbers | Need playtesting to feel fair |
| Decay percentages | 3%/5% might need adjustment |
| Hosting diminishing returns | After 4 hours feels right? |
| Guest diversity formula | How to calculate "new" guests? |
| Seasonal reset frequency | Weekly? Monthly? Quarterly? |

---

## Summary

Fame rewards players who:
- Show up consistently (daily login helps!)
- Create social value (parties, good apartments, emote syncing)
- Engage with multiple systems
- Maintain activity without burnout

Fame is gentle to:
- Casual players (low thresholds, grace periods)
- Real life interruptions (recoverable decay)
- New players (protected newcomer tier)

---

*See [Economy_System.md](Economy_System.md) for how Fame interacts with currencies.*
*See [Housing_System.md](Housing_System.md) for party hosting details.*
