# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**HyVibe** is a Hytale social/hangout server project - a cozy MMO-lite where players can relax, roleplay, customize their space, and build meaningful connections.

**Current Phase:** Phase 0 - Foundation (Design Complete, Learning Hytale)
**Core Promise:** A trusted, non-pay-to-win social platform

This repository contains complete game design documentation. No code or assets exist yet.

## Economy Model

**Dual Currency + Lootboxes:**

| Currency | Role | Tradeable? |
|----------|------|------------|
| **Cash ($)** | Common currency for everyday purchases | Yes |
| **Gems** | Premium currency for lootboxes | No |
| **Lootboxes** | Primary reward vehicle (cosmetics, furniture, pets) | No |

**Key Design Decision:** Housing and job unlocks use Cash only. No premium currency gates.

## Documentation Structure

| Document | Purpose |
|----------|---------|
| [VISION_DOCUMENT.md](VISION_DOCUMENT.md) | Overall vision, target audience, core pillars, monetization |
| [Development_Path.md](Development_Path.md) | Roadmap from current state to launch |
| [Core_Systems_Overview.md](Core_Systems_Overview.md) | How all systems connect (the core loop) |
| [Economy_System.md](Economy_System.md) | Cash, Gems, Lootboxes, trading |
| [Fame_System.md](Fame_System.md) | Social status with gentle decay |
| [Jobs_System.md](Jobs_System.md) | Task-based careers, minigames |
| [Housing_System.md](Housing_System.md) | Instanced apartments, furniture, parties |
| [Progression_System.md](Progression_System.md) | XP, levels 1-100, milestones |

## Key Numbers (Quick Reference)

| Metric | Value |
|--------|-------|
| Level Cap | **None** (infinite) |
| Housing Tiers | 5 (Studio → Mansion) |
| Fame Tiers | 8 (Newcomer → Legend) |
| Lootbox Tiers | 4 (Common → Legendary) |
| Passive XP | 5 XP/min (universal) |
| Daily Login Fame | +10 |
| Cash/Hour Target | $800-1,200 |

## Development Phases

**Strategy:** Community-first. Get players in early with minimal features, expand based on feedback.

- **Phase 0A (Current):** Basic lobby with levels, fame, profiles - invite first players
- **Phase 0B:** Add one activity (parkour/fishing), basic economy
- **Phase 1:** Core loop - Housing, one job, full fame, lootboxes
- **Phase 2:** Expansion - Full jobs, minigames, housing tiers
- **Phase 3:** Polish - Onboarding, moderation, achievements, launch prep
- **Phase 4:** Live Operations - Content updates, events, growth

## Working with This Project

### Game Design Help
- **Always update existing documents** rather than creating new ones
- Maintain consistency across all interconnected systems
- When adjusting numbers, consider ripple effects on other systems
- All design choices must respect the non-pay-to-win principle
- Reference specific documents for detailed numbers

### Balance Principles
- Cash is easy to earn, used for housing and basics
- Gems are slower to earn, used for lootboxes
- Lootboxes are the excitement mechanic
- Fame decay is gentle (2-day grace period)
- All content achievable through gameplay

### Learning Path (Phase 0 Priorities)
1. Learn Hytale building tools
2. Build proof-of-concept (small plaza)
3. Research scripting capabilities
4. Start Discord community
5. Find team members (builders, scripters)

### Team Collaboration
Key roles needed (per VISION_DOCUMENT.md):
- **Builder(s):** World building, environmental design (High priority)
- **Scripter/Developer:** Modding, game logic, systems (High priority)
- **3D Modeler:** Custom furniture, items, cosmetics (Medium priority)
- **2D Artist:** UI, icons, branding (Medium priority)

## Design Constraints

- Hytale is in Early Access - capabilities may be limited
- All monetization must be cosmetic-only (no gameplay advantages)
- Systems should feel rewarding without pressure (cozy, not grindy)
- Target audience: 13+, family-friendly content
- All items must be earnable through gameplay (no purchase-exclusives)
