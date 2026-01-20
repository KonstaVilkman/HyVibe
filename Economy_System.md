# Economy System

**Purpose:** Resource flow that drives player goals and maintains balance.  
**Status:** Concept Phase

---

## Currency Overview

| Currency | Role | Earn Rate | Tradeable? |
|----------|------|-----------|------------|
| **Cash ($)** | Common, daily use | Fast | Yes (player-to-player) |
| **Orbs** | Premium, rare purchases | Slow | No (sacred) |
| **Anchor [TBD]** | Stable-value trade item, sinks | Medium | Yes (this IS the trade currency) |
| **Event Tickets** | Time-limited event items | Event-only | No |

---

## Cash ($)

### Purpose
Everyday currency. Easy to earn, easy to spend. Keeps players engaged with basic loops.

### Earning Cash

| Source | Amount | Frequency |
|--------|--------|-----------|
| Entry job task | $5-15 | Per task |
| Skilled job task | $15-30 | Per task |
| Minigame win | $20-50 | Per win |
| Minigame participation | $5-10 | Per game |
| Daily login | $50 | Daily |
| Selling items to NPC | Varies | Anytime |
| Player trades | Varies | Anytime |
| Hosting bonus (from Fame) | % of guest earnings | During parties |

### Spending Cash

| Sink | Cost Range | Notes |
|------|------------|-------|
| Basic cosmetics | $100-500 | Clothes, common items |
| Basic furniture | $50-300 | Apartment decor |
| Apartment rent/upgrade | $500-5,000 | Progression |
| Food/drinks (emotes) | $10-50 | Social items |
| Job tools | $100-500 | Efficiency upgrades |
| Trading with players | Varies | Player economy |

### Balance Goal
Players should earn ~$500-1,000/hour of active play. Basic cosmetics accessible within first few hours.

---

## Orbs

### Purpose
Premium currency that feels special. Marks significant achievements and unlocks exclusive items.

### Earning Orbs

| Source | Amount | Frequency |
|--------|--------|-----------|
| Achievement unlocked | 5-50 | One-time |
| Level milestone (every 5 levels) | 10-25 | Progression |
| Rare drop from activities | 1-5 | Random, rare |
| Event completion | 10-30 | Per event |
| Daily login streak (7 days) | 10 | Weekly |
| Featured apartment bonus | 25 | If selected |

### Spending Orbs

| Sink | Cost Range | Notes |
|------|------------|-------|
| Premium cosmetics | 50-200 | Exclusive looks |
| Rare furniture | 30-150 | Statement pieces |
| Exclusive pets | 100-300 | Companions |
| Special effects/particles | 50-150 | Visual flair |
| Premium apartment themes | 100-250 | Full room makeovers |

### Balance Goal
Players earn ~50-100 Orbs/week through normal play. Premium items feel earned, not bought.

### Why Not Tradeable
- Maintains "earned" feeling
- Prevents inflation through trading
- Keeps Orbs special and personal
- Anchor item handles trade economy

---

## Anchor Item [NAME TBD]

### Purpose
Stable-value item for player trading and premium sinks. The "World Lock" of this economy.

### Naming Considerations

The name should feel:
- Unique to this world
- Slightly mysterious
- Worth collecting
- Not generic (not "Keys" or "Tokens")

**Candidates:**

| Name | Vibe | Fits Story? |
|------|------|-------------|
| **Echoes** | Remnants of the city's origin | âœ“ Mysterious |
| **Sparks** | Energy that powers the city | âœ“ Modern-fantasy |
| **Marks** | City's official seal of value | âœ“ Urban |
| **Fragments** | Pieces of something greater | âœ“ Mysterious |
| **Pulses** | Heartbeat of the city | âœ“ Modern |
| **Glints** | Rare, shiny, valuable | âœ“ Collectible feel |
| **Creds** | Street credibility made tangible | âœ“ Urban |
| **Halos** | Circles of light/value | âœ“ Fantasy touch |

**Decision needed.** Placeholder: `[ANCHOR]`

### Earning Anchor

| Source | Amount | Frequency |
|--------|--------|-----------|
| Job milestone (Level 5, 10) | 1-3 | Per milestone |
| Level milestone (every 10 levels) | 2-5 | Progression |
| Rare activity drops | 1 | Random, uncommon |
| Event rewards | 2-5 | Per event |
| Trading with players | Varies | Player economy |
| Achievement tiers | 1-5 | One-time |

### Spending Anchor (SINKS)

| Sink | Cost | Frequency | Notes |
|------|------|-----------|-------|
| **Party Hosting** | 1-5 | Often | Core sink for Fame |
| **Crafting Recipes** | 1-10 | Sometimes | Rare item creation |
| **VIP Area Access** | 1-2 | Often | Per entry or day pass |
| **Shop Reroll** | 1 | Daily option | Refresh daily deals |
| **Quest Reroll** | 1 | Daily option | Get new dailies |
| **Exclusive Shop Items** | 5-20 | Sometimes | Rare cosmetics/furniture |
| **Career Unlock** | 3-5 | Once per career | Entry â†’ Skilled |

### Why These Sinks Work

| Sink | Why It Maintains Value |
|------|------------------------|
| Party Hosting | Recurring, scales with Fame ambition |
| Crafting | Consumable, rare items desirable |
| VIP Access | Recurring, rewards justify cost |
| Rerolls | Small, frequent, adds up |
| Exclusive Items | Desirable, limited |
| Career Unlock | One-time but universal need |

### Trade Hierarchy

Like World Locks â†’ Diamond Locks â†’ Blue Gem Locks:

```
1 [ANCHOR] = Base unit
10 [ANCHOR] = Silver [ANCHOR]
100 [ANCHOR] = Gold [ANCHOR]
1000 [ANCHOR] = Diamond [ANCHOR]
```

This allows large trades without counting hundreds of items.

---

## Event Tickets

### Purpose
Time-limited currency for event-exclusive items. Creates urgency and event engagement.

### Earning Event Tickets

| Source | Amount | Notes |
|--------|--------|-------|
| Event daily login | 5 | During event |
| Event tasks | 10-30 | Event-specific |
| Event minigames | 5-15 | Per participation |
| Event milestones | 20-50 | Achievement |

### Spending Event Tickets

| Item | Cost | Notes |
|------|------|-------|
| Event cosmetics | 50-200 | Limited time |
| Event furniture | 30-150 | Themed items |
| Event pets | 100-250 | Exclusive companions |
| Event loot boxes* | 25-50 | If implemented (odds disclosed) |

*Loot boxes optional and must follow Hytale's disclosure rules.

### After Event Ends
- Unspent tickets convert to small Cash amount
- OR: Tickets carry over to next event (decision needed)
- Event items become unobtainable (rarity increases)

---

## Economy Flow Diagram

```
â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”
â”‚                     EARNING SOURCES                          â”‚
â”œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”¤
â”‚                                                              â”‚
â”‚  â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”  â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”  â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”  â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”        â”‚
â”‚  â”‚  JOBS   â”‚  â”‚MINIGAMESâ”‚  â”‚ DAILY   â”‚  â”‚ EVENTS  â”‚        â”‚
â”‚  â”‚         â”‚  â”‚         â”‚  â”‚ LOGIN   â”‚  â”‚         â”‚        â”‚
â”‚  â””â”€â”€â”€â”€â”¬â”€â”€â”€â”€â”˜  â””â”€â”€â”€â”€â”¬â”€â”€â”€â”€â”˜  â””â”€â”€â”€â”€â”¬â”€â”€â”€â”€â”˜  â””â”€â”€â”€â”€â”¬â”€â”€â”€â”€â”˜        â”‚
â”‚       â”‚            â”‚            â”‚            â”‚              â”‚
â”‚       â–¼            â–¼            â–¼            â–¼              â”‚
â”‚  â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”       â”‚
â”‚  â”‚                PLAYER WALLET                     â”‚       â”‚
â”‚  â”‚  Cash: $$$    Orbs: â—‹â—‹â—‹    Anchor: â—†â—†â—†          â”‚       â”‚
â”‚  â””â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜       â”‚
â”‚       â”‚            â”‚            â”‚                           â”‚
â”‚       â–¼            â–¼            â–¼                           â”‚
â”œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”¤
â”‚                     SPENDING SINKS                           â”‚
â”œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”¤
â”‚                                                              â”‚
â”‚  â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”  â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”  â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”  â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”        â”‚
â”‚  â”‚COSMETICSâ”‚  â”‚ HOUSING â”‚  â”‚ PARTIES â”‚  â”‚VIP/CRAFTâ”‚        â”‚
â”‚  â”‚($/Orbs) â”‚  â”‚   ($)   â”‚  â”‚(Anchor) â”‚  â”‚(Anchor) â”‚        â”‚
â”‚  â””â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜  â””â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜  â””â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜  â””â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜        â”‚
â”‚                                                              â”‚
â””â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜
```

---

## Trading System (Secondary Feature)

### How It Works
- Player-to-player direct trades
- Trade window shows both inventories
- Both players confirm before trade executes
- Trade history logged (scam protection)

### What's Tradeable

| Tradeable | Not Tradeable |
|-----------|---------------|
| Cash | Orbs |
| Anchor items | Event Tickets |
| Cosmetics (most) | Account-bound items |
| Furniture (most) | Achievement rewards |
| Materials | Level/Fame |

### Anti-Scam Measures
- Trade confirmation delay (3 seconds)
- "Are you sure?" for high-value trades
- Report system for scammers
- Trade history viewable

---

## Inflation Prevention

| Risk | Prevention |
|------|------------|
| Too much Cash | Multiple sinks, no NPC buying |
| Anchor devaluation | Strong sink variety |
| Rich get richer | Hosting bonuses capped, decay exists |
| New player poverty | Protected early progression, easy Cash |

---

## Open Questions

| Question | Options |
|----------|---------|
| Anchor item name | See candidates above |
| Event ticket carryover? | Convert to Cash or save for next? |
| Exact earn/spend rates | Needs playtesting |
| Trade tax? | Small % removed from trades to sink currency? |

---

*See FAME_SYSTEM.md for hosting bonus details.*  
*See JOBS_SYSTEM.md for earning rates by job.*