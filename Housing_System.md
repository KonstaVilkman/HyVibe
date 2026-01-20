# Housing System

**Purpose:** Personal space for self-expression, social hosting, and flexing.  
**Status:** Concept Phase

---

## Core Concept

Housing is the **endgame flex**. Players grind to upgrade, decorate, and show off their apartments. Visiting others' homes is a core social activity.

**Key Principles:**
- Apartments are instanced (private dimensions)
- Progression through tiers
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
    â†“
Server loads that player's instance
    â†“
Player appears in their apartment
    â†“
Other players can be invited/join
    â†“
Leaving returns to shared world
```

---

## Apartment Tiers

| Tier | Name | Size | Rooms | Cost | Unlock Requirement |
|------|------|------|-------|------|-------------------|
| 1 | Studio | Small | 1 | Free (starter) | New player |
| 2 | Apartment | Medium | 2-3 | $2,000 + 5 [ANCHOR] | Level 10 |
| 3 | Loft | Large | 4-5 | $5,000 + 15 [ANCHOR] | Level 20 |
| 4 | Penthouse | Huge | 6+ | $15,000 + 40 [ANCHOR] | Level 35 |
| 5 | Mansion | Massive | 10+ | $50,000 + 100 [ANCHOR] | Level 50 |

### What Each Tier Unlocks

| Tier | New Features |
|------|--------------|
| Studio | Basic furniture, 1 room |
| Apartment | Multiple rooms, balcony, more slots |
| Loft | Outdoor space, special furniture |
| Penthouse | Rooftop, premium slots, party bonuses |
| Mansion | Ultimate space, unique items only |

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
| Common | Cash shop, always | White/gray name |
| Uncommon | Cash shop, rotating | Green name |
| Rare | Orb shop, events | Blue name |
| Epic | Events, crafting | Purple name |
| Legendary | Rare drops, limited | Orange name |
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
â˜…â˜…â˜… Luxurious
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

| Party Type | Cost | Duration | Max Guests | Fame Multiplier |
|------------|------|----------|------------|-----------------|
| Casual Hangout | Free | Unlimited | 10 | 1x (base) |
| Small Party | 1 [ANCHOR] | 2 hours | 20 | 1.5x |
| Big Party | 3 [ANCHOR] | 4 hours | 40 | 2x |
| Mega Party | 10 [ANCHOR] | 8 hours | 100 | 3x |

### How Parties Work

1. Host starts party (pays Anchor if applicable)
2. Party appears in public "Active Parties" list
3. Players can join from list
4. Host earns Fame from guest presence/activities
5. Host earns % of guest earnings (based on Fame tier)
6. Party ends when duration expires or host ends it

### Party Fame Earning (Host)

| Guest Action | Host Fame Earned |
|--------------|------------------|
| Guest present (per 5 min) | +1 |
| Guest plays minigame | +3 |
| Guest uses interactive furniture | +2 |
| Guest likes apartment | +5 |
| Guest invites friend | +2 |

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

**Staff Pick:** +500 Fame, special badge for the week

---

## Apartment Unlock Flow

```
New Player
    â†“
Starter Studio (Free)
    â†“
Level 10 â†’ Unlock Apartment tier (Buy for $/Anchor)
    â†“
Level 20 â†’ Unlock Loft tier
    â†“
Level 35 â†’ Unlock Penthouse tier
    â†“
Level 50 â†’ Unlock Mansion tier
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
| Premium Shop | Orbs | Always |
| Rotating Shop | Cash/Orbs | Daily refresh |
| Event Shop | Event Tickets | During events |
| Crafting | Materials + Anchor | Anytime |
| Drops | Free (rare) | Random from activities |
| Trading | Cash/Anchor | Player-to-player |

### Crafting Furniture

Rare furniture can be crafted:

```
Recipe: Neon Couch (Epic)
- 5x Fabric (from job/minigame)
- 3x Neon Tube (from shop)
- 2x [ANCHOR]
= Neon Couch
```

Crafting provides:
- Anchor sink
- Goal for collectors
- Alternative to buying

---

## Open Questions

| Question | Considerations |
|----------|----------------|
| Exact tier costs | Needs balancing |
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
- Anchor sinks (upgrades, parties)
- Social visiting/discovery
- Collection gameplay (furniture)

---

*See FAME_SYSTEM.md for party hosting bonuses.*  
*See ECONOMY_SYSTEM.md for furniture costs.*