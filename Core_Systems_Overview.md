# Core Systems Overview

**Purpose:** High-level view of how all systems connect.  
**Status:** Concept Phase

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
│   │Minigames│    │Orbs     │    │Cosmetics│           │
│   │Socialize│    │Anchor   │    │Unlocks  │           │
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

## System Map

| System | Purpose | Connects To |
|--------|---------|-------------|
| **Fame** | Social status, hosting power | Parties, Leaderboards, Titles |
| **Economy** | Resource flow, trading | Jobs, Shops, Housing, Sinks |
| **Jobs** | Active earning, progression | Economy, Fame, Unlocks |
| **Housing** | Personal space, flex | Economy, Fame (parties), Cosmetics |
| **Progression** | Long-term goals, unlocks | All systems |

---

## Currency Flow

```
         EARNING                          SPENDING
         
┌─────────────────┐              ┌─────────────────┐
│                 │              │                 │
│  Jobs ─────────▶│              │◀───── Housing   │
│  Minigames ────▶│    CASH      │◀───── Cosmetics │
│  Daily Login ──▶│     ($)      │◀───── Basic     │
│  Selling ──────▶│              │        Items    │
│                 │              │                 │
└─────────────────┘              └─────────────────┘

┌─────────────────┐              ┌─────────────────┐
│                 │              │                 │
│  Achievements ─▶│              │◀───── Premium   │
│  Milestones ───▶│    ORBS      │        Cosmetics│
│  Rare Drops ───▶│              │◀───── Exclusive │
│  Events ───────▶│              │        Items    │
│                 │              │                 │
└─────────────────┘              └─────────────────┘

┌─────────────────┐              ┌─────────────────┐
│                 │              │                 │
│  Jobs ─────────▶│              │◀───── Parties   │
│  Milestones ───▶│   ANCHOR     │◀───── Crafting  │
│  Events ───────▶│    [TBD]     │◀───── VIP Areas │
│  Trading ──────▶│              │◀───── Rerolls   │
│                 │              │◀───── Unlocks   │
└─────────────────┘              └─────────────────┘

┌─────────────────┐              ┌─────────────────┐
│                 │              │                 │
│  Event Tasks ──▶│    EVENT     │◀───── Event     │
│  Participation─▶│   TICKETS    │        Shop     │
│  Challenges ───▶│              │◀───── Limited   │
│                 │              │        Items    │
└─────────────────┘              └─────────────────┘
```

---

## Fame Flow

```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│  EARNING FAME                      FAME BENEFITS        │
│                                                         │
│  ┌─────────────┐                 ┌─────────────┐        │
│  │Host Parties │───────────────▶│ Hosting Bonus│       │
│  │Get Visits   │                 │(% of guest  │       │
│  │Win Games    │                 │ earnings)   │       │
│  │Complete Jobs│                 └─────────────┘       │
│  │Socialize    │                                       │
│  └──────┬──────┘                 ┌─────────────┐       │
│         │                        │Title/Rank   │       │
│         ▼                        │Display      │       │
│  ┌─────────────┐                 └─────────────┘       │
│  │ FAME TOTAL  │────────────────▶                     │
│  └──────┬──────┘                 ┌─────────────┐       │
│         │                        │Leaderboard  │       │
│         │   DECAY                │Position     │       │
│         ▼   (if threshold missed)└─────────────┘       │
│  ┌─────────────┐                                       │
│  │ Threshold   │                 ┌─────────────┐       │
│  │ Check Daily │                 │Exclusive    │       │
│  └─────────────┘                 │Unlocks      │       │
│                                  └─────────────┘       │
└─────────────────────────────────────────────────────────┘
```

---

## Player Journey

### Early Game (Level 1-10)
- Spawn in Rooftop Hub
- Explore, meet players
- Start Entry-level job
- Earn Cash, buy first cosmetics
- Get starter apartment
- Learn systems through play

### Mid Game (Level 11-30)
- Unlock Skilled jobs
- Upgrade apartment
- Start earning Anchor items
- Host first parties
- Build Fame, climb ranks
- Trade with other players

### Late Game (Level 31+)
- Compete for Fame leaderboard
- Host premium parties
- Collect rare items
- Max out housing
- Become known/recognized
- Help shape community

---

## System Documents

| Document | Contents |
|----------|----------|
| [FAME_SYSTEM.md](./FAME_SYSTEM.md) | Fame earning, decay, tiers, incentives |
| [ECONOMY_SYSTEM.md](./ECONOMY_SYSTEM.md) | Currencies, anchor item, sinks, balance |
| [JOBS_SYSTEM.md](./JOBS_SYSTEM.md) | Careers, tasks, progression |
| [HOUSING_SYSTEM.md](./HOUSING_SYSTEM.md) | Apartments, parties, customization |
| [PROGRESSION_SYSTEM.md](./PROGRESSION_SYSTEM.md) | Levels, unlocks, milestones |

---

## Open Questions

| Question | Status |
|----------|--------|
| Anchor item name | TBD — needs to feel special |
| Exact fame decay numbers | Needs playtesting |
| Job task specifics | Depends on Hytale capabilities |
| Trading system depth | Secondary feature, design later |
| Minigame list | Depends on what's fun to build |

---

*This document is the map. Individual system docs have the details.*