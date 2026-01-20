# Core Systems Overview

**Purpose:** High-level view of how all systems connect.
**Status:** Concept Phase
**Last Updated:** January 2026

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

## System Map

| System | Purpose | Connects To |
|--------|---------|-------------|
| **Economy** | Resource flow (Cash + Gems) | Jobs, Lootboxes, Housing, Trading |
| **Lootboxes** | Primary reward vehicle | Economy, Progression, Fame, Events |
| **Fame** | Social status, hosting power | Parties, Leaderboards, Titles |
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
│  Daily Login ──▶│     ($)      │◀───── Parties   │
│  Trading ──────▶│              │◀───── Trading   │
│  Lootboxes ────▶│              │                 │
│                 │              │                 │
└─────────────────┘              └─────────────────┘

┌─────────────────┐              ┌─────────────────┐
│                 │              │                 │
│  Level Ups ────▶│              │◀───── Common    │
│  Achievements ─▶│    GEMS      │        Lootbox  │
│  Daily Login ──▶│              │◀───── Rare      │
│  Fame Tiers ───▶│              │        Lootbox  │
│  Events ───────▶│              │◀───── Epic/     │
│                 │              │        Legendary│
└─────────────────┘              └─────────────────┘

┌─────────────────┐              ┌─────────────────┐
│                 │              │                 │
│  Level Ups ────▶│              │◀───── Cosmetics │
│  Achievements ─▶│  LOOTBOXES   │◀───── Furniture │
│  Fame Tiers ───▶│              │◀───── Pets      │
│  Challenges ───▶│              │◀───── Currency  │
│  Events ───────▶│              │◀───── Materials │
│                 │              │                 │
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
│  │Daily Login  │                                       │
│  └──────┬──────┘                 ┌─────────────┐       │
│         │                        │Title/Rank   │       │
│         ▼                        │Display      │       │
│  ┌─────────────┐                 └─────────────┘       │
│  │ FAME TOTAL  │────────────────▶                     │
│  └──────┬──────┘                 ┌─────────────┐       │
│         │                        │Leaderboard  │       │
│         │   GENTLE DECAY         │Position     │       │
│         ▼   (grace period)       └─────────────┘       │
│  ┌─────────────┐                                       │
│  │ Threshold   │                 ┌─────────────┐       │
│  │ Check Daily │                 │Tier Rewards │       │
│  └─────────────┘                 │(Lootboxes!) │       │
│                                  └─────────────┘       │
└─────────────────────────────────────────────────────────┘
```

---

## Player Journey

### Early Game (Level 1-25)
- Spawn in Central Hub
- Explore, meet players
- Start Entry-level job
- Earn Cash, buy first cosmetics
- Get starter apartment → upgrade to Apartment
- Open first Lootboxes from leveling
- Learn systems through play

### Mid Game (Level 26-60)
- Unlock Skilled jobs
- Upgrade to Loft → Penthouse
- Build Fame, climb ranks
- Host parties
- Trade with other players
- Open better Lootboxes, collect rare items

### Late Game (Level 61-100)
- Compete for Fame leaderboard
- Host premium parties
- Collect rare/legendary items
- Max out to Mansion housing
- Become known/recognized
- Help shape community

---

## System Documents

| Document | Contents |
|----------|----------|
| [Economy_System.md](./Economy_System.md) | Currencies (Cash, Gems), Lootboxes, trading |
| [Fame_System.md](./Fame_System.md) | Fame earning, gentle decay, tiers, rewards |
| [Jobs_System.md](./Jobs_System.md) | Careers, tasks, minigames, progression |
| [Housing_System.md](./Housing_System.md) | Apartments, parties, furniture, customization |
| [Progression_System.md](./Progression_System.md) | Levels, unlocks, milestones, achievements |

---

## Key Design Decisions

| Decision | Rationale |
|----------|-----------|
| **Dual Currency (Cash + Gems)** | Simple, familiar, no confusion |
| **Lootboxes as primary rewards** | Exciting, variable, drives engagement |
| **No premium currency gates** | Housing/jobs use Cash only, fair for all |
| **Gentle Fame decay** | Respects casual players and real life |
| **Level cap at 100** | Achievable goal, prestigious to reach |
| **Cash-only housing** | Everyone can progress, no P2W feel |

---

## Progression Alignment

All systems now use consistent level requirements:

| Level | Housing Unlock | Job Unlock | Fame Tier |
|-------|---------------|------------|-----------|
| 1 | Studio (free) | All Entry jobs | Newcomer |
| 10 | Apartment ($3K) | — | Local |
| 25 | Loft ($10K) | — | Known |
| 40 | Penthouse ($30K) | — | Popular |
| 60 | Mansion ($75K) | — | Celebrity |
| — | — | — | Star (Fame-based) |
| — | — | — | Icon (Fame-based) |
| — | — | — | Legend (Fame-based) |

---

## Open Questions

| Question | Status |
|----------|--------|
| Final lootbox drop rates | Needs playtesting |
| Event system details | Design later |
| Minigame specifics | Depends on Hytale capabilities |
| Trading system depth | Secondary feature |
| Live events/concerts | Phase 2+ feature |

---

*This document is the map. Individual system docs have the details.*
