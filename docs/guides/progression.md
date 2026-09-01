# Progression Guide

Level up, unlock new content, and earn achievements and titles.

## XP and Leveling

Every fish you catch earns XP. The amount depends on where you caught it, its rarity, and its traits.

**Base XP per catch:** 25 XP, scaled up by three things in order:

1. **Location type** — deeper, higher-level waters are worth more XP. The multiplier is roughly `1 + (location's base level x 0.04)`, so a Stream catch is about 1.04x while an Arctic catch is about 3.0x.
2. **Geographic region** — the same water is worth more the further into a region's level range it sits, so a Common at the Patagonian Ice Fields earns noticeably more than a Common at the Alaskan Arctic even though both are "Arctic" catches.
3. **Rarity's XP multiplier**, then trait bonuses (traits matter less for XP than they do for coins), a seasonal-pattern bonus, and any gear XP bonus.

The number scales with **where** you fish as much as **what** you catch. For example:

- A Common at the Appalachian Stream (NA Stream) is worth about **26 XP**.
- A Common at the Patagonian Ice Fields (SA Arctic) is worth about **262 XP** — the same rarity, over ten times the reward, purely from location.
- A Mythical at the Patagonian Ice Fields is worth about **6,562 XP**.

Traits like Giant (1.5x), Ancient (2x), and Glowing (1.75x) multiply on top of all of the above, though their effect on XP is smaller than their effect on coin value.

### XP Formula

The XP required to reach each level follows a power curve:

> **XP for level N** = 30 x N^2.3^

| Level | Total XP Required | XP for This Level |
|-------|------------------|-------------------|
| 2 | 147 | 147 |
| 5 | 1,215 | 488 |
| 10 | 5,985 | 1,288 |
| 20 | 29,477 | 3,280 |
| 50 | 242,522 | 11,011 |
| 75 | 616,257 | 18,735 |
| 100 | 1,194,321 | 27,291 |
| 110 | 1,487,046 | 30,910 |
| 125 | 1,995,327 | 36,523 |

The maximum level is **125**.

### Level-Up Bonuses

When you level up into a new stretch of water, your level-up message names the location and points you at `/locations` and `/travel` so you can find it. If you jump multiple levels at once, you'll see every water you crossed — so a big catch that takes you from level 18 to level 22 names both the Pacific Ocean (level 20) and Lake Baikal (level 22), not just the last one. If more than three open up at once, the message names three and says how many more there are.

## Achievements

Achievements are milestones that reward you for playing. They're organized into categories:

- **Level** — Reach certain levels
- **Fishing** — Catch a number of fish or specific rarities
- **Collection** — Build your tank collection
- **Exploration** — Visit different locations
- **Economy** — Earn coins
- **Voting** — Vote for the bot
- **Daily** — Maintain daily streaks

Each achievement grants a reward when unlocked — typically coins, bait, consumables, or a title.

The Level category's headline milestones are **Mythical Angler** (level 75), **Fishing God** (level 100), **Deep Water** (level 110), and **End of the Map** (level 125 — the highest there is).

Check your progress with `/achievements` and filter by category.

## Titles

Titles are cosmetic labels that appear on your profile. They're unlocked through:

- **Achievements** — Most titles come from hitting milestones
- **Chest drops** — Rare titles can drop from higher-tier chests

Titles have their own rarity tiers: Common, Rare, Epic, and Legendary.

Equip a title with `/title <name>` to show it off on your profile.

## What Levels Unlock

As you level up, you unlock access to new locations, better equipment, and achievements:

| Level | Unlocks |
|-------|---------|
| 1 | Stream, Pond (NA) |
| 5 | River (NA), Wooden Rod |
| 10 | Lake (NA), Fiberglass Rod, **Basic Net** |
| 15 | Asia (Stream, Pond), Pearl Rod, **Improved Net**, **Camp** |
| 20 | Ocean (NA), Carbon Fiber Rod, **Reinforced Net** |
| 25 | Cave (NA), **Master Net** |
| 30 | Europe (Stream, Pond), Reef (NA), **Legendary Net** |
| 35 | Deep Sea (NA), Titanium Rod |
| 45 | Volcano (NA) |
| 50 | Arctic (NA), Legendary Rod |
| 55 | Shipwreck (NA) |
| 60 | Deep Sea (Europe) |
| 65 | Shipwreck (Europe) |
| 68 | Volcano (Europe) |
| 75 | Mystic Rod, Arctic (Europe) |
| 80–125 | South America opens gradually, from Andean Meltwater (Stream, level 80) through to Patagonian Ice Fields (Arctic, level 125) — the last water on the map |

*South America's full route — every location and the level it opens at — is in the [Locations Reference](../reference/locations.md#south-america).*

*Note: Nets are passive fishing items that automatically catch fish for you over time. Once you reach the required level, you can purchase them in the **Nets** tab of the `/shop`. Use `/net status` and `/net collect` to manage them!*
