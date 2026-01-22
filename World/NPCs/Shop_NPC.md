# Shop NPC

**Purpose:** Primary general store for basic items and currency exchanges.
**Location:** Penthouse Bar - Shop Area (Main Floor)
**Status:** Phase 0A

---

## Overview

The Shop NPC is the main vendor players interact with for everyday purchases. Located prominently in the Penthouse Bar, this NPC offers a stable selection of common items at fixed prices.

---

## Appearance

| Aspect | Design |
|--------|--------|
| **Style** | Friendly shopkeeper, approachable |
| **Indicator** | Shop bag/coin icon above head |
| **Interaction** | Click to open shop UI |

---

## Shop Inventory

### Always Available

| Category | Items | Price Range | Currency |
|----------|-------|-------------|----------|
| **Basic Cosmetics** | Common outfits, accessories | $200-1,000 | Cash |
| **Starter Furniture** | Basic chairs, tables, decor | $100-500 | Cash |
| **Consumables** | Food, drinks (social items) | $20-100 | Cash |
| **Lootboxes** | Common Lootbox only | $500 | Cash |
| **Job Tools** | Basic efficiency items | $200-500 | Cash |

### Rotating Stock (Daily Reset)

| Slot | Item Type | Refresh |
|------|-----------|---------|
| Featured Item 1 | Random Uncommon cosmetic | Daily |
| Featured Item 2 | Random furniture piece | Daily |
| Featured Item 3 | Random accessory | Daily |

---

## Pricing Philosophy

| Principle | Implementation |
|-----------|----------------|
| **Fair Base Prices** | Items priced at intended value |
| **No Inflation** | Prices never increase |
| **Buyback** | Sell items for 50% of shop price |
| **No Exclusive Items** | Everything also earnable through gameplay |

---

## Shop UI Features

```
┌─────────────────────────────────────────────────────┐
│  GENERAL SHOP                         [X] Close     │
├─────────────────────────────────────────────────────┤
│                                                     │
│  Your Cash: $2,450                                  │
│                                                     │
│  ┌─────────┐ ┌─────────┐ ┌─────────┐               │
│  │COSMETICS│ │FURNITURE│ │ ITEMS   │  ← Tabs       │
│  └─────────┘ └─────────┘ └─────────┘               │
│                                                     │
│  ┌─────────────────────────────────────────────┐   │
│  │ ┌───┐  Basic Tee            $300            │   │
│  │ │ ☐ │  Common cosmetic      [BUY]           │   │
│  │ └───┘                                       │   │
│  │ ┌───┐  Casual Jeans         $450            │   │
│  │ │ ☐ │  Common cosmetic      [BUY]           │   │
│  │ └───┘                                       │   │
│  │ ┌───┐  ★ Daily Special      $800            │   │
│  │ │ ☐ │  Uncommon hat         [BUY]           │   │
│  │ └───┘                                       │   │
│  └─────────────────────────────────────────────┘   │
│                                                     │
│  [SELL ITEMS]                                       │
│                                                     │
└─────────────────────────────────────────────────────┘
```

---

## Sell System

Players can sell items back to the shop:

| Item Rarity | Sell Price |
|-------------|------------|
| Common | 50% of base value |
| Uncommon | 50% of base value |
| Rare+ | 50% of base value |
| Event Items | Cannot sell |
| Achievement Items | Cannot sell |

**Sell Confirmation:** Items worth over $1,000 show a confirmation dialog.

---

## Location Details

```
    MAIN BAR (Interior)

    ┌─────────────────────────────────────────┐
    │                                         │
    │   ┌───────┐                             │
    │   │ SHOP  │  ← Shop NPC stands here     │
    │   │  NPC  │                             │
    │   │  [S]  │                             │
    │   └───────┘                             │
    │                                         │
    │   Item displays nearby (visual)         │
    │   ┌───┐ ┌───┐ ┌───┐                     │
    │   │ □ │ │ □ │ │ □ │                     │
    │   └───┘ └───┘ └───┘                     │
    │                                         │
    └─────────────────────────────────────────┘
```

---

## Phase 0A Scope

### Implemented
- [ ] NPC placement
- [ ] Basic shop UI
- [ ] Cash transactions
- [ ] Common items available

### Later Phases
- Daily rotating stock
- Full furniture catalog
- Seasonal items
- Shop reputation/discounts

---

*See [../../Systems/Economy_System.md](../../Systems/Economy_System.md) for currency details.*
