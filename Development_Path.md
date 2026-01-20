# Development Path

**Purpose:** Clear roadmap from current state to playable server.
**Strategy:** Community-first - get players in early, expand features over time.
**Last Updated:** January 2026

---

## Philosophy: Build Community First

**Don't wait until everything is perfect.** Get a basic lobby working, invite people, and grow the community while building features.

**Why this works:**
- Early feedback shapes development
- Community grows alongside the server
- Players feel invested in the project
- You stay motivated seeing real people enjoy it

---

## Current State

**You have:**
- [x] Complete game design documentation
- [x] Coherent economy system designed
- [x] All systems planned and balanced

**You need:**
- [ ] Basic Hytale building skills
- [ ] A functional lobby (even simple)
- [ ] Discord community
- [ ] First few players to hang out with

---

## Phase 0A: Minimum Viable Lobby (ASAP)

**Goal:** Something playable to invite people to.

### Spawn Area: Penthouse Bar

**The first area is a penthouse bar** - a high-end indoor lounge with rooftop access. This will later become an exclusive area accessible from the main city below.

**Penthouse Zones (Indoor):**

| Zone | Description |
|------|-------------|
| **Main Bar** | Central gathering spot, stools, bartender NPC |
| **Lounge Area** | Couches, coffee tables, warm lighting |
| **Dance Floor** | Open space, future DJ booth, mood lighting |
| **VIP Section** | Roped off corner (later: fame-gated) |
| **Elevator/Stairs** | Access point (later: connects to city) |

**Rooftop Access (Outdoor):**

| Zone | Description |
|------|-------------|
| **Rooftop Deck** | Open air terrace with city skyline views |
| **Outdoor Seating** | Lounge chairs, small tables |
| **Overlook** | Railing area for taking in the view |

**Vibe:** Modern penthouse interior - warm wood, ambient lighting, leather seating. Rooftop is open air with night city aesthetic, neon glow from below.

### What You're Building

| Feature | Description | Priority |
|---------|-------------|----------|
| **Rooftop Bar** | Spawn area with multiple zones | Must have |
| **Levels** | XP gain (5/min passive) | Must have |
| **Basic Profiles** | Click player → see name, level, fame | Must have |
| **Basic Fame** | Foundation system (earning, display) | Must have |
| **Chat** | Players can talk | Must have |

**NOT building yet:**
- Housing, Jobs, Lootboxes, Complex economy, Minigames
- Fame decay (comes later)
- Full fame tiers (comes later)

### Why Start This Simple?

1. **Faster to build** - Get something live in weeks, not months
2. **Community first** - People can hang out and chat
3. **Test core feel** - Does the rooftop feel right?
4. **Gather feedback** - What do players actually want?

---

## Phase 0A Roadmap (Weeks 1-4)

### Week 1: Learn + Plan

| Day | Task |
|-----|------|
| 1-2 | Install Hytale, explore the game |
| 3-4 | Watch building tutorials, experiment |
| 5-7 | Sketch rooftop bar layout (paper or digital) |

**Create Discord server now** - Start inviting people interested in the concept.

### Week 2: Build Rooftop Bar

| Zone | Details |
|------|---------|
| Main structure | Rooftop footprint, railings, skyline backdrop |
| Bar area | Counter, stools, shelving, bartender spot |
| Lounge | Couches, low tables, ambient lighting |
| Outdoor deck | Open section, city view, plants |
| Dance floor | Open space, lighting for later DJ booth |
| VIP corner | Roped area (decorative for now) |

**Vibe check:** Neon accents, warm lighting, modern furniture, night sky.

### Week 3: Basic Systems

| System | Implementation |
|--------|---------------|
| **Levels** | Track XP, display in profile |
| **Passive XP** | 5 XP per minute online |
| **Fame** | Simple number (+1 per 10 min, +5 daily) |
| **Profiles** | Click player → name, level, fame |

### Week 4: Test + Invite

| Task | Details |
|------|---------|
| Test with 2-3 friends | Walk around, check vibe, find bugs |
| Polish based on feedback | Lighting? Layout? Missing spots? |
| Invite Discord members | Start with 10-20 people |
| Gather feedback | Does it feel like a place to hang? |

---

## Basic Profile System (Phase 0A)

**What players see when clicking another player:**

```
┌─────────────────────────┐
│  PlayerName             │
│  Level: 12              │
│  Fame: 47               │
│                         │
│  [Add Friend] [Block]   │
└─────────────────────────┘
```

**That's it.** Fame is just a number for now. Bio, titles, tiers, cosmetics come later.

---

## Basic Fame System (Phase 0A)

**Foundation only - building the skeleton for later expansion.**

### What We're Building

| Component | Phase 0A | Full System (Later) |
|-----------|----------|---------------------|
| Fame score | ✓ Just a number | Tiers, titles, icons |
| Earning | ✓ Time online, login | Parties, visits, jobs |
| Display | ✓ Show in profile | Leaderboards, badges |
| Decay | ✗ Not yet | Gentle threshold decay |
| Benefits | ✗ Not yet | Hosting bonus, unlocks |

### Fame Earning (Phase 0A)

| Action | Fame | Notes |
|--------|------|-------|
| Per 10 minutes online | +1 | Passive earning |
| Daily login | +5 | Show up bonus |
| First time visiting rooftop | +10 | One-time welcome |

**That's it.** No complex earning yet. Just get the number working.

### Fame Display (Phase 0A)

Show fame as a simple number in profile:

```
┌─────────────────────────┐
│  PlayerName             │
│  Level: 12              │
│  Fame: 47               │
└─────────────────────────┘
```

**Later (Phase 1):** Add tier names (Newcomer, Local, Known, etc.), icons, and leaderboards.

### Why Foundation Only?

- Get the data structure right
- Test if players care about the number
- Easy to expand later
- No decay = no frustrated players early on

---

## Basic Leveling (Phase 0A)

**Simple XP system:**
- 5 XP per minute online
- 200 XP daily login bonus
- No cap - grind forever

**Display:** Level shows next to name or in profile.

**Full progression (milestones, lootboxes, achievements) comes later.**

---

## Phase 0B: First Expansion

**After basic lobby is live and you have 20-50 regular players:**

### Add One Activity

Pick ONE thing to add:
- **Option A:** Simple parkour course (race to finish, leaderboard)
- **Option B:** Fishing spot (cast, wait, catch, sell)
- **Option C:** Social minigame (hide & seek, trivia)

**Why one thing?** Test if players engage. Iterate based on feedback.

### Add Basic Economy

- Cash display
- Earn from activity
- Simple shop (buy furniture or cosmetics)

---

## Phase 1: Core Loop (After Community Established)

**When you have 50-100 regular players, expand to:**

- [ ] Housing (Studio apartments)
- [ ] One full job (Delivery)
- [ ] Full fame system
- [ ] Basic lootboxes
- [ ] More detailed profiles

---

## Community Building Strategy

### Discord Setup

| Channel | Purpose |
|---------|---------|
| #announcements | Updates, server news |
| #general | Chat, hanging out |
| #suggestions | Player ideas |
| #screenshots | Share cool moments |
| #looking-for-friends | Meet people |

### Growing Community

| Week | Goal | How |
|------|------|-----|
| 1-2 | 50 members | Friends, Hytale communities |
| 3-4 | 100 members | Post updates, share progress |
| 5-8 | 200 members | Word of mouth, content |
| 9-12 | 500 members | Early players invite friends |

### Content to Share

- Build progress screenshots
- Design doc snippets
- "Coming soon" teasers
- Behind-the-scenes decisions
- Polls ("What should we name the café?")

---

## Timeline (Realistic)

| Phase | Duration | Outcome |
|-------|----------|---------|
| 0A | 3-4 weeks | Basic lobby live, 20-50 players |
| 0B | 2-3 weeks | One activity, basic economy |
| 1 | 6-8 weeks | Housing, job, fame, lootboxes |
| 2 | 8-12 weeks | Full systems, beta ready |
| 3 | 4-6 weeks | Polish, launch |

**Total to beta:** ~6 months
**Total to launch:** ~8-10 months

---

## Decision Points

### Before Building Rooftop:
1. **Server name** - Pick one and commit
2. **Rooftop style** - Full neon? Warm wood accents? Mix?
3. **City backdrop** - What does the skyline look like?
4. **Time of day** - Permanent night? Day/night cycle?

### After First Players:
1. **Where do they hang?** - Bar? Lounge? Deck?
2. **What do they ask for?** - More seating? Music? Activities?
3. **Does it feel right?** - Cozy? Too empty? Too crowded?

---

## This Week's Actions

1. [ ] Create Discord server
2. [ ] Post in Hytale communities about the concept
3. [ ] Install Hytale and experiment with building
4. [ ] Sketch rooftop bar layout (zones, furniture placement)
5. [ ] Watch building tutorials (focus on interior/modern builds)
6. [ ] Decide on server name
7. [ ] Find reference images for rooftop bar vibe

---

## Minimum Launch Checklist (Phase 0A)

Before inviting first players:

- [ ] Players spawn on rooftop bar
- [ ] Players can walk around all zones
- [ ] Players can chat
- [ ] Level system works (5 XP/min passive)
- [ ] Fame system works (+1 per 10 min, +5 daily login)
- [ ] Clicking player shows profile (name, level, fame)
- [ ] Bar, lounge, deck areas feel complete
- [ ] Lighting and vibe feel right
- [ ] No game-breaking bugs

**That's it.** City, housing, jobs, full fame system - all wait.

---

*Start simple. Build community. Expand based on what players actually want.*
