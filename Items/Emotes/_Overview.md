# Emotes

Animations and expressions for player characters. A core social feature in HyVibe.

---

## Emote Syncing

One of the main social mechanics. When a player is emoting, others can click on them to join in and sync up.

**How it works:**
1. Player A starts an emote (dancing, waving, sitting, etc.)
2. Player B clicks on Player A
3. Player B automatically joins and syncs to the same emote
4. More players can click to join - no limit

**Why this matters:**
- Creates spontaneous group moments
- Dance floors actually feel alive
- Easy way to interact without typing
- Strangers become friends through shared emotes

### Fame from Syncing

Group emotes earn Fame for everyone involved. The more people sync up, the more Fame generated.

| Participants | Fame (each) |
|--------------|-------------|
| 2 players | +1 |
| 3-5 players | +2 |
| 6-10 players | +3 |
| 11+ players | +5 |

*Cooldown: Fame from syncing only triggers once per emote session (prevents spam)*

---

## Emote Categories

| Category | Examples | Sync Type |
|----------|----------|-----------|
| **Dances** | Club dance, Wave, Groove | Full sync - everyone matches |
| **Sitting** | Sit, Lounge, Meditate | Position sync - sit together |
| **Reactions** | Clap, Cheer, Laugh | Timing sync |
| **Poses** | Photo pose, Flex, Peace sign | Static sync |
| **Special** | Event/rare emotes | Unique sync animations |

---

## Emote Sources

| Source | Emote Type |
|--------|------------|
| Starter pack | 5 basic emotes (wave, sit, dance, clap, peace) |
| Lootboxes | Common to Epic emotes |
| Fame milestones | Exclusive emotes per tier |
| Events | Limited-time seasonal emotes |
| Shop | Rotating selection |

---

## Rarity

| Rarity | Drop Rate | Examples |
|--------|-----------|----------|
| Common | 60% | Basic wave, simple sit |
| Uncommon | 25% | Themed dances, reactions |
| Rare | 12% | Complex animations, group-focused |
| Epic | 3% | Flashy effects, unique animations |

---

## Technical Notes

- Sync uses host player's animation timing as reference
- Late joiners snap to current animation frame
- Emotes interrupted by movement or damage
- Some emotes have idle loops, others are one-shot

---

*See [../Systems/Fame_System.md](../../Systems/Fame_System.md) for Fame earning details.*
