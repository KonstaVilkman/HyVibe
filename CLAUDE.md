# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**HyVibe** is a Hytale social/hangout server project - a cozy MMO-lite where players can relax, roleplay, customize their space, and build meaningful connections.

**Current Phase:** Phase 0 - Pre-Development/Planning
**Core Promise:** A trusted, non-pay-to-win social platform

This repository currently contains game design documentation only. No code or assets exist yet.

## Documentation Structure

| Document | Purpose |
|----------|---------|
| [VISION_DOCUMENT.md](VISION_DOCUMENT.md) | Overall vision, target audience, core pillars, monetization, development phases |
| [Core_Systems_Overview.md](Core_Systems_Overview.md) | High-level view of how all systems connect (the core loop) |
| [Economy_System.md](Economy_System.md) | Currency design, earning/spending flow, trading |
| [Fame_System.md](Fame_System.md) | Social status mechanics, decay system, tier benefits |
| [Jobs_System.md](Jobs_System.md) | Task-based careers, progression, rewards |
| [Housing_System.md](Housing_System.md) | Instanced apartments, furniture, party hosting |
| [Progression_System.md](Progression_System.md) | XP, player levels, milestones, achievements |

## Key Terminology

| Term | Definition |
|------|------------|
| **Cash ($)** | Common currency, fast to earn, tradeable between players |
| **Orbs** | Premium currency, earned through achievements/milestones, NOT tradeable |
| **Anchor [TBD]** | Stable-value item for trading and premium sinks (name pending) |
| **Event Tickets** | Time-limited currency for seasonal events |
| **Fame** | Social status score with daily decay threshold - must earn minimum daily to maintain |
| **Party** | Hosted events in apartments that generate Fame and passive income |
| **The Core Loop** | PLAY → EARN → SPEND → FLEX → ASPIRE → PLAY |

## Development Phases

- **Phase 0 (Current):** Establish vision, learn Hytale tools, create proof-of-concept
- **Phase 1:** Core loop - Hub, housing, one minigame, AFK rewards, basic economy
- **Phase 2:** Expansion - More minigames, roleplay systems, events, monetization
- **Phase 3:** Polish - Onboarding, moderation, community features, launch prep
- **Phase 4:** Live Operations - Content updates, events, growth

## Working with This Project

### Game Design Help
- **Always update existing documents** rather than creating new ones
- Maintain consistency across all interconnected systems
- When adjusting numbers, consider ripple effects on other systems
- All design choices must respect the non-pay-to-win principle
- Mark open questions in documents for future playtesting decisions

### Learning Path (Phase 0 Priorities)
1. Learn Hytale building tools and create small test builds
2. Research Hytale scripting/modding capabilities as they become available
3. Experiment with Hytale Model Maker for custom assets
4. Identify which designed systems are feasible with current Hytale features

### Team Collaboration
Key roles needed (per VISION_DOCUMENT.md):
- **Builder(s):** World building, environmental design (High priority)
- **Scripter/Developer:** Modding, game logic, systems (High priority)
- **3D Modeler:** Custom furniture, items, cosmetics (Medium priority)
- **Pixel/2D Artist:** UI, icons, branding (Medium priority)
- **Community Manager:** Discord, social media (Medium priority)

## Design Constraints

- Hytale is in Early Access - capabilities may be limited
- All monetization must be cosmetic-only (no gameplay advantages)
- Systems should feel rewarding without pressure (cozy, not grindy)
- Target audience: 13+, family-friendly content
