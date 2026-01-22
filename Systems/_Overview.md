# Systems

**Purpose:** All game mechanics — how players play, earn, spend, and progress.

---

## What's In This Folder

| Document | Description |
|----------|-------------|
| [Economy_System.md](Economy_System.md) | Cash, Gems, Crystals, Lootboxes, trading |
| [Fame_System.md](Fame_System.md) | Social status, decay, tiers, hosting bonuses |
| [Jobs_System.md](Jobs_System.md) | Careers, tasks, minigames, job progression |
| [Housing_System.md](Housing_System.md) | Apartments, parties, furniture, plants |
| [Progression_System.md](Progression_System.md) | XP, levels, milestones, achievements |

---

## The Core Loop

```
PLAY → EARN → SPEND → FLEX → ASPIRE → PLAY

┌─────────────────────────────────────────────────────────┐
│                                                         │
│   ┌─────────┐    ┌─────────┐    ┌─────────┐           │
│   │  PLAY   │───▶│  EARN   │───▶│  SPEND  │           │
│   │         │    │         │    │         │           │
│   │Jobs     │    │Cash     │    │Housing  │           │
│   │Minigames│    │Gems     │    │Lootboxes│           │
│   │Socialize│    │Lootboxes│    │Cosmetics│           │
│   │Idle     │    │Fame     │    │Parties  │           │
│   └─────────┘    └─────────┘    └─────────┘           │
│        ▲                              │                │
│        │                              ▼                │
│   ┌─────────┐                   ┌─────────┐           │
│   │ ASPIRE  │◀──────────────────│  FLEX   │           │
│   │         │                   │         │           │
│   │"I want  │                   │Show off │           │
│   │ that"   │                   │Be seen  │           │
│   └─────────┘                   └─────────┘           │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

---

## System Connections

| System | Purpose | Connects To |
|--------|---------|-------------|
| **Economy** | Resource flow (Cash + Gems + Crystals) | Jobs, Lootboxes, Housing, Trading |
| **Lootboxes** | Primary reward vehicle | Economy, Progression, Fame, Events |
| **Fame** | Social status, hosting power | Parties, Leaderboards, Titles |
| **Jobs** | Active earning, progression | Economy, Fame, Unlocks |
| **Housing** | Personal space, flex | Economy, Fame (parties), Cosmetics |
| **Progression** | Long-term goals, unlocks | All systems |

---

## Currency Overview

| Currency | Role | Earn Rate | Tradeable? |
|----------|------|-----------|------------|
| **Cash ($)** | Common, daily use | Fast | Yes |
| **Gems** | Premium, lootboxes | Medium | No |
| **Crystals** | Economy anchor, parties | Moderate | Yes |

---

## Key Numbers

| Metric | Value |
|--------|-------|
| Level Cap | None (infinite) |
| Housing Tiers | 5 (Studio → Mansion) |
| Fame Tiers | 8 (Newcomer → Legend) |
| Lootbox Tiers | 4 (Common → Legendary) |
| Passive XP | 5 XP/min |
| Cash/Hour Target | $800-1,200 |

---

## Player Journey

### Early Game (Level 1-25)
- Spawn in Central Hub
- Explore, meet players
- Start Entry-level job
- Earn Cash, buy first cosmetics
- Get starter apartment → upgrade to Apartment
- Open first Lootboxes from leveling

### Mid Game (Level 26-60)
- Unlock Skilled jobs
- Upgrade to Loft → Penthouse
- Build Fame, climb ranks
- Host parties
- Trade with other players
- Collect rare items

### Late Game (Level 61+)
- Compete for Fame leaderboard
- Host premium parties
- Collect rare/legendary items
- Max out to Mansion
- Become recognized community member

---

## Key Design Decisions

| Decision | Rationale |
|----------|-----------|
| **Three Currencies** | Cash (everyday), Gems (excitement), Crystals (anchor) |
| **Lootboxes as rewards** | Exciting, variable, drives engagement |
| **No premium gates** | Housing/jobs use Cash only, fair for all |
| **Gentle Fame decay** | Respects casual players and real life |
| **No level cap** | Let grinders grind, high levels are flex |
| **5 XP/min passive** | Simple, universal, always progressing |
| **Crystals tradeable** | Creates player economy, social selling |

---

*Each system document contains complete details and balance numbers.*
