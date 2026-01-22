# Black Market Dealer

**Purpose:** Secret NPC with exclusive rotating deals and rare items.
**Location:** Random spawn points (hidden)
**Status:** Design Phase (Phase 1+)

---

## Overview

The Black Market Dealer is a **secret NPC** who appears in random hidden locations throughout the server. Finding them rewards players with access to exclusive deals, rare items at discounts, and unique trades not available elsewhere.

**Design Intent:**
- Creates exploration incentive
- Rewards observant players
- Adds mystery and excitement
- Gives veterans something to hunt for
- Community sharing ("I found the dealer!")

---

## Appearance

| Aspect | Design |
|--------|--------|
| **Style** | Mysterious, hooded figure |
| **Vibe** | Slightly shady but not threatening |
| **Indicator** | No overhead icon (secret!) |
| **Recognition** | Distinct silhouette, subtle glow |
| **Voice/Text** | Whispered, conspiratorial tone |

**Sample Dialogue:**
- *"Psst... looking for something special?"*
- *"You didn't see me here, got it?"*
- *"These deals won't last forever..."*
- *"Tell your friends... or don't."*

---

## Spawn System

### Spawn Schedule

| Aspect | Details |
|--------|---------|
| **Active Hours** | Spawns for 2-4 hours, then despawns |
| **Frequency** | 2-3 times per day |
| **Announcement** | None (players must discover) |
| **Server-Wide** | Same location for all players |

### Spawn Timing Pattern

```
Daily Schedule (Example):
├── 00:00-06:00  No spawn window
├── 06:00-10:00  Possible spawn (Morning)
├── 10:00-14:00  No spawn window
├── 14:00-18:00  Possible spawn (Afternoon)
├── 18:00-22:00  Possible spawn (Evening/Prime)
└── 22:00-00:00  No spawn window

Actual spawn time randomized within windows.
Duration: 2-4 hours once spawned.
```

### Spawn Locations (Penthouse Bar)

The dealer spawns in **hidden or semi-hidden spots**:

| Location | Difficulty to Find | Hint |
|----------|-------------------|------|
| Behind the bar counter | Easy | "Employees only" area |
| Under DJ booth (maintenance) | Medium | Hatch in floor |
| Rooftop edge alcove | Medium | Hidden behind plants |
| Elevator shaft top | Hard | Requires exploration |
| Secret room (if unlocked) | Hard | Housing feature area |

```
SPAWN LOCATION MAP (Penthouse Bar)

    ┌────────────────────────────────────────────────┐
    │                                                │
    │    [3]                              [4]        │  ← Rooftop level
    │   Garden                          Edge         │
    │   Corner                         Alcove        │
    │                                                │
    │    ════════════════════════════════════        │
    │                                                │
    │    ┌──────────────────────────────────┐        │
    │    │                                  │        │
    │    │        [1]              [5]      │        │  ← Main floor
    │    │     Behind Bar       VIP Corner  │        │
    │    │                                  │        │
    │    │              [2]                 │        │
    │    │           Under DJ               │        │
    │    │                                  │        │
    │    └──────────────────────────────────┘        │
    │                                                │
    │                  [6]                           │
    │             Elevator Shaft                     │  ← Below/behind
    │                (rare)                          │
    │                                                │
    └────────────────────────────────────────────────┘

    [1]-[6] = Potential spawn points (one active at a time)
```

---

## Inventory System

### Rotating Deals

The Black Market Dealer's inventory **completely refreshes** each spawn:

| Slot | Contents | Special Feature |
|------|----------|-----------------|
| **Deal 1** | Random Rare item | 20-40% discount |
| **Deal 2** | Random Uncommon item | 30-50% discount |
| **Deal 3** | Lootbox bundle | 3 for price of 2 |
| **Deal 4** | Currency exchange | Favorable rate |
| **Deal 5** | "Mystery Item" | Hidden until purchased |
| **Deal 6** | Black Market Exclusive | Unique cosmetic |

### Deal Types

#### Discounted Items
Regular items at significant discounts.

| Example | Normal Price | Black Market Price |
|---------|--------------|-------------------|
| Rare Jacket | $5,000 | $3,000 (40% off) |
| Epic Hat | 100 Gems | 65 Gems (35% off) |
| Furniture Set | $2,500 | $1,500 (40% off) |

#### Currency Exchange
Better rates than normal conversion.

| Exchange | Normal Rate | Black Market Rate |
|----------|-------------|-------------------|
| Cash → Gems | Not available | $2,000 = 10 Gems |
| Crystals → Gems | Not available | 2 Crystals = 15 Gems |

#### Mystery Items
Purchase reveals what you get.

| Price | Possible Contents |
|-------|-------------------|
| $1,000 | Common-Rare item (weighted toward Uncommon) |
| 50 Gems | Uncommon-Epic item (weighted toward Rare) |
| 5 Crystals | Rare-Legendary item (weighted toward Epic) |

**Pity System:** Mystery items never give something worth less than 80% of purchase price.

#### Black Market Exclusives

Items **only available** from the Black Market Dealer:

| Item Type | Examples | Rotation |
|-----------|----------|----------|
| Titles | "Shadow Shopper", "Back Alley Regular" | Weekly |
| Badges | Black Market themed icons | Weekly |
| Cosmetics | Dark/mysterious variants | Monthly |
| Particles | Subtle shadow effects | Monthly |

**Important:** These are cosmetic-only and don't provide advantages. They're flex items for dedicated hunters.

---

## Shop UI

```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│   ░░░ THE BLACK MARKET ░░░           [X]               │
│                                                         │
│   "These deals disappear in: 2h 34m"                   │
│                                                         │
├─────────────────────────────────────────────────────────┤
│                                                         │
│   TODAY'S DEALS                                         │
│                                                         │
│   ┌───────────────────────────────────────────────┐    │
│   │ ★ Midnight Coat (Rare)                        │    │
│   │   Was: $5,000  NOW: $3,000                    │    │
│   │   ░░░░░░░░░░░░░░░░░░░░░  [BUY]               │    │
│   └───────────────────────────────────────────────┘    │
│                                                         │
│   ┌───────────────────────────────────────────────┐    │
│   │ ◆ Lootbox Bundle                              │    │
│   │   3x Rare Lootboxes for 150 Gems (save 75!)   │    │
│   │   ░░░░░░░░░░░░░░░░░░░░░  [BUY]               │    │
│   └───────────────────────────────────────────────┘    │
│                                                         │
│   ┌───────────────────────────────────────────────┐    │
│   │ ? MYSTERY ITEM                                │    │
│   │   $1,000 - What could it be?                  │    │
│   │   ░░░░░░░░░░░░░░░░░░░░░  [BUY]               │    │
│   └───────────────────────────────────────────────┘    │
│                                                         │
│   ┌───────────────────────────────────────────────┐    │
│   │ ★ EXCLUSIVE: "Shadow Shopper" Title           │    │
│   │   50 Gems - Only here!                        │    │
│   │   ░░░░░░░░░░░░░░░░░░░░░  [BUY]               │    │
│   └───────────────────────────────────────────────┘    │
│                                                         │
│   Your Cash: $4,200  |  Gems: 89  |  Crystals: 3       │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

---

## Discovery Mechanics

### Finding the Dealer

| Method | Description |
|--------|-------------|
| **Exploration** | Checking hidden spots manually |
| **Social** | Other players share location in chat |
| **Sound Cue** | Subtle audio when near (footsteps, whispers) |
| **Visual Cue** | Faint particle effect in area |

### Community Dynamics

The dealer creates organic social moments:
- *"Black Market is up behind the bar!"*
- Players rushing to find the spawn
- Veterans knowing the spawn points
- New players learning from community

---

## Purchase Limits

To prevent exploitation:

| Limit Type | Restriction |
|------------|-------------|
| **Per Item** | 1 of each deal per spawn |
| **Mystery Items** | Max 3 per spawn |
| **Exclusives** | 1 per player per week |

---

## Progression Tie-In

### Black Market Reputation (Future)

| Reputation Level | Purchases Needed | Unlock |
|-----------------|------------------|--------|
| First Timer | 1 | Access to shop |
| Regular | 10 | Better mystery item odds |
| VIP Customer | 25 | Early spawn notification? |
| Shadow Elite | 50 | Exclusive title + badge |

---

## Balance Considerations

### Why This Works

| Aspect | Reasoning |
|--------|-----------|
| **Not Pay-to-Win** | All items are cosmetic or convenience |
| **Fair Discounts** | Rewards exploration, not wallets |
| **Exclusives Are Flex** | Titles/badges show dedication, not power |
| **Mystery Items** | Excitement mechanic with pity protection |

### Potential Issues to Watch

| Risk | Mitigation |
|------|------------|
| Players feel forced to hunt | Deals are nice-to-have, not essential |
| FOMO pressure | Most items return eventually |
| Bots farming spawn | Location randomization, manual spot design |

---

## Implementation Notes

### Phase 1 (Basic)
- [ ] 3 spawn locations in Penthouse Bar
- [ ] 4-5 deal slots
- [ ] Basic rotation system
- [ ] Manual spawn triggering by admin

### Phase 2 (Automated)
- [ ] Automatic spawn scheduling
- [ ] More spawn locations
- [ ] Reputation system
- [ ] Sound/visual cues

### Phase 3 (Expanded)
- [ ] Multiple world locations
- [ ] Special event appearances
- [ ] Unique Black Market events

---

*See [Shop_NPC.md](Shop_NPC.md) for the regular shop comparison.*
*See [../../Systems/Economy_System.md](../../Systems/Economy_System.md) for currency balancing.*
