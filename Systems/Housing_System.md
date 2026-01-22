# Housing System

**Purpose:** Personal space for self-expression, social hosting, and flexing.
**Status:** Concept Phase
**Last Updated:** January 2026

---

## Core Concept

Housing is the **endgame flex**. Players grind to upgrade, decorate, and show off their apartments. Visiting others' homes is a core social activity.

**Key Principles:**
- Apartments are instanced (private dimensions)
- Progression through tiers (Cash only - no currency gates)
- Decoration is the primary expression
- Parties turn housing into Fame engines

---

## Technical Model: Instanced Housing

**Each apartment exists in its own instance.**

| Benefit | Why It Matters |
|---------|----------------|
| No performance issues | Hundreds of apartments don't load simultaneously |
| No location conflicts | Multiple players can "own" same building |
| Unlimited housing | Server can support any player count |
| Privacy control | Owner decides who can enter |

### How It Works

```
Player enters apartment door
    |
Server loads that player's instance
    |
Player appears in their apartment
    |
Other players can be invited/join
    |
Leaving returns to shared world
```

---

## Apartment Tiers

| Tier | Name | Size | Rooms | Cost | Unlock Requirement |
|------|------|------|-------|------|-------------------|
| 1 | Studio | Small | 1 | Free (starter) | New player |
| 2 | Apartment | Medium | 2-3 | $3,000 | Level 10 |
| 3 | Loft | Large | 4-5 | $10,000 | Level 25 |
| 4 | Penthouse | Huge | 6+ | $30,000 | Level 40 |
| 5 | Mansion | Massive | 10+ | $75,000 | Level 60 |

**Design Note:** Housing costs are Cash-only. No premium currency gates. Every player can reach every tier through normal play.

### What Each Tier Unlocks

| Tier | New Features | Plant Slots |
|------|--------------|-------------|
| Studio | Basic furniture, 1 room, 20 item slots | 2 |
| Apartment | Multiple rooms, 50 item slots | 3 |
| Loft | Outdoor space, special furniture, 100 item slots | 4 |
| Penthouse | Rooftop, premium slots, party bonuses, 150 item slots | 5 |
| Mansion | Ultimate space, unique items only, 250 item slots | 6 |

### Crystal-Unlockable Features

Some housing features require **Crystals** to unlock (one-time cost):

| Feature | Crystal Cost | Available On | Description |
|---------|--------------|--------------|-------------|
| Balcony | 10-15 | Apartment+ | Outdoor extension with views |
| Rooftop Access | 15-20 | Loft+ | Private rooftop area |
| Secret Room | 25-35 | Penthouse+ | Hidden room behind bookshelf/painting |
| Basement | 20-30 | Mansion only | Underground expansion |
| Custom Entrance | 10-15 | Any tier | Personalized doorway/portal |
| Extended Garden | 20-25 | Mansion only | Large outdoor green space |

**Design Note:** These features provide horizontal progression within a housing tier. Players can invest in their current home rather than always upgrading to the next tier.

---

## Furniture & Decoration

### Furniture Categories

| Category | Examples | Purpose |
|----------|----------|---------|
| **Seating** | Sofas, chairs, beanbags | Social spots, poses |
| **Tables** | Coffee tables, dining | Decorative, interaction |
| **Beds** | Single, double, luxury | Decorative, AFK spot |
| **Storage** | Shelves, cabinets | Display items |
| **Lighting** | Lamps, neon, candles | Atmosphere |
| **Decor** | Plants, art, rugs | Personalization |
| **Interactive** | TV, arcade, instruments | Activities |
| **Pets** | Following companions | Flex, personality |

### Furniture Rarity

| Rarity | Availability | Visual Indicator |
|--------|--------------|------------------|
| Common | Cash shop, lootboxes | White/gray name |
| Uncommon | Lootboxes, rotating shop | Green name |
| Rare | Lootboxes, events | Blue name |
| Epic | Lootboxes (rare), achievements | Purple name |
| Legendary | Lootboxes (very rare), events | Orange name |
| Event | Limited-time only | Special border |

### Furniture Sets

Themed collections that encourage completion:

| Set | Theme | Pieces | Completion Bonus |
|-----|-------|--------|------------------|
| Cozy Cabin | Rustic, warm | 15 | +5% party Fame |
| Neon Night | Cyberpunk, glow | 12 | Special light effect |
| Botanical | Plants, nature | 18 | Ambient sounds |
| Vintage | Retro, classic | 14 | Sepia filter option |

---

## Apartment Value Score

**Visible metric showing apartment "worth."**

### How It's Calculated

| Factor | Points |
|--------|--------|
| Apartment tier | 100-500 base |
| Furniture count | +2 per item |
| Furniture rarity | +5 (uncommon) to +50 (legendary) |
| Set completion | +100 per completed set |
| Unique items | +25 each |
| Visit count (all-time) | +0.1 per visit |
| Like count | +1 per like |

### Display

Shown on apartment entrance and player profile:

```
Apartment Value: 2,847
*** Luxurious
```

| Value Range | Rating |
|-------------|--------|
| 0-500 | Starter |
| 501-1,500 | Cozy |
| 1,501-3,000 | Stylish |
| 3,001-6,000 | Luxurious |
| 6,001-12,000 | Extravagant |
| 12,001+ | Legendary |

---

## Plant System

### Overview

Plants are a **passive lootbox generation system** inside player apartments. They provide a cozy, low-effort way to earn rewards over time.

### How Plants Work

1. Player plants a seed in an available plant slot
2. Plant grows over time (real-time, even while offline)
3. When ready, player harvests for a lootbox
4. Slot becomes available for a new seed

### Plant Types

| Seed Type | Grow Time | Yield | Source |
|-----------|-----------|-------|--------|
| Common Seed | 12 hours | 1 Common Lootbox | Shop, lootbox drops |
| Rare Seed | 48 hours | 1 Rare Lootbox | Shop, lootbox drops |
| Epic Seed | 72 hours | 1 Epic Lootbox | Achievements, events |
| Super Seed | 72 hours | 1 Epic + chance for 1-2 bonus boxes (any rarity) | High-price shop only |

### Plant Slots by Housing Tier

| Housing Tier | Plant Slots |
|--------------|-------------|
| Studio | 2 |
| Apartment | 3 |
| Loft | 4 |
| Penthouse | 5 |
| Mansion | 6 |

### Seed Acquisition

| Source | Seed Types Available |
|--------|---------------------|
| Basic Shop (Cash) | Common, Rare |
| Premium Shop (Cash, high price) | Super Seed |
| Lootbox drops | Common, Rare (as contents) |
| Event rewards | Epic Seeds |
| Achievement rewards | Epic Seeds |
| Player trading | All types (tradeable) |

### Design Philosophy

Plants create a **daily check-in loop** without pressure:
- Log in → check plants → harvest if ready → replant
- Rewards patience, not grinding
- Encourages apartment visits (see your growing garden)
- Scales with housing investment (more slots = more passive income)

---

## Social Features

### Visiting

- Visit any player's apartment (if public or invited)
- Costs nothing
- Host gains +2 Fame per visitor
- Visitor can "Like" apartment (+5 Fame to host)
- One like per visitor per day

### Privacy Settings

| Setting | Who Can Enter |
|---------|---------------|
| Public | Anyone |
| Friends Only | Friends list |
| Invite Only | Must be invited |
| Private | Owner only |

### Guest Interactions

When visiting someone's apartment:
- Sit on furniture (poses)
- Use interactive items
- Chat
- Like the apartment
- Join hosted party (if active)

---

## Party System

### What Are Parties?

**Hosted events in your apartment that generate Fame and create social hubs.**

### Party Tiers

| Party Type | Cash Cost | Crystal Cost | Duration | Max Guests | Fame Multiplier |
|------------|-----------|--------------|----------|------------|-----------------|
| Casual Hangout | Free | Free | Unlimited | 15 | 1x (base) |
| Small Party | $500 | 1 Crystal | 2 hours | 25 | 1.5x |
| Big Party | $2,000 | 2 Crystals | 4 hours | 50 | 2x |
| Mega Party | $5,000 | 4 Crystals | 8 hours | 100 | 3x |

**Design Note:** Boosted parties require both Cash AND Crystals. This makes hosting more intentional while keeping Casual Hangouts accessible to everyone. Crystals are tradeable, so non-social players can sell them to frequent hosts.

### How Parties Work

1. Host starts party (pays Cash + Crystals for boosted parties)
2. Party appears in public "Active Parties" list
3. Players can join from list
4. Host earns Fame from guest presence/activities
5. Host earns % of guest earnings (based on Fame tier)
6. Party ends when duration expires or host ends it

**Hosting Frequency Targets:**
- Mid-game players: ~1 Big Party per 2-3 days
- High-level players: 1-2 Big Parties per day (if focused on hosting)

### Party Fame Earning (Host)

| Guest Action | Host Fame Earned | With 2x Multiplier |
|--------------|------------------|-------------------|
| Guest present (per 5 min) | +1 | +2 |
| Guest plays minigame | +2 | +4 |
| Guest uses interactive furniture | +1 | +2 |
| Guest likes apartment | +5 | +10 |
| Guest invites friend | +2 | +4 |

**Example:** Big Party (2x multiplier) with 20 guests for 2 hours:
- 20 guests x 24 intervals (2 hours) x 2 Fame = 960 Fame
- Plus activity bonuses

### Why Host Parties?

| Reason | Benefit |
|--------|---------|
| Fame growth | Primary Fame engine |
| Passive income | % of guest earnings |
| Social status | "Good host" reputation |
| Apartment exposure | More visits, more likes |
| Community building | Your apartment becomes known |

---

## Featured Apartments

### Discovery System

Players can find apartments through:

| List | Criteria | Refresh |
|------|----------|---------|
| Active Parties | Currently hosting | Real-time |
| Most Visited (Today) | Highest visit count | Daily |
| Rising | New apartments gaining traction | Daily |
| Staff Picks | Curated by moderation | Weekly |
| Top Rated | Highest like ratio | Weekly |

### Featured Apartment Bonus

**Staff Pick:** +500 Fame, special badge for the week, 1 Rare Lootbox

---

## Apartment Unlock Flow

```
New Player
    |
Starter Studio (Free)
    |
Level 10 -> Unlock Apartment tier ($3,000)
    |
Level 25 -> Unlock Loft tier ($10,000)
    |
Level 40 -> Unlock Penthouse tier ($30,000)
    |
Level 60 -> Unlock Mansion tier ($75,000)
```

### Why Gate By Level?

- Creates progression goals
- Ensures players understand systems before upgrading
- Prevents new players from feeling overwhelmed
- Makes higher tiers aspirational

---

## Furniture Economy

### Where to Get Furniture

| Source | Currency | Availability |
|--------|----------|--------------|
| Basic Shop | Cash | Always |
| Rotating Shop | Cash/Gems | Daily refresh |
| Lootboxes | Gems (or free from progression) | Always |
| Event Shop | Event Tokens | During events |
| Achievements | Free | One-time |
| Trading | Cash | Player-to-player |

### Furniture Price Ranges

| Rarity | Cash Shop Price | Trade Value |
|--------|-----------------|-------------|
| Common | $100-300 | $50-200 |
| Uncommon | $500-1,500 | $300-1,000 |
| Rare | Not sold (lootbox only) | $2,000-5,000 |
| Epic | Not sold (lootbox only) | $10,000-25,000 |
| Legendary | Not sold (lootbox only) | $50,000+ |

---

## Open Questions

| Question | Considerations |
|----------|----------------|
| Exact tier costs | May need balancing after playtesting |
| Party duration lengths | 2/4/8 hours feel right? |
| Max furniture per room | Performance limits? |
| Outdoor spaces | Gardens, balconies, rooftops? |
| Multiple apartments? | Own more than one? |

---

## Summary

Housing provides:
- Endgame flex and goal
- Personal expression space
- Fame engine through parties
- Cash sinks (upgrades, parties)
- Social visiting/discovery
- Collection gameplay (furniture from lootboxes)

---

*See [Fame_System.md](Fame_System.md) for party hosting bonuses.*
*See [Economy_System.md](Economy_System.md) for furniture costs and lootbox drops.*
