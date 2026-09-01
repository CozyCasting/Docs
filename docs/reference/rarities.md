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
3. **Active effects and consumables** — Timed buffs like a Rarity Boost potion shift the odds further
4. **Gear** — Equipped gear can carry its own rarity bonus

These bonuses shift weight from Common toward higher tiers.

!!! note "Location doesn't change your odds"
    Where you're fishing has no effect on rarity — the same odds apply whether you're casting into the Appalachian Stream or the Patagonian Ice Fields. Location decides the **species pool**, the **base coin value**, and the **XP** you earn, not what rarity you can pull. See the [Locations Reference](locations.md) for how those vary.

## Value Calculation

A fish's coin value builds up through an ordered chain of multipliers, all applied to the location type's base value:

1. **Location level scaling** — higher-level location types scale the base value up; the Arctic's scaling is 13.5x the Stream's before anything else is applied.
2. **Geographic region** — North America is the baseline, Asia runs about 1.15x, Europe about 1.30x, and South America about 1.79x, on top of the location scaling.
3. **Rarity sell multiplier** — from the table above.
4. **Size factor** — bigger-than-average fish of their species sell for more, smaller for less, within a 0.5x–5.0x range.
5. **Weight bonus** — a smaller nudge, clamped between 0.5x and 2.0x.
6. **Pattern bonus** — from Solid (1.0x) up to Speckled (1.5x).
7. **Trait multipliers** — stack on top, and a fish with a secondary colour gets a further +15%.

Finally, a **soft cap** keeps any single fish from being worth an absurd amount: value above the cap only counts for 10% of what it normally would, and value above *twice* the cap only counts for 2.5%. The caps scale with rarity, from 12,000 for a Common up to 3,000,000 for a Unique.

None of this changes which rarities can appear where — any rarity can come from any water. It only changes how much a given catch is worth once you land it.

## Unique Rarity

Unique fish are special event-only catches that cannot appear from normal fishing. They have a 500x sell multiplier and 50x XP multiplier — but you might want to keep them as collector's items. The most common way to get one is catching a Monster Fish while placing 1st in a Monster Fish event.
