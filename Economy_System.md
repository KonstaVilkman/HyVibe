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

**Design Philosophy:** Two currencies, one simple loop. Cash for everyday gameplay, Gems for exciting rewards.

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

Lootboxes can contain:
- **Cosmetics:** Outfits, furniture, pets, particles, emotes
- **Currency:** Cash ($50-500), Gems (5-50)
- **Materials:** Crafting components, rare resources
- **Consumables:** Temporary boosts, social items

### Duplicate Protection
- First duplicate: 100% item value as Cash
- Repeated duplicates: 75% item value as Cash
- Legendary duplicates: Full value + 10 Gems

### Earning Lootboxes (Free)

| Source | Box Type | Frequency |
|--------|----------|-----------|
| Level up (every level) | Common | Per level |
| Level milestone (every 10 levels) | Rare | Per milestone |
| Achievement (Gold tier) | Rare | One-time |
| Achievement (Platinum tier) | Epic | One-time |
| Weekly challenge completion | Rare | Weekly |
| Event participation | Event-specific | Per event |
| Fame tier promotion | Rare | Per tier |

---

## Economy Flow Diagram

```
┌─────────────────────────────────────────────────────────────┐
│                     EARNING SOURCES                          │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  ┌─────────┐  ┌─────────┐  ┌─────────┐  ┌─────────┐        │
│  │  JOBS   │  │MINIGAMES│  │ DAILY   │  │ EVENTS  │        │
│  │         │  │         │  │ LOGIN   │  │         │        │
│  └────┬────┘  └────┬────┘  └────┬────┘  └────┬────┘        │
│       │            │            │            │              │
│       ▼            ▼            ▼            ▼              │
│  ┌─────────────────────────────────────────────────────┐   │
│  │               PLAYER WALLET                          │   │
│  │  Cash: $$$              Gems: ◇◇◇                   │   │
│  └─────────────────────────────────────────────────────┘   │
│       │                         │                           │
│       ▼                         ▼                           │
├─────────────────────────────────────────────────────────────┤
│                     SPENDING SINKS                           │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  ┌─────────┐  ┌─────────┐  ┌─────────┐  ┌─────────┐        │
│  │COSMETICS│  │ HOUSING │  │LOOTBOXES│  │ TRADING │        │
│  │  (Cash) │  │  (Cash) │  │ (Gems)  │  │  (Cash) │        │
│  └─────────┘  └─────────┘  └─────────┘  └─────────┘        │
│                                                              │
└─────────────────────────────────────────────────────────────┘
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
| Cosmetics (most) | Account-bound items |
| Furniture (most) | Achievement rewards |
| Materials | Lootboxes (unopened) |
| Crafting items | Level/Fame |

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

*See FAME_SYSTEM.md for Fame milestone rewards.*
*See JOBS_SYSTEM.md for earning rates by job.*
*See HOUSING_SYSTEM.md for apartment costs.*
