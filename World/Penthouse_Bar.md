# Penthouse Bar

**Purpose:** Main social hub and spawn location for HyVibe.
**Status:** Design Phase
**Phase:** 0A (Minimum Viable Lobby)

---

## Overview

The Penthouse Bar is a rooftop social venue that serves as the **primary spawn point** for all players. It's designed to feel exclusive yet welcoming — a place where players naturally gather, socialize, and discover the server's features.

**Design Goals:**
- Immediate "wow" moment upon arrival
- Clear navigation to key areas
- Natural gathering spots
- Vertical progression feeling (you're at the top)

---

## Visual Layout

### Floor Plan (Top-Down View)

```
                              NORTH (City View)
    ┌─────────────────────────────────────────────────────────────────┐
    │                                                                 │
    │    ┌─────────────┐                         ┌─────────────┐      │
    │    │   ROOFTOP   │                         │   ROOFTOP   │      │
    │    │   GARDEN    │                         │   LOUNGE    │      │
    │    │  (plants)   │                         │  (seating)  │      │
    │    └──────┬──────┘                         └──────┬──────┘      │
    │           │              TERRACE                  │             │
    │    ───────┴──────────────────────────────────────┴───────      │
    │                    [ OUTDOOR SEATING ]                          │
    │                         [ DJ BOOTH ]                            │
W   │    ═══════════════════════════════════════════════════════     │   E
E   │                                                                 │   A
S   │    ┌─────────────────────────────────────────────────────┐     │   S
T   │    │                                                     │     │   T
    │    │                    MAIN BAR                         │     │
    │    │     ┌─────┐                           ┌─────┐       │     │
    │    │     │SHOP │                           │ VIP │       │     │
    │    │     │ NPC │      [ BAR COUNTER ]      │AREA │       │     │
    │    │     └─────┘           |||             └─────┘       │     │
    │    │                       |||                           │     │
    │    │    [ TABLES ]    [ DANCE FLOOR ]    [ TABLES ]      │     │
    │    │       oo              :::              oo           │     │
    │    │       oo              :::              oo           │     │
    │    │                       :::                           │     │
    │    │    ┌────────┐         :::         ┌────────┐        │     │
    │    │    │ARCADE  │                     │JUKEBOX │        │     │
    │    │    │CORNER  │                     │ AREA   │        │     │
    │    │    └────────┘                     └────────┘        │     │
    │    │                                                     │     │
    │    └─────────────────────────┬───────────────────────────┘     │
    │                              │                                  │
    │                     ┌────────┴────────┐                        │
    │                     │                 │                        │
    │                     │    ELEVATOR     │                        │
    │                     │     LOBBY       │                        │
    │                     │   [SPAWN]       │                        │
    │                     │    ┌───┐        │                        │
    │                     │    │ E │ ← Elevator Doors                │
    │                     │    └───┘        │                        │
    │                     │                 │                        │
    │                     └─────────────────┘                        │
    │                                                                 │
    └─────────────────────────────────────────────────────────────────┘
                              SOUTH (Elevator Access)
```

### Side View (East-West Cross Section)

```
    ┌──────────────────────────────────────────────────────────────┐
    │  ☆ ☆ ☆  NIGHT SKY / CITY LIGHTS  ☆ ☆ ☆                      │
    ├──────────────────────────────────────────────────────────────┤
    │                                                              │
    │         ┌─────┐                    ┌─────┐                   │
    │         │PLANT│    TERRACE         │LNGE │                   │  ← Rooftop Level
    │         └──┬──┘    RAILING         └──┬──┘                   │    (Open Air)
    │    ════════╪══════════════════════════╪═════════             │
    │            │                          │                      │
    │    ┌───────┴──────────────────────────┴──────────────┐       │
    │    │                                                 │       │  ← Main Floor
    │    │   SHOP    BAR COUNTER    DANCE    VIP          │       │    (Interior)
    │    │    []        ▓▓▓▓▓        :::     []           │       │
    │    │                                                 │       │
    │    └────────────────────┬────────────────────────────┘       │
    │                         │                                    │
    │                    ┌────┴────┐                               │
    │                    │ELEVATOR │                               │  ← Elevator Lobby
    │                    │  ████   │                               │    (Spawn Point)
    │                    └────┬────┘                               │
    │                         │                                    │
    │                         ▼                                    │
    │                    (Building Below)                          │
    └──────────────────────────────────────────────────────────────┘
```

---

## Zones & Spaces

### Interior Spaces

| Zone | Size | Purpose | Key Features |
|------|------|---------|--------------|
| **Elevator Lobby** | Small | Spawn point | Elevator doors, welcome signage, direction indicators |
| **Main Bar** | Large | Primary social area | Bar counter, seating, ambient lighting |
| **Dance Floor** | Medium | Active social area | Open space, lighting effects, center stage |
| **Shop Area** | Small | NPC commerce | Shop NPC, item displays, purchase UI |
| **VIP Area** | Small | Aspirational space | Velvet ropes, exclusive seating (Fame-gated?) |
| **Arcade Corner** | Small | Future minigames | Placeholder machines, coming soon signage |
| **Jukebox Area** | Small | Music/ambiance | Jukebox prop, seating nook |

### Exterior Spaces

| Zone | Size | Purpose | Key Features |
|------|------|---------|--------------|
| **Terrace** | Large | Outdoor social | City views, outdoor seating, ambient lights |
| **DJ Booth** | Small | Event focal point | Elevated platform, speaker props |
| **Rooftop Garden** | Medium | Peaceful corner | Plants, benches, quiet atmosphere |
| **Rooftop Lounge** | Medium | Premium seating | Couches, fire pit, premium feel |

---

## Spawn System (Elevator)

### Player Entry Flow

```
Player Joins Server
        │
        ▼
┌───────────────────┐
│  Loading Screen   │
│  (Elevator going  │
│      up...)       │
└─────────┬─────────┘
          │
          ▼
┌───────────────────┐
│  Elevator Doors   │
│      Open         │
│   *ding sound*    │
└─────────┬─────────┘
          │
          ▼
┌───────────────────┐
│  Player Steps     │
│   Into Lobby      │
│  (First View)     │
└───────────────────┘
```

### Spawn Point Details

| Aspect | Design |
|--------|--------|
| **Location** | Center of Elevator Lobby |
| **Facing** | North (toward Main Bar entrance) |
| **First View** | Bar entrance with ambient lighting visible |
| **Audio** | Elevator ding, muffled music from bar |
| **Signage** | "Welcome to HyVibe" + directional hints |

### Elevator Lobby Layout

```
        ┌─────────────────────────────┐
        │                             │
        │     → TO MAIN BAR →         │
        │                             │
        │   ┌─────┐       ┌─────┐     │
        │   │SIGN │       │SIGN │     │
        │   │Info │       │Map? │     │
        │   └─────┘       └─────┘     │
        │                             │
        │         [SPAWN]             │
        │            X                │
        │                             │
        │      ┌───────────┐          │
        │      │ ELEVATOR  │          │
        │      │   DOORS   │          │
        │      │    ██     │          │
        │      └───────────┘          │
        │                             │
        └─────────────────────────────┘
```

---

## Key Sightlines

When sketching, ensure these views work:

| From | Looking At | Should See |
|------|-----------|------------|
| Spawn point | North | Bar entrance, warm lighting, activity |
| Bar entrance | Dance floor | Open space, other players, energy |
| Dance floor | Bar counter | NPC location, purchase area |
| Terrace entrance | Outside | City skyline, night sky, premium feel |
| Any corner | Center | Dance floor always visible |

---

## Atmosphere & Mood

### Lighting

| Area | Lighting Style |
|------|----------------|
| Elevator Lobby | Neutral, transitional |
| Main Bar | Warm amber, intimate |
| Dance Floor | Dynamic, colorful accents |
| Terrace | Cool night tones, city glow |
| VIP Area | Purple/gold accent lighting |

### Audio Zones

| Zone | Sound |
|------|-------|
| Elevator | Muffled bass, anticipation |
| Main Bar | Full music, ambient chatter |
| Terrace | Softer music, city ambiance |
| Garden | Quiet, nature sounds |

---

## NPC Placements

| NPC | Location | Purpose |
|-----|----------|---------|
| **Shop NPC** | Shop Area (Main Bar) | General item shop |
| **Bartender** | Behind Bar Counter | Flavor/social (non-functional for now) |
| **Black Market Dealer** | Random (see NPCs folder) | Secret rotating deals |

---

## Secret Spots

Potential hidden areas for exploration:

| Secret | Location Hint | Reward/Purpose |
|--------|---------------|----------------|
| Behind the bar | Employees only door | Easter egg, maybe Black Market spawn |
| Rooftop edge | Hidden ladder/path | Secret viewpoint |
| Under the DJ booth | Maintenance hatch | Black Market spawn location |

---

## Build Priority (Phase 0A)

### Must Have
- [ ] Elevator Lobby (spawn functional)
- [ ] Main Bar shell (walls, floor, ceiling)
- [ ] Basic lighting
- [ ] Shop NPC placement spot

### Nice to Have
- [ ] Dance floor markings
- [ ] Terrace access
- [ ] Bar counter props

### Later Phases
- [ ] VIP area (Fame-gated)
- [ ] Arcade machines (functional)
- [ ] Full terrace decoration
- [ ] Rooftop areas

---

## Technical Notes

- Spawn point coordinates: TBD after build
- Keep main floor relatively flat for navigation
- Test player density in dance floor area
- Ensure clear pathways (no collision traps)

---

*See [NPCs/_Overview.md](NPCs/_Overview.md) for NPC details.*
*See [../Development/Phase_0A_Minimum_Viable_Lobby.md](../Development/Phase_0A_Minimum_Viable_Lobby.md) for build timeline.*
