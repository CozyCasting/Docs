# Rarities Reference

Every fish has a rarity tier that determines its value, XP reward, and how likely it is to appear.

## Rarity Tiers

| Rarity | Emoji | Base Chance | Sell Multiplier | XP Multiplier | Color |
|--------|-------|------------|-----------------|---------------|-------|
| Common | :white_circle: | ~70% | 1x | 1x | Grey |
| Uncommon | :green_circle: | ~20% | 2x | 1.5x | Green |
| Rare | :blue_circle: | ~7% | 5x | 2.5x | Blue |
| Epic | :purple_circle: | ~2.25% | 12x | 5x | Purple |
| Legendary | :yellow_circle: | ~0.6% | 20x | 10x | Gold |
| Mythical | :red_circle: | ~0.15% | 50x | 25x | Red |
| Unique | :star: | Event only | 500x | 50x | Gold |

## How Rarity Is Determined

Base chances are modified by:

1. **Rod rarity bonus** — Each rod adds a flat percentage bonus (e.g., Mystic Rod adds +30%)
2. **Bait rarity bonus** — Equipped bait adds an additional bonus (e.g., Magic Bait adds +30%)
3. **Location rarity modifiers** — Some locations give extra chances for specific rarities

These bonuses shift weight from Common toward higher tiers.

## Value Calculation

A fish's coin value starts from:

> **Value** = Location Base Value x Rarity Sell Multiplier x Trait Multipliers

Size, weight, and pattern also nudge the final number up or down a bit around this baseline — a larger, heavier, more elaborately patterned specimen of the same species and rarity sells for more.

### Example Values by Location and Rarity

| | Stream (15) | River (30) | Ocean (65) | Deep Sea (100) | Arctic (140) |
|---|-----------|-----------|-----------|-------------|-------------|
| Common (1x) | 15 | 30 | — | — | — |
| Uncommon (2x) | 30 | 60 | 130 | — | — |
| Rare (5x) | 75 | 150 | 325 | 500 | 700 |
| Epic (12x) | — | 360 | 780 | 1,200 | 1,680 |
| Legendary (20x) | — | — | 1,300 | 2,000 | 2,800 |
| Mythical (50x) | — | — | — | 5,000 | 7,000 |

*Dashes indicate that rarity is not available at that location type. See the [Locations Reference](locations.md) for base values of every location type.*

Trait multipliers stack on top. A Giant (2x) Mythical fish from the Arctic would be worth **14,000 coins**.

## Unique Rarity

Unique fish are special event-only catches that cannot appear from normal fishing. They have a 500x sell multiplier and 50x XP multiplier — but you might want to keep them as collector's items. The most common way to get one is catching a Monster Fish while placing 1st in a Monster Fish event.
