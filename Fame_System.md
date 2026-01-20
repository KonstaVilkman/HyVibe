# Fame System

**Purpose:** Social status that rewards active, social players.  
**Status:** Concept Phase

---

## Core Concept

Fame measures how **known** and **active** a player is. It's not a currency â€” it's a reputation score that unlocks benefits and shows status.

**Key Principles:**
- Fame must be earned continuously (decay exists)
- True grinders rank high, half-actives stay middle
- No hard cap, but diminishing display returns
- Leaderboard rank matters more than raw number

---

## Why Players Want Fame

| Incentive | How Fame Delivers It |
|-----------|---------------------|
| **Status** | Visible rank/title that others see |
| **Passive Income** | Higher fame = better hosting bonuses |
| **Exclusivity** | Fame-locked cosmetics and areas |
| **Recognition** | Leaderboard presence, being "known" |
| **Aspiration** | Seeing high-fame players creates goals |

---

## Earning Fame

| Action | Fame Gained | Notes |
|--------|-------------|-------|
| Daily login | +5 | Baseline for showing up |
| Someone visits your apartment | +2 | Encourages good apartments |
| Someone likes your apartment | +5 | Quality over quantity |
| Hosting party (per guest per 5 min) | +1 | Core fame engine |
| Guest plays minigame at your party | +3 | Encourages fun parties |
| Winning public minigame | +10 | Skill reward |
| Job task completed | +1 | Grind reward |
| Achievement unlocked | +20-100 | Milestone spikes |
| Event participation | +15 | Engagement reward |

**Design Note:** Fame sources are varied so players can earn through different playstyles.

---

## Fame Decay â€” Threshold Model

### The Problem to Solve
- Active players should rank high
- Half-active players should rank middle
- Inactive players should fall
- Nobody should "retire" at the top

### How It Works

**Daily Threshold:** Minimum fame to earn that day to avoid decay.

| Current Fame | Rank Tier | Daily Threshold |
|--------------|-----------|-----------------|
| 0 - 499 | Newcomer | 0 (Protected) |
| 500 - 1,999 | Local | 25 |
| 2,000 - 4,999 | Known | 40 |
| 5,000 - 9,999 | Popular | 60 |
| 10,000 - 24,999 | Celebrity | 80 |
| 25,000 - 49,999 | Star | 100 |
| 50,000+ | Icon | 120 (Capped) |

**Threshold caps at 120** â€” even with 1 million fame, you only need 120/day.

---

### Decay Rules

| Scenario | What Happens |
|----------|--------------|
| **Hit threshold** | No decay, fame grows |
| **Miss threshold (Day 1)** | Warning, no decay yet |
| **Miss threshold (Day 2)** | -5% fame |
| **Miss threshold (Day 3+)** | -7% fame per day |
| **Return and hit threshold** | Decay stops immediately |

### Half-Active Prevention

**Problem:** Player earns 30 fame, threshold is 40. They're "active" but not enough.

**Solution:** Partial credit doesn't exist. Either hit threshold or don't.

| Earned | Threshold | Result |
|--------|-----------|--------|
| 45 | 40 | âœ“ No decay |
| 39 | 40 | âœ— Counts as miss |
| 0 | 40 | âœ— Counts as miss |

**This forces commitment:** You can't coast at 50% effort.

---

### Decay Math Examples

**Example A: Celebrity goes inactive**

```
Day 0: 7,000 Fame (Celebrity, threshold 60)
Day 1: Earns 20 fame â€” MISS (warning)
Day 2: Earns 0 fame â€” MISS (-5%) = 6,650
Day 3: Earns 0 fame â€” MISS (-7%) = 6,185
Day 4: Earns 0 fame â€” MISS (-7%) = 5,752
Day 5: Earns 75 fame â€” HIT, decay stops at 5,752
```

**Example B: Half-active player**

```
Day 0: 3,000 Fame (Known, threshold 40)
Day 1: Earns 35 fame â€” MISS (warning)
Day 2: Earns 38 fame â€” MISS (-5%) = 2,850
Day 3: Earns 42 fame â€” HIT, decay stops
Day 4: Earns 30 fame â€” MISS (warning)
Day 5: Earns 25 fame â€” MISS (-5%) = 2,708
...cycles between decay and recovery, stays mid-tier
```

**Example C: True grinder**

```
Day 0: 15,000 Fame (Celebrity, threshold 80)
Day 1: Earns 150 fame â€” HIT = 15,150
Day 2: Earns 200 fame â€” HIT = 15,350
Day 3: Earns 180 fame â€” HIT = 15,530
...consistently grows, climbs leaderboard
```

---

## Fame Display â€” Rank Over Number

### Why Hide Raw Numbers?

- Prevents "number go big" obsession
- Focuses on relative position
- Makes leaderboard rank meaningful
- Reduces intimidation for new players

### Display Format

Instead of: `Fame: 47,832`

Show: `â˜… Star #12`

| Component | Meaning |
|-----------|---------|
| â˜… | Tier icon |
| Star | Tier name |
| #12 | Leaderboard position within tier (or global) |

### Tier Titles

| Fame Range | Title | Icon |
|------------|-------|------|
| 0 - 499 | Newcomer | Â· |
| 500 - 1,999 | Local | â—‹ |
| 2,000 - 4,999 | Known | â— |
| 5,000 - 9,999 | Popular | â— |
| 10,000 - 24,999 | Celebrity | â˜… |
| 25,000 - 49,999 | Star | â˜…â˜… |
| 50,000 - 99,999 | Icon | â˜…â˜…â˜… |
| 100,000+ | Legend | âœ¦ |

### Prestige Tiers (High Fame)

For players beyond Icon, add prestige markers:

| Fame | Display |
|------|---------|
| 50,000 | Icon I |
| 75,000 | Icon II |
| 100,000 | Legend I |
| 150,000 | Legend II |
| 200,000 | Legend III |
| ... | ... |

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

**Example:** You're a Star hosting 15 guests. They collectively earn 10,000 Cash playing minigames. You get 250 Cash (2.5%) as hosting bonus.

### Other Fame Benefits

| Tier | Unlocks |
|------|---------|
| Local (500) | Can host basic parties |
| Known (2,000) | Apartment featured in "Rising" list |
| Popular (5,000) | Exclusive cosmetic set unlocked |
| Celebrity (10,000) | VIP lounge access, premium party hosting |
| Star (25,000) | Exclusive title colors, rare cosmetics |
| Icon (50,000) | Legacy cosmetics, permanent recognition |
| Legend (100,000) | Ultimate flex items, monument in city |

---

## Competitive Balance

### Preventing Permanent Domination

**Problem:** Rich player hosts 24/7, stays #1 forever.

**Solutions:**

1. **Threshold still applies** â€” Even #1 must earn 120 fame daily
2. **Diminishing hosting returns** â€” After X hours/day, hosting fame gains reduce
3. **Guest diversity bonus** â€” Same guests = less fame; new guests = more fame
4. **Leaderboard resets** â€” Weekly/monthly competitive leaderboards alongside lifetime

### Catch-Up Mechanics

**Problem:** New player can never reach old player.

**Solutions:**

1. **Decay equalizes over time** â€” Inactive veterans fall
2. **Events spike fame** â€” Limited-time high-fame opportunities
3. **Tier-based competition** â€” Compete within your tier, not globally
4. **Seasonal rankings** â€” Fresh starts for competitive players

---

## Open Questions

| Question | Considerations |
|----------|----------------|
| Exact threshold numbers | Need playtesting to feel fair |
| Decay percentages | 5%/7% might be too harsh or lenient |
| Hosting diminishing returns | After how many hours? |
| Guest diversity formula | How to calculate "new" guests? |
| Seasonal reset frequency | Weekly? Monthly? Quarterly? |

---

## Summary

Fame rewards players who:
- Show up consistently
- Create social value (parties, good apartments)
- Engage with multiple systems
- Commit to the threshold, not half-effort

Fame punishes:
- Inactivity
- Half-hearted engagement
- Trying to "retire" at the top

---

*See ECONOMY_SYSTEM.md for how Fame interacts with currencies.*