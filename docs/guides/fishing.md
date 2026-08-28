# Fishing Guide

Everything you need to know about catching fish in CozyCasting.

## How Catching Works

When you use `/fish`, the game:

1. **Picks a species** from the pool available at your current location
2. **Rolls a rarity** based on base weights, modified by your rod and bait bonuses
3. **Rolls for traits** — special modifiers that affect value and XP
4. **Calculates size, value, and XP** based on all the above

!!! tip "Beginner's Luck"
    The very first achievement you unlock (even something as small as your first catch) grants **Beginner's Luck** — bites come 75% faster for the next **24 hours**. It's a one-time nudge to help new anglers get going.

## Fishing Sessions

When you use `/fish`, a fishing session begins. Press **Cast Line** to start your first cast — it's guaranteed to catch a fish or chest.

Subsequent casts in the same session have an increasing **escape chance** that climbs from 0% on your second cast to roughly 80% by the 10th+ cast. If a fish escapes, your session ends. If you have a **Fishing Ticket**, you can use it to guarantee the next catch and keep fishing.

You can keep casting until you miss, run out of time, or manually stop. **One 15-minute cooldown applies per session, not per cast** — so all your catches in a session share the same cooldown timer.

### Streaks

Consecutive catches in a session build a **streak**. Each catch adds **+1% rarity bonus**, capped at **+10%** (shown on the catch embed). When your session ends, you see a summary: fish caught, kept/sold split, coins earned, XP gained, chests found, best streak, and any achievements or quests you completed along the way.

### During a Session

- **Chest catches** — There's roughly a 6% chance to reel in a chest instead of a fish. Chests count toward your streak.
- **Bait switching** — After each catch, a "Bait" button appears so you can switch bait mid-session without ending it.
- **Double catches** — A small chance to reel in two fish on one cast (each with independent species and rarity rolls). You get a 4-button view: Keep Both / Sell Both / Keep 1st Sell 2nd / Sell 1st Keep 2nd.
- **Random events** — Once in a while (about 4% per session end, level 3+), you'll run into a random encounter — a riddle, a lucky frog, a wishing well, and more. Every outcome is a win or a wash; there's no way to lose anything. See [Random Events](#random-events) below.
- **Monster Fish** — Very rarely (about 1 in 200 catches), a cooperative boss fight can spawn in your channel. See [Monster Fish](#monster-fish) below.

## Rarity Tiers

Fish come in 7 rarity tiers. Higher rarities are worth more coins and XP but are much harder to catch.

| Rarity | Base Chance | Sell Multiplier | XP Multiplier |
|--------|------------|-----------------|---------------|
| Common | ~70% | 1x | 1x |
| Uncommon | ~20% | 2x | 1.5x |
| Rare | ~7% | 5x | 2.5x |
| Epic | ~2.25% | 12x | 5x |
| Legendary | ~0.6% | 20x | 10x |
| Mythical | ~0.15% | 50x | 25x |
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

!!! tip "Spotting Pearlescent fish"
    Pearlescent fish are marked with 🦪 everywhere your fish are listed (`/tank`, bulk sell, etc.) — they're the only fish worth displaying in your camp's [Display Tank](economy.md#camp) instead of selling, since they earn pearls instead of coins. Bulk sell will warn you before you sell one, so you don't lose a pearl-earner by accident.

### Negative Traits

| Trait | Value Multiplier | XP Multiplier | Rarity |
|-------|-----------------|---------------|--------|
| Tiny | 0.5x | 1x | Common |
| Damaged | 0.25x | 0.75x | Common |

Trait multipliers stack with rarity multipliers, so a Giant Legendary fish is worth significantly more than a normal one.

### Breeding-Only Mutations

These rare traits can **only** appear through the fish breeding system. They offer exceptional value bonuses and unique appearances.

**Fertility** is a stat (0–100) on every fish that determines how many times it can breed. Wild-caught fish start with **50 fertility**. Each breeding costs **15 fertility** from each parent (minimum 10 required to breed). Offspring start with a fertility penalty — roughly parent average minus 10 — which naturally limits how many generations you can chain.

| Trait | Value Multiplier | XP Multiplier | Appearance | Source |
|-------|-----------------|---------------|-----------|--------|
| Gilded | 3.5x | 1.3x | Rich golden shimmer | Breeding mutation (2–6% chance) |
| Bioluminescent | 2.5x | 1.3x | Glowing teal coloration | Breeding mutation (2–6% chance) |
| Colossal | 1.8x | 1.3x | Massive size (2–3× normal) | Special: Both parents Giant (5% chance) |

**How to obtain:**
- **Gilded & Bioluminescent** — Random mutations that can occur during breeding. Mutation chance increases with Breeding Tank level (2% at Level 1–2, 4% at Level 3–4, 6% at Level 5). Only one mutation per breeding session.
- **Colossal** — A special upgrade that occurs when both parents have the Giant trait. There's a 5% chance the Giant trait becomes Colossal instead. If both parents are Giant, the offspring also has a bonus 25% chance to inherit Giant even if the normal inheritance roll fails.

!!! note "Pearlescent fish can't breed"
    Pearlescent fish have 0 fertility and can't be used for breeding.

## Improving Your Odds

### Rods

Better rods reduce your fishing cooldown **and** increase your rarity bonus. Each rod has a rarity bonus percentage that shifts catches toward higher tiers.

| Rod | Cooldown Reduction | Rarity Bonus | Cost | Level |
|-----|-------------------|--------------|------|-------|
| Basic Rod | 0s | +0% | Free | 1 |
| Wooden Rod | -5s | +5% | 500 coins | 5 |
| Fiberglass Rod | -10s | +10% | 2,000 coins | 10 |
| Carbon Fiber Rod | -15s | +15% | 25,000 coins | 20 |
| Titanium Rod | -20s | +20% | 75,000 coins | 35 |
| Legendary Rod | -25s | +25% | 250,000 coins | 50 |
| Mystic Rod | -30s | +30% | 1,000,000 coins | 75 |
| Pearl Rod | 0s | +0% | 500 pearls | 15 |

The **Pearl Rod** is special — it doesn't boost rarity or reduce cooldown, but it can give fish the exclusive **Pearlescent** trait.

### Your rod caps your total cooldown reduction

Gear, potions, server buffs and guild buffs all shorten your cooldown on top of your rod's own reduction — but there's a **limit on how much they can take off in total**, and that limit rises with every rod tier. Upgrading your rod therefore pays twice: once for the rod's reduction, and again for the extra headroom it unlocks.

You are very unlikely to hit the limit through normal play — a full set of cooldown gear plus a server buff plus a guild mission buff still fits underneath it at every tier. It exists so that a lucky run of crafted gear can't out-cut a rod you haven't earned yet. If you *are* over it, `/gear` says so on the **Cooldown** line and tells you a better rod will raise it.

**Frenzy Potions ignore this limit entirely.** They set your cooldown to a flat few seconds rather than reducing it by a percentage, so they're a full burst regardless of your rod. Server-wide **Fishing Frenzy** events work the same way and are also unaffected.

### Server buffs

Anyone with pearls can buy a buff that applies to **everyone in a Discord server**, from `/shop` → **Server Buffs**. They stack with your own gear and consumables.

| Buff | Effect |
|------|--------|
| ⭐ XP Boost | +20% XP from fishing |
| 🪝 Faster Bites | 20% less waiting for a bite |
| ⏱️ Cooldown Reduction | 10% shorter fishing cooldown |
| 💰 Sell Boost | +15% coins when selling |

There is deliberately **no rarity buff here**. Rare-fish chance is earned — rod, bait, gear, consumables, guild — and never bought.

Buying a buff a server already has **extends** it from its current expiry rather than replacing it, so nothing is wasted by buying early.

The monthly top-server prize, 🏆 **Champion's Bite** (25% less waiting for a bite, 7 days), can't be bought at all and stacks with a purchased Faster Bites.

### Bait

Bait is consumed on each cast and provides a rarity bonus. Some baits work better in specific location types.

| Bait | Rarity Bonus | Best Locations | Cost | Uses |
|------|-------------|----------------|------|------|
| Earthworm | +1% | All | 5 coins | 1 |
| Cricket | +2% | Pond, River, Lake | 10 coins | 1 |
| Minnow | +5% | Lake, River | 25 coins | 1 |
| Shrimp | +8% | Ocean, Deep Sea | 50 coins | 1 |
| Squid | +12% | Deep Sea, Ocean | 500 coins | 1 |
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

### How Net Fishing Works

Your net fills gradually over time in the background — it doesn't matter where you are or what you're doing. However, **the fish are not decided until you collect them**.

When you press `/net collect`:

- **Location matters** — Your net generates fish based on **wherever you're standing right now**, not where you deployed the net
- **Species pool** — The fish come from your current location's species pool
- **No rod or bait bonuses** — Net fish are generated with a basic rod and no bait, so they miss out on the rarity and value boosts you'd get from equipped gear (only the net's own rarity bonus applies)
- **Collection journal** — Your fish count toward the location you collect at, not the location where the net was soaking

**Practical tip:** Travel to the location you want to fish from *before* collecting your net. If you leave a net soaking at Lake Baikal and collect at Svalbard Waters, you'll get Svalbard Arctic fish that count toward your Arctic collection — not Lake Baikal's.

## Chests

There's a ~6% chance to receive a chest when you catch a fish. Chests come in tiers: Common, Rare, Epic, and Legendary. Every chest opens directly from your inventory — no key, no daily limit. Seasonal chests (limited-time event chests) are the rare ones, at about 10% of chest drops.

See the [Economy Guide](economy.md#chests) for more details on chest loot and seasonal variants.

## Random Events

While you're fishing, you might stumble into a random encounter — roughly a **4% chance** each time a session ends, once you're level 3 or higher. Ten different events can appear, from a riddling old angler to a lucky frog, a wishing well, a shooting star, and more.

Every event follows one rule: **it can only help you or do nothing — it's never a loss.** Rewards range from small coin drops to timed buffs (XP, rarity, cooldown, or sell boosts) up to chests and pearls. A few events are puzzles (answer right for the better reward table; a wrong answer still gets you a small consolation prize).

You have 2 minutes to respond before the moment passes with no reward — never a penalty. Events have their own 30-minute cooldown per player, separate from your fishing cooldown.

## Monster Fish

Very rarely (about a 0.5% chance per catch), a massive Monster Fish appears in your channel and kicks off a cooperative boss fight:

1. **Join phase (60 seconds)** — Anyone in the channel can join. At least 3 players are needed for the fight to start; if too few join, the event fizzles out with no cooldown penalty.
2. **The fight (15 rounds, 5 seconds each)** — Each round, click the attack button matching the monster's weak spot. A correct hit scores a point; a miss costs one (never below zero).
3. **Rewards** — The top 3 scorers earn chests: 🥇 Legendary + Seasonal Chest, 🥈 Epic Chest, 🥉 Rare Chest. Ties for a placement are broken randomly, not by who joined first.
4. **Catching the monster** — 1st place also has a chance to reel in the Monster Fish itself as a **Unique**-rarity catch. The base chance is small, but scales up with your equipped rod's rarity bonus — better rods meaningfully improve your odds.

There are 31 unique Monster Fish species that can **only** be caught this way — 10 belonging to each region, plus Zeb's Abyssal Dragonfish, which can surface in any of them.
