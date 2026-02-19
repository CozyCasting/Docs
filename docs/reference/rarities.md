# Rarities Reference

Every fish has a rarity tier that determines its value, XP reward, and how likely it is to appear.

## Rarity Tiers

| Rarity | Emoji | Base Chance | Sell Multiplier | XP Multiplier | Color |
|--------|-------|------------|-----------------|---------------|-------|
| Common | :white_circle: | ~70% | 1x | 1x | Grey |
| Uncommon | :green_circle: | ~20% | 2x | 1.5x | Green |
| Rare | :blue_circle: | ~7% | 5x | 2.5x | Blue |
| Epic | :purple_circle: | ~2.25% | 12x | 5x | Purple |
| Legendary | :yellow_circle: | ~0.6% | 30x | 10x | Gold |
| Mythical | :red_circle: | ~0.15% | 100x | 25x | Red |
| Unique | :star: | Event only | 500x | 50x | Gold |

## How Rarity Is Determined

Base chances are modified by:

1. **Rod rarity bonus** — Each rod adds a flat percentage bonus (e.g., Mystic Rod adds +50%)
2. **Bait rarity bonus** — Equipped bait adds an additional bonus (e.g., Magic Bait adds +35%)
3. **Location rarity modifiers** — Some locations give extra chances for specific rarities

These bonuses shift weight from Common toward higher tiers.

## Value Calculation

A fish's coin value is calculated as:

> **Value** = Location Base Value x Rarity Sell Multiplier x Trait Multipliers

### Example Values by Location and Rarity

| | Stream (10) | River (25) | Ocean (50) | Deep Sea (80) | Arctic (100) |
|---|-----------|-----------|-----------|-------------|-------------|
| Common (1x) | 10 | 25 | — | — | — |
| Uncommon (2x) | 20 | 50 | 100 | — | — |
| Rare (5x) | 50 | 125 | 250 | 400 | 500 |
| Epic (12x) | — | 300 | 600 | 960 | 1,200 |
| Legendary (30x) | — | — | 1,500 | 2,400 | 3,000 |
| Mythical (100x) | — | — | — | 8,000 | 10,000 |

*Dashes indicate that rarity is not available at that location type.*

Trait multipliers stack on top. A Giant (2x) Mythical fish from the Arctic would be worth **20,000 coins**.

## Unique Rarity

Unique fish are special event-only catches that cannot appear from normal fishing. They have a 500x sell multiplier and 50x XP multiplier — but you might want to keep them as collector's items.
