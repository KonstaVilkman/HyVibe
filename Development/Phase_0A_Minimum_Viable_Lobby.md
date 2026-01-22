# Phase 0A: Minimum Viable Lobby (ASAP)

**Goal:** Get players into a functional social space as fast as possible to validate the concept and build community.

**Timeline:** 2-3 months from start
**Status:** Not Started
**Last Updated:** January 21, 2026

---

## Quick Answers to Your Questions

### Q: Do I start with building or create the server first?

**Answer: Do BOTH in parallel, but prioritize learning the building tools first.**

| Week 1-2 | Week 3-4 | Week 5+ |
|----------|----------|---------|
| Learn Asset Editor | Build test lobby locally | Set up server |
| Experiment in Creative Mode | Create prefabs | Deploy & test with friends |
| Watch tutorials | Iterate on design | Install plugins |

**Why building first?**
- You can build in Creative Mode without a server
- Learning the tools takes time (platform is 8 days old)
- You need something to deploy before the server matters
- Building reveals what's actually possible in Hytale

### Q: Can I build in my private world and deploy later?

**YES!** This is the recommended workflow:
1. Build in your local Creative Mode world
2. Save builds as **Prefabs** using the Prefab Editor
3. Export and deploy to your server
4. Iterate based on player feedback

### Q: Should I use publicly available mods like LuckPerms?

**YES - Absolutely use existing mods!** Don't reinvent the wheel.

#### Available Now (Verified January 2026):

| Mod | Purpose | Status |
|-----|---------|--------|
| **LuckPerms v5.5.25-beta7** | Permissions (ranks, roles) | Full port, web editor works |
| **TheEconomy** | Shop GUI, MySQL, Cash system | 2,293 downloads |
| **HyVault API** | Economy API (like Vault) | For plugin compatibility |
| **Party System** | 8-player parties, teleport | Good for groups |
| **HomesPlus** | Multiple home teleports | Useful for testing |

#### NOT Available Yet (Need Custom Development):

| Feature | Status | Solution |
|---------|--------|----------|
| Instanced Housing | No plugin exists | Custom Java plugin needed |
| Job System | No plugin exists | Custom Java plugin needed |
| Lootbox System | No plugin exists | Custom Java plugin needed |
| XP/Leveling | No plugin exists | Custom Java plugin needed |
| Fame System | No plugin exists | Custom Java plugin needed |

**This is why we need a Java developer!**

---

## Phase 0A Scope (Simplified)

Given the 8-day-old ecosystem, we're simplifying Phase 0A to what's actually achievable:

### Must Have (MVP)
- [ ] Small lobby plaza (one zone)
- [ ] Basic spawn point
- [ ] Chat functionality (built-in)
- [ ] Player profiles (name display)
- [ ] LuckPerms for basic ranks
- [ ] TheEconomy for Cash system
- [ ] Simple level display (custom plugin)

### Should Have (If Time Permits)
- [ ] Fame display (custom plugin)
- [ ] NPC shopkeepers
- [ ] Basic furniture/decoration
- [ ] Parkour course (one simple track)

### Deferred to Phase 0B
- Instanced housing
- Full job system
- Lootboxes
- Gem currency
- Complex minigames

---

## Technical Setup Guide

### Server Requirements

```
Java: 25 (required)
Protocol: QUIC over UDP
Port: 5520 (default)
RAM: 4GB minimum recommended
```

### Hosting Options

| Option | Cost | Pros | Cons |
|--------|------|------|------|
| **Self-hosted** | Free | Full control | Requires technical skill |
| **Aternos** | Free | Easy setup | Limited resources, ads |
| **Shockbyte** | ~$5/mo | Reliable, panels | Monthly cost |
| **Apex Hosting** | ~$7/mo | Good support | Monthly cost |

**Recommendation:** Start self-hosted for development, consider paid hosting for public testing.

### Server Setup Steps

1. **Install Java 25**
   - Download from Oracle or Adoptium
   - Verify: `java -version`

2. **Download Hytale Server**
   - Get from official Hytale sources
   - Extract to dedicated folder

3. **Configure Server**
   - Edit `server.properties`
   - Set port, max players, world settings

4. **Port Forward**
   - UDP port 5520 in router
   - Or use tunneling (playit.gg, ngrok)

5. **Install Plugins**
   ```
   /plugins/
   ├── LuckPerms-Hytale-5.5.25.jar
   ├── TheEconomy.jar
   └── HyVault.jar
   ```

6. **Configure LuckPerms**
   - Use web editor: `lp editor`
   - Create ranks: Guest, Member, VIP, Staff, Admin

---

## Building Workflow

### Tools You'll Use

| Tool | Purpose | Learning Time |
|------|---------|---------------|
| **Asset Editor** | Create blocks, items, NPCs | 1-2 weeks |
| **Prefab Editor** | Save reusable structures | 2-3 days |
| **Visual Node Editor** | Procedural terrain (optional) | 1 week |
| **Creative Mode** | Free building | Immediate |

### Recommended Learning Path

**Week 1: Foundations**
- [ ] Play Hytale normally (understand the game)
- [ ] Explore Creative Mode
- [ ] Watch official tutorials
- [ ] Join Hytale Discord for tips

**Week 2: Asset Editor**
- [ ] Create a simple custom block
- [ ] Create a basic NPC
- [ ] Understand the asset pipeline
- [ ] Make a simple prefab

**Week 3-4: Build the Lobby**
- [ ] Design lobby layout on paper first
- [ ] Block out main areas
- [ ] Add decorations
- [ ] Test player flow
- [ ] Create spawn point

### Lobby Design: Penthouse Bar

**Concept:** High-end indoor lounge with rooftop access. Later becomes an exclusive area accessible from the main city below.

```
    ┌─────────────────────────────────────┐
    │           ROOFTOP DECK              │
    │   [Lounge Chairs]  [Overlook/Rail]  │
    │        [Outdoor Seating]            │
    └──────────────┬──────────────────────┘
                   │ stairs/elevator
    ┌──────────────┴──────────────────────┐
    │            PENTHOUSE                │
    │                                     │
    │  [VIP Corner]     [Dance Floor]     │
    │      (roped)      (DJ booth later)  │
    │                                     │
    │  [Lounge Area]    [Main Bar]        │
    │   (couches)       (stools, NPC)     │
    │                   [SPAWN]           │
    │                                     │
    │        [Elevator to City]           │
    │         (future connection)         │
    └─────────────────────────────────────┘
```

**Zones:**
| Zone | Description |
|------|-------------|
| **Main Bar** | Spawn area, counter, stools, bartender NPC |
| **Lounge Area** | Couches, coffee tables, warm lighting |
| **Dance Floor** | Open space, future DJ booth, mood lighting |
| **VIP Section** | Roped corner (later: fame-gated) |
| **Rooftop Deck** | Open air terrace, city skyline views |
| **Outdoor Seating** | Lounge chairs, small tables |
| **Overlook** | Railing for taking in the view |

**Vibe:** Modern penthouse - warm wood, ambient lighting, leather seating, neon accents. Rooftop has night city aesthetic with neon glow from below.

---

## Development Checklist

### Phase 0A Milestones

#### Milestone 1: Learning (Week 1-2)
- [ ] Purchase Hytale ($19.99)
- [ ] Complete tutorial/early game
- [ ] Learn Creative Mode basics
- [ ] Open Asset Editor, watch tutorials
- [ ] Create first test prefab
- [ ] Join Hytale Discord communities

#### Milestone 2: Building (Week 3-4)
- [ ] Design lobby on paper
- [ ] Build lobby in Creative Mode
- [ ] Add basic decorations
- [ ] Create NPC placeholders
- [ ] Save as prefab

#### Milestone 3: Server Setup (Week 5)
- [ ] Install Java 25
- [ ] Set up local test server
- [ ] Install LuckPerms + TheEconomy
- [ ] Configure basic permissions
- [ ] Deploy lobby build
- [ ] Test with alt account

#### Milestone 4: Custom Systems (Week 6-8)
- [ ] Find/hire Java developer
- [ ] Specify XP/Level system requirements
- [ ] Specify Fame system requirements
- [ ] Develop custom plugins
- [ ] Test integration

#### Milestone 5: Soft Launch (Week 9-10)
- [ ] Invite 5-10 trusted players
- [ ] Gather feedback
- [ ] Fix critical bugs
- [ ] Iterate on design
- [ ] Document issues

---

## Team Needs for Phase 0A

### Solo Tasks (You're Doing)
- Learn Hytale tools (8 days playtime, made Monster Energy mod)
- Design documents (complete)
- Build lobby (starting sketches)
- Basic server setup
- Community management (Discord server in progress)
- Custom Java plugins (learning - confident to self-develop)

### Optional Help
| Role | Priority | Task | Notes |
|------|----------|------|-------|
| **Builder** | MEDIUM | Help with detailed builds | Nice to have |
| **QA Tester** | LOW | Friends/community volunteers | Free |

### Where to Find Help (If Needed)
- **Hytale Discord** - Community builders/devs
- **CurseForge Forums** - Plugin developers
- **r/Hytale** - Community connections

---

## Risk Mitigation

### Platform Risks (Hytale is 8 days old)

| Risk | Likelihood | Mitigation |
|------|------------|------------|
| Breaking API changes | HIGH | Keep plugins simple, expect rewrites |
| Limited documentation | HIGH | Join Discord, experiment, ask questions |
| Bugs in tools | MEDIUM | Report bugs, find workarounds |
| Missing features | MEDIUM | Adjust scope, wait for updates |

### Project Risks

| Risk | Likelihood | Mitigation |
|------|------------|------------|
| Can't find developer | MEDIUM | Start looking NOW, have backup options |
| Scope creep | HIGH | Stick to this document strictly |
| Burnout | MEDIUM | Set realistic goals, take breaks |
| No players | LOW | Start Discord community early |

---

## Budget Estimate

### Your Budget (Self-Developing)

| Item | Cost | Notes |
|------|------|-------|
| Hytale game | $20 | Already owned |
| Hosting (first 3 months) | $0-45 | Free start (Aternos), paid later |
| Domain (optional) | $12/year | For website/branding |
| Discord Nitro (optional) | $30 | Server boosts |
| **Total** | **$0-87** | Minimal since you're coding yourself |

---

## Success Criteria for Phase 0A

### Minimum Success
- [ ] Lobby is playable
- [ ] 5+ concurrent players without crashes
- [ ] Basic economy works
- [ ] Players can see their level
- [ ] Positive feedback from testers

### Ideal Success
- [ ] 10+ concurrent players stable
- [ ] Fame system functional
- [ ] Discord community of 50+ members
- [ ] Players asking "when can we do more?"
- [ ] Clear feedback on what to build next

---

## Next Steps (Start Today)

1. **Buy Hytale** if you haven't ($19.99)
2. **Play the game** for a few hours
3. **Join Hytale Discord** communities
4. **Start sketching** lobby design on paper
5. **Create HyVibe Discord** server for future community
6. **Begin looking** for Java developer

---

## Related Documents

- [Development_Path.md](Development_Path.md) - Overall roadmap
- [../Systems/_Overview.md](../Systems/_Overview.md) - How systems connect
- [../Systems/Economy_System.md](../Systems/Economy_System.md) - Cash/Gems/Lootbox details
- [../Systems/Fame_System.md](../Systems/Fame_System.md) - Fame tier specifics
- [../Systems/Progression_System.md](../Systems/Progression_System.md) - XP and leveling

---

*Phase 0A is about proving the concept works. Keep it simple, get players in, and iterate based on real feedback.*
