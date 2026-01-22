# Economy System

**Purpose:** Resource flow that drives player goals and maintains balance.
**Status:** Concept Phase
**Last Updated:** January 2026

---

## Currency Overview

| Currency | Role | Earn Rate | Tradeable? |
|----------|------|-----------|------------|
| **Cash ($)** | Common, daily use | Fast | Yes (player-to-player) |
| **Gems** | Premium, lootboxes, exclusive items | Medium | No |
| **Crystals** | Economy anchor, party hosting, housing features | Moderate | Yes (player-to-player) |

**Design Philosophy:** Two currencies plus one anchor item. Cash for everyday gameplay, Gems for lootboxes, Crystals as the economy foundation and trading standard.

---

## Cash ($)

### Purpose
Everyday currency. Easy to earn, easy to spend. Keeps players engaged with basic loops.

### Earning Cash

| Source | Amount | Frequency |
|--------|--------|-----------|
| Entry job task | $10-15 | Per task |
| Skilled job task | $25-40 | Per task |
| Minigame win | $30-50 | Per win |
| Minigame participation | $10-20 | Per game |
| Daily login | $100 | Daily |
| Weekly login streak (7 days) | $500 bonus | Weekly |
| Selling items to NPC | 50% item value | Anytime |
| Player trades | Varies | Anytime |
| Lootbox (common drop) | $50-200 | Random |

### Spending Cash

| Sink | Cost Range | Notes |
|------|------------|-------|
| Basic cosmetics | $200-1,000 | Common outfits, furniture |
| Apartment upgrades | $2,000-50,000 | See Housing System |
| Food/drinks (social items) | $20-100 | Emotes, consumables |
| Job tools | $200-500 | Efficiency items |
| Basic lootboxes | $500 | Common tier |
| Trading with players | Varies | Player economy |

### Balance Goal
- **Target:** $800-1,200/hour of active play
- **New player first hour:** ~$500 (enough for first cosmetic)
- **Daily casual (1 hour):** ~$1,000

---

## Gems

### Purpose
Premium currency that makes earning feel exciting. Used for lootboxes and exclusive purchases.

### Earning Gems

| Source | Amount | Frequency |
|--------|--------|-----------|
| Level milestone (every 5 levels) | 10-30 | Progression |
| Achievement unlocked | 5-50 | One-time |
| Daily login | 5 | Daily |
| Weekly login streak (7 days) | 25 bonus | Weekly |
| Event participation | 10-50 | Per event |
| Fame milestone (tier up) | 20-100 | Progression |
| Lootbox (rare drop) | 10-50 | Random |

### Spending Gems

| Sink | Cost | Notes |
|------|------|-------|
| Common Lootbox | 25 Gems | Basic rewards |
| Rare Lootbox | 75 Gems | Better odds, exclusive items |
| Epic Lootbox | 150 Gems | Premium items, guaranteed rare+ |
| Legendary Lootbox | 300 Gems | Best odds, exclusive legendaries |
| Direct purchase (exclusive items) | 50-500 | Rotating shop |

### Balance Goal
- **Target:** 50-80 Gems/week through normal play
- **Common Lootbox:** Affordable every 2-3 days
- **Rare Lootbox:** Weekly reward for active players
- **Epic/Legendary:** Monthly goals or event rewards

---

## Crystals

### Purpose
Crystals are the **economy anchor** — a tradeable item with real utility that becomes the backbone of player-to-player trading. Think of them like World Locks in Growtopia: valuable because they're useful, not just rare.

### Why Crystals Exist
| Problem | How Crystals Solve It |
|---------|----------------------|
| Cash inflates over time | Crystals have consistent utility sinks |
| No trading standard | Crystals become de facto trade currency |
| Parties need meaning | Crystal cost makes hosting intentional |
| Housing needs prestige | Crystal-locked features create goals |

### Earning Crystals

Crystals drop from **lootboxes only** — they cannot be purchased directly or earned from activities.

| Lootbox Tier | Crystal Drop Chance | Expected per 10 Boxes |
|--------------|---------------------|----------------------|
| Common | 5-8% | ~0.5-0.8 |
| Rare | 12-15% | ~1.2-1.5 |
| Epic | 20-25% | ~2-2.5 |
| Legendary | 40-50% | ~4-5 |

**Weekly Crystal Income (by player type):**

| Player Type | Weekly Boxes Opened | Crystals/Week |
|-------------|---------------------|---------------|
| Casual | ~15-20 | 1-2 |
| Mid-game | ~35-50 | 4-5 |
| High-level | ~80-120 | 10-15 |

### Spending Crystals

| Sink | Cost (Crystals) | Frequency | Purpose |
|------|-----------------|-----------| --------|
| **Small Party** | 1 | Recurring | Entry-level hosting |
| **Big Party** | 2 | Recurring | Standard hosting |
| **Mega Party** | 4 | Recurring | Event-style hosting |
| **Balcony Unlock** | 10-15 | One-time | Housing prestige |
| **Rooftop Access** | 15-20 | One-time | Housing prestige |
| **Secret Room** | 25-35 | One-time | Aspirational goal |
| **Custom Entrance** | 10-15 | One-time | Housing personalization |
| **Premium Shop Items** | 5-20 | One-time | Exclusive cosmetics |

### Balance Target

| Player Type | Crystals/Week | Can Host |
|-------------|---------------|----------|
| Mid-game | 4-5 | 1 Big Party per 2-3 days |
| High-level | 10-15 | 1-2 Big Parties per day |

### Trading Value

Crystals are **fully tradeable** between players. This creates natural economy dynamics:
- Social players (who host often) buy Crystals from others
- Non-social players sell Crystals for Cash or items
- Market price stabilizes based on supply/demand

---

## Lootbox System

### Philosophy
Lootboxes are the **primary excitement mechanic**. Opening boxes should feel rewarding, surprising, and fair.

**Key Principles:**
- Always disclose odds (required by many platforms)
- No duplicates of equipped items
- Duplicate items convert to Cash (not lost)
- Guaranteed minimum value per box

### Lootbox Tiers

| Tier | Cost (Gems) | Cost (Cash) | Guaranteed |
|------|-------------|-------------|------------|
| **Common** | 25 | $500 | 1 item (Common+) |
| **Rare** | 75 | — | 1 item (Uncommon+) |
| **Epic** | 150 | — | 1 item (Rare+), 1 bonus |
| **Legendary** | 300 | — | 1 item (Epic+), 2 bonus |

### Drop Rates (Common Lootbox)

| Rarity | Chance | Examples |
|--------|--------|----------|
| Common | 60% | Basic furniture, simple outfits |
| Uncommon | 25% | Themed items, better cosmetics |
| Rare | 12% | Statement pieces, pets |
| Epic | 2.5% | Premium sets, rare particles |
| Legendary | 0.5% | Ultra-rare, flex items |

### Drop Rates (Rare Lootbox)

| Rarity | Chance |
|--------|--------|
| Uncommon | 50% |
| Rare | 35% |
| Epic | 12% |
| Legendary | 3% |

### Drop Rates (Epic Lootbox)

| Rarity | Chance |
|--------|--------|
| Rare | 55% |
| Epic | 35% |
| Legendary | 10% |

### Drop Rates (Legendary Lootbox)

| Rarity | Chance |
|--------|--------|
| Epic | 60% |
| Legendary | 40% |

### Lootbox Contents

Lootboxes contain items from these categories:

| Category | Examples | Rarity Range |
|----------|----------|--------------|
| **Crystals** | Economy anchor item | Special (see Crystal section) |
| **Titles** | "Plant Parent", "Night Owl" | Common-Rare |
| **Name Colors/Effects** | Gradient names, sparkle text | Uncommon-Rare |
| **Badges** | Profile display items | Common-Rare |
| **Emotes** | Animations, expressions | Common-Epic |
| **Furniture** | All housing items | All rarities |
| **Pets** | Companions, creatures | Rare-Legendary |
| **Particles/Trails** | Footsteps, auras, effects | Rare-Epic |
| **Plant Seeds** | Common, Rare, Epic seeds | Common-Rare |
| **Cash** | $50-500 | Common filler |
| **Gems** | 5-50 | Rare drop |

**Design Note:** All tiers of lootboxes can contain all cosmetic types. Higher tiers have better odds at rare content but nothing is tier-locked (except themed boxes like "Legendary Particle Box").

### Duplicate Protection
- First duplicate: 100% item value as Cash
- Repeated duplicates: 75% item value as Cash
- Legendary duplicates: Full value + 10 Gems

### Earning Lootboxes (Free)

**Progression Sources:**

| Source | Box Type | Frequency |
|--------|----------|-----------|
| Level up (every level) | Common | Per level |
| Level milestone (every 10 levels) | Rare | Per milestone |
| Achievement (Gold tier) | Rare | One-time |
| Achievement (Platinum tier) | Epic | One-time |
| Fame tier promotion | Rare-Legendary | Per tier |
| Event participation | Event-specific | Per event |

**Repeatable Sources:**

| Source | Box Type | Frequency |
|--------|----------|-----------|
| Daily challenge completion (5/day) | Common | Up to 5/day |
| Weekly challenge completion (8/week) | Mixed (Common-Epic) | Up to 8/week |
| Minigame wins | Common | 1 per 2 wins |
| Login streak (7 days) | Common | Weekly |
| Login streak (14 days) | Rare | Bi-weekly |
| Login streak (30 days) | Epic | Monthly |

**Passive Sources (Plants):**

| Plant Type | Grow Time | Yield |
|------------|-----------|-------|
| Common Seed | 12 hours | 1 Common Lootbox |
| Rare Seed | 48 hours | 1 Rare Lootbox |
| Epic Seed | 72 hours | 1 Epic Lootbox |
| Super Seed | 72 hours | 1 Epic + chance for 1-2 bonus boxes (any rarity) |

*See [Housing_System.md](Housing_System.md) for plant slot details.*

**Shop Purchase:**

| Box Type | Cash Cost | Gems Cost |
|----------|-----------|-----------|
| Common | $500 | 25 |
| Rare | — | 75 |
| Epic | — | 150 |
| Legendary | — | 300 |

---

## Economy Flow Diagram

```
+----------------------------------------------------------------------+
|                        EARNING SOURCES                                |
+----------------------------------------------------------------------+
|                                                                       |
|  +---------+  +---------+  +---------+  +---------+  +--------+      |
|  |  JOBS   |  |MINIGAMES|  | LOGIN   |  | EVENTS  |  | PLANTS |      |
|  |         |  |         |  | STREAK  |  |         |  |        |      |
|  +----+----+  +----+----+  +----+----+  +----+----+  +---+----+      |
|       |            |            |            |            |           |
|       v            v            v            v            v           |
|  +--------------------------------------------------------------------+
|  |                    PLAYER INVENTORY                                |
|  |  Cash: $$$        Gems: ***        Crystals: +++                  |
|  +--------------------------------------------------------------------+
|       |                    |                    |                     |
|       v                    v                    v                     |
+----------------------------------------------------------------------+
|                        SPENDING SINKS                                 |
+----------------------------------------------------------------------+
|                                                                       |
|  +---------+  +---------+  +---------+  +---------+  +--------+      |
|  |COSMETICS|  | HOUSING |  |LOOTBOXES|  | PARTIES |  |TRADING |      |
|  |  (Cash) |  |  (Cash) |  | (Gems)  |  |(Crystal)|  | (All)  |      |
|  +---------+  +---------+  +---------+  +---------+  +--------+      |
|                                                                       |
|                    +---------------------+                            |
|                    |  HOUSING FEATURES   |                            |
|                    |     (Crystals)      |                            |
|                    | Balcony, Secret Room|                            |
|                    +---------------------+                            |
|                                                                       |
+----------------------------------------------------------------------+
```

---

## Trading System

### How It Works
- Player-to-player direct trades
- Trade window shows both inventories
- Both players confirm before trade executes
- Trade history logged (scam protection)

### What's Tradeable

| Tradeable | Not Tradeable |
|-----------|---------------|
| Cash | Gems |
| **Crystals** | Account-bound items |
| Cosmetics (most) | Achievement rewards |
| Furniture (most) | Lootboxes (unopened) |
| Materials | Level/Fame |
| Plant Seeds | — |

### Anti-Scam Measures
- Trade confirmation delay (3 seconds)
- "Are you sure?" for high-value trades
- Report system for scammers
- Trade history viewable for 30 days

---

## Inflation Prevention

| Risk | Prevention |
|------|------------|
| Too much Cash | NPC sells at fixed prices, no buyback inflation |
| Item devaluation | Lootbox odds maintain rarity |
| Rich get richer | Fame bonuses capped, no exponential returns |
| New player poverty | Generous early rewards, catch-up mechanics |

---

## Event Currency

During seasonal events, a **temporary Event Token** is added:

| Aspect | Details |
|--------|---------|
| Earning | Event tasks, minigames, daily login |
| Spending | Event shop (exclusive items) |
| After event | Converts to Cash (10 Tokens = $100) |
| Tradeable | No |

**Why temporary?** Creates urgency, doesn't clutter main economy, makes event items rare.

---

## Real Money Purchases (Optional)

If monetization is enabled:

| Package | Price | Contents |
|---------|-------|----------|
| Starter Pack | $4.99 | 100 Gems + 1 Rare Lootbox |
| Gem Bundle (Small) | $4.99 | 150 Gems |
| Gem Bundle (Medium) | $9.99 | 350 Gems |
| Gem Bundle (Large) | $19.99 | 800 Gems |
| Season Pass | $9.99 | See Progression System |

**Rules:**
- No gameplay advantages
- No exclusive items (all earnable in-game)
- Just faster access to cosmetics
- Prices clearly displayed

---

## Balance Checkpoints

### New Player (Level 1-10)
- Should afford: First outfit, basic furniture
- Cash earned: ~$5,000
- Gems earned: ~50
- Lootboxes opened: 5-8 (from leveling)

### Mid Player (Level 11-30)
- Should afford: Apartment upgrade, multiple outfits
- Cash earned: ~$50,000 total
- Gems earned: ~300 total
- Lootboxes opened: 30-40

### Established Player (Level 31-50)
- Should afford: Loft apartment, full wardrobe
- Cash earned: ~$200,000 total
- Gems earned: ~800 total
- Lootboxes opened: 80-100

### Veteran (Level 51+)
- Collecting rare items
- Trading for specific pieces
- Event exclusives become focus

---

*See [Fame_System.md](Fame_System.md) for Fame milestone rewards.*
*See [Jobs_System.md](Jobs_System.md) for earning rates by job.*
*See [Housing_System.md](Housing_System.md) for apartment costs.*
