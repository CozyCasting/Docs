# Progression Guide

Level up, unlock new content, and earn achievements and titles.

## XP and Leveling

Every fish you catch earns XP. The amount depends on the fish's rarity and traits.

**Base XP per catch:** 10 XP, multiplied by the rarity's XP multiplier and any trait bonuses.

| Rarity | XP per Catch |
|--------|-------------|
| Common | 10 |
| Uncommon | 15 |
| Rare | 25 |
| Epic | 50 |
| Legendary | 100 |
| Mythical | 250 |

Traits like Giant (1.5x), Ancient (2x), and Glowing (1.75x) multiply on top of the rarity bonus.

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

The maximum level is **100**.

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
| 30 | Europe (Stream, Pond), **Legendary Net** |
| 35 | Deep Sea (NA), Titanium Rod |
| 45 | Volcano (NA) |
| 50 | Arctic (NA), Legendary Rod |
| 75 | Mystic Rod |

*Note: Nets are passive fishing items that automatically catch fish for you over time. Once you reach the required level, you can purchase them in the **Nets** tab of the `/shop`. Use `/net status` and `/net collect` to manage them!*
