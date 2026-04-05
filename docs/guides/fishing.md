# Fishing Guide

Everything you need to know about catching fish in CozyCasting.

## How Catching Works

When you use `/fish`, the game:

1. **Picks a species** from the pool available at your current location
2. **Rolls a rarity** based on base weights, modified by your rod and bait bonuses
3. **Rolls for traits** — special modifiers that affect value and XP
4. **Calculates size, value, and XP** based on all the above

## Rarity Tiers

Fish come in 7 rarity tiers. Higher rarities are worth more coins and XP but are much harder to catch.

| Rarity | Base Chance | Sell Multiplier | XP Multiplier |
|--------|------------|-----------------|---------------|
| Common | ~70% | 1x | 1x |
| Uncommon | ~20% | 2x | 1.5x |
| Rare | ~7% | 5x | 2.5x |
| Epic | ~2.25% | 12x | 5x |
| Legendary | ~0.6% | 30x | 10x |
| Mythical | ~0.15% | 100x | 25x |
| Unique | Event only | 500x | 50x |

Your rod and bait add **rarity bonuses** that shift the odds in your favor. See the [Rarities Reference](../reference/rarities.md) for the full breakdown.

## Traits

Fish can spawn with special traits that modify their value and XP. Traits are rolled independently of rarity.

### Positive Traits

| Trait | Value Multiplier | XP Multiplier | Rarity |
|-------|-----------------|---------------|--------|
| Shiny | 1.5x | 1.25x | Uncommon |
| Pristine | 1.75x | 1.5x | Uncommon |
| Giant | 2x | 1.5x | Rare |
| Glowing | 2.25x | 1.75x | Rare |
| Ancient | 2.5x | 2x | Very Rare |

### Special Traits

| Trait | Value Multiplier | XP Multiplier | Source |
|-------|-----------------|---------------|--------|
| Pearlescent | 1.6x | 1.3x | Pearl Rod exclusive |

### Negative Traits

| Trait | Value Multiplier | XP Multiplier | Rarity |
|-------|-----------------|---------------|--------|
| Tiny | 0.5x | 1x | Common |
| Damaged | 0.25x | 0.75x | Common |

Trait multipliers stack with rarity multipliers, so a Giant Legendary fish is worth significantly more than a normal one.

### Breeding-Only Mutations

These rare traits can **only** appear through the fish breeding system. They offer exceptional value bonuses and unique appearances.

| Trait | Value Multiplier | XP Multiplier | Appearance | Source |
|-------|-----------------|---------------|-----------|--------|
| Gilded | 3.5x | 1.3x | Rich golden shimmer | Breeding mutation (2–6% chance) |
| Bioluminescent | 2.5x | 1.3x | Glowing teal coloration | Breeding mutation (2–6% chance) |
| Colossal | 1.8x | 1.3x | Massive size (2–3× normal) | Special: Both parents Giant (5% chance) |

**How to obtain:**
- **Gilded & Bioluminescent** — Random mutations that can occur during breeding. Mutation chance increases with Breeding Tank level (2% at Level 1–2, 4% at Level 3–4, 6% at Level 5). Only one mutation per breeding session.
- **Colossal** — A special upgrade that occurs when both parents have the Giant trait. There's a 5% chance the Giant trait becomes Colossal instead. If both parents are Giant, the offspring also has a bonus 25% chance to inherit Giant even if the normal inheritance roll fails.

## Improving Your Odds

### Rods

Better rods reduce your fishing cooldown **and** increase your rarity bonus. Each rod has a rarity bonus percentage that shifts catches toward higher tiers.

| Rod | Cooldown Reduction | Rarity Bonus | Cost | Level |
|-----|-------------------|--------------|------|-------|
| Basic Rod | 0s | +0% | Free | 1 |
| Wooden Rod | -5s | +5% | 500 coins | 5 |
| Fiberglass Rod | -10s | +10% | 2,000 coins | 10 |
| Carbon Fiber Rod | -15s | +15% | 8,000 coins | 20 |
| Titanium Rod | -20s | +20% | 25,000 coins | 35 |
| Legendary Rod | -30s | +30% | 100,000 coins | 50 |
| Mystic Rod | -40s | +50% | 500,000 coins | 75 |
| Pearl Rod | 0s | +0% | 500 pearls | 15 |

The **Pearl Rod** is special — it doesn't boost rarity or reduce cooldown, but it can give fish the exclusive **Pearlescent** trait.

### Bait

Bait is consumed on each cast and provides a rarity bonus. Some baits work better in specific location types.

| Bait | Rarity Bonus | Best Locations | Cost | Uses |
|------|-------------|----------------|------|------|
| Earthworm | +0% | All | 5 coins | 1 |
| Cricket | +2% | Pond, River, Lake | 10 coins | 1 |
| Minnow | +5% | Lake, River | 25 coins | 1 |
| Shrimp | +8% | Ocean, Deep Sea | 50 coins | 1 |
| Squid | +12% | Deep Sea, Ocean | 100 coins | 1 |
| Golden Lure | +20% | All | 2,500 coins | 1 |
| Magic Bait | +30% | All | 6,000 coins | 1 |
| Seasonal Bait | +25% | All | 500 coins | 1 |
| Lucky Double Worm | +5% | All | N/A (Event/Drop) | 1 |

*Note: The **Seasonal Bait** gives a 50% chance to guarantee catching a Seasonal Variant fish (when an event is active). The **Lucky Double Worm** provides a 15% chance to catch two fish in a single cast!*

## Location Matters

Different locations have different species pools, base values, and rarity modifiers. Higher-level locations like Deep Sea, Volcano, and Arctic have better odds for Epic+ fish and higher base coin values. See the [Locations Reference](../reference/locations.md) for details.

## Nets (Passive Fishing)

In addition to casting your rod, you can passively catch fish using your **Net**. Your net automatically gathers fish and occasional items or chests over time while you are away.

Use `/net status` to view your current net capacity and what's waiting for you, and use `/net collect` to claim your catches! Nets can sometimes catch rare fish or items, making them an excellent way to continue progressing even when you aren't actively fishing.

## Chests

There's a ~5% chance to receive a chest when you catch a fish. Chests come in tiers: Common, Rare, Epic, and Legendary. Core chests open directly with no key required. Seasonal chests (limited-time event chests) require a Chest Key and have a daily open limit based on your level.

See the [Economy Guide](economy.md#chests) for more details on chest loot and seasonal variants.
