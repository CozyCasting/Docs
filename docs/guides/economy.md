# Economy Guide

How to earn and spend your currencies in CozyCasting.

## Currencies

CozyCasting has three currencies:

### Coins

The primary currency. Earned by selling fish, claiming dailies, and from camp income.

**Starting balance:** 100 coins

### Pearls

A premium currency earned through special activities like displaying Pearlescent fish in your camp. Used to buy the Pearl Rod (500 pearls) and other exclusive items.

### Vote Tickets

A currency earned by voting for CozyCasting on bot listing sites. Spend them with the Roaming Trader, who sets up at a fishing location every Thursday. More places to spend them are coming soon.

## Earning Coins

### Selling Fish

The main way to earn coins. Fish value is determined by:

1. **Location base value** — Higher-level locations have higher base values (see the [Locations Reference](../reference/locations.md) for every location type's base value)
2. **Rarity sell multiplier** — Rarer fish are worth much more
3. **Trait multipliers** — Traits like Giant (2x) and Ancient (2.5x) boost the value

The final sell value is: `base_value x rarity_multiplier x trait_multipliers`, with size and weight nudging it up or down a bit further.

For example, a Giant Legendary fish from the Arctic (base value 140) would be worth roughly: 140 x 20 x 2.0 = **5,600 coins**.

Your `/tank` has a **Bulk Sell** button — toggle individual fish or entire pages for sale, then confirm in one click. Fish sitting in your camp Display Tank, or with the Pearlescent trait, are flagged with a warning before you confirm — selling them ends their passive income.

### Daily Rewards

Use `/daily` once every 24 hours to claim:

- **Base reward:** 200 coins
- **Streak bonus:** +25 coins per consecutive day
- **Level bonus:** +5 coins per level
- **Chest chance:** 10% to receive a common chest

### Referral Rewards

Share your referral code with `/referral`. New players can use `/refer <code>` before reaching level 4. When the referred player reaches level 5, **you earn 150 pearls** and **they earn 100 pearls**.

### Weekly & Monthly Contests

Catch the most fish in a week or a month and you'll be paid out automatically once the period ends — see [Contests](../commands/profile.md#contests) for prize details and how to check the live standings.

### Camp Income

Your fishing camp generates passive income from the Display Tank and free bait from the Bait Bin. See the [Camp](#camp) section below for details.

## Spending Coins

### Rods

Your biggest investment. Better rods reduce cooldown and boost rarity odds.

| Rod | Cost | Level |
|-----|------|-------|
| Basic Rod | Free | 1 |
| Wooden Rod | 500 | 5 |
| Fiberglass Rod | 2,000 | 10 |
| Carbon Fiber Rod | 25,000 | 20 |
| Titanium Rod | 75,000 | 35 |
| Legendary Rod | 250,000 | 50 |
| Mystic Rod | 1,000,000 | 75 |

### Bait

Consumable items that boost rarity or add special effects per cast. Ranges from 5 coins (Earthworm) to 6,000 coins (Magic Bait). See the [Fishing Guide](fishing.md) for the full bait table.

### Tank Slot Upgrades

Expand your fish tank capacity with permanent upgrades.

Each Tank Slot upgrade adds 5 additional slots to your storage capacity. Prices scale with each purchase:

| Purchase | Cost |
|----------|------|
| 1st Slot | 2,000 coins |
| 2nd Slot | 3,600 coins |
| 3rd Slot | 6,480 coins |
| 4th Slot | 11,664 coins |
| 5th Slot | 20,995 coins |
| 6th Slot | 37,791 coins |
| 7th Slot | 68,023 coins |
| 8th Slot | 122,442 coins |
| 9th Slot | 220,395 coins |
| 10th Slot | 396,711 coins |

Each subsequent purchase costs 1.8x the previous price (base cost: 2,000 coins).

### Camp Upgrades

Invest in your camp buildings for long-term passive income. See the [Camp](#camp) section below.

## Chests

There's a ~6% chance to receive a chest each time you catch a fish. When one drops, it goes straight into your inventory.

### Core Chests

Core chests come in four tiers:

| Chest | Rolls | Typical Loot |
|-------|-------|--------------|
| Common | 2 | Bait, small coin drops, fishing tickets |
| Rare | 3 | Better bait, consumables, fishing tickets |
| Epic | 4 | Consumables, rare bait, titles |
| Legendary | 5 | Premium consumables (Magnets, etc.), rare titles, gear |

Possible loot from any chest includes coins, pearls, bait, consumables (XP boosts, rarity boosts, Magnets, Double Worms), fishing tickets, titles, and gear.

### Seasonal Chests

Seasonal chests are limited-time event chests (e.g., Summer 2026) with unique loot pools and bonus gear drops. They open directly from your inventory, the same as core chests — no key, no daily limit.

They are rarer instead: when a chest drops from fishing, there's a 90% chance it's a core chest and a 10% chance it's a seasonal chest (if one is currently active).

### Unique Chest

The Unique Chest isn't a fishing drop — it's a reward you win, from a weekly/monthly [contest](../commands/profile.md#contests) or a top-3 finish in a [Monster Fish](fishing.md#monster-fish) event. It always contains a guaranteed Rare-or-better piece of crafted gear. Open it the same way, with `/chest unique`.

### Opening Chests

Use `/chest <type> [amount]` to open chests. You can open up to 25 at once and loot is aggregated into a single summary.

## Gear Salvage

Got more gear than slots? Use `/salvage` to trade in **10 unequipped gear items** for one chest: **60%** Rare, **30%** Epic, **10%** Legendary. Pick which 10 to scrap from a paginated list — equipped gear never shows up as an option, so your loadout is safe. The chest lands unopened, same as any other.

## Camp

The fishing camp is a passive income system that unlocks at **level 15** for **75,000 coins**. Once purchased, your camp earns XP from fishing and levels up to unlock building upgrades.

### Camp Commands

- `/camp view` — View your camp overview, buildings, and display tank
- `/camp buy` — Purchase your camp (level 15+, 75,000 coins)
- `/camp build <building>` — Construct a new building (level 1)
- `/camp upgrade <building>` — Upgrade a building to the next level
- `/camp collect` — Collect accumulated bait and display income
- `/camp display add <fish_code>` — Place a fish in your Display Tank
- `/camp display remove <fish_code>` — Remove a fish from your Display Tank

### Buildings

Your camp has four buildings, each upgradeable up to level 5:

#### Bait Bin

Generates free bait over time. Higher levels produce more bait per cycle and unlock better bait types.

- Generates bait every **2 hours**, stacking up to 12 cycles
- Level 1 produces 1 bait per cycle (mostly Earthworms)
- Level 5 produces 5 bait per cycle with a mix of all bait types
- Collect with `/camp collect`

#### Tackle Shop

Gives you a discount on shop purchases and **camp building upgrades**. Each level adds **5% off**, up to 25% at level 5.

#### Display Tank

Lets you showcase your best fish and earn passive coin and pearl income.

- Each level adds **1 display slot** (up to 5 fish at level 5)
- Displayed fish earn **5% of their value per day** in coins
- Fish with the **Pearlescent** trait (marked 🦪 wherever your fish are listed) earn pearls instead of coins
- Income accumulates for up to 3 days before it caps — collect regularly with `/camp collect`

#### Breeding Tank

Unlock the fish breeding system. Breed two compatible fish to create offspring with inherited traits and rare mutations.

- **Requirements:** Breeding Tank must be built (level 1+)
- **Breeding slots per level:** Level 1–2 = 1 slot, Level 3–4 = 2 slots, Level 5 = 3 slots
- **Breeding time:** 12–24 hours depending on parent rarities. Tank level reduces time (up to 30% faster at level 5)
- **Offspring inheritance:** Species (45% each parent + 10% random), rarity (mostly matches parent avg, 15% up/10% down), traits (40% inherit chance per trait)
- **Breeding-only mutations:** Gilded (3.5× value), Bioluminescent (2.5× value), Colossal (1.8× value + size multiplier)

See the [Fishing Guide](fishing.md#breeding-only-mutations) for details on the special traits that can only appear via breeding.

### Building Costs

Buildings cost coins (and pearls at higher levels) to construct and upgrade:

| Level | Coin Cost | Pearl Cost |
|-------|-----------|------------|
| 1 (Build) | 15,000 | 0 |
| 2 | 40,000 | 0 |
| 3 | 75,000 | 0 |
| 4 | 150,000 | 50 |
| 5 | 300,000 | 150 |

### Camp Levels

Your camp earns XP passively from fishing. Higher camp levels unlock the ability to upgrade buildings further.

| Camp Level | XP Required |
|------------|-------------|
| 1 | 0 |
| 2 | 15,000 |
| 3 | 40,000 |
| 4 | 75,000 |
| 5 | 120,000 |

## Tips

- **Don't sell everything** — Keep rare fish for your collection and achievement progress
- **Use bait wisely** — Expensive bait at low-level locations is wasteful; save it for Ocean+ spots
- **Daily streaks matter** — A 30-day streak gives you +750 bonus coins per claim
- **Upgrade your rod first** — The cooldown reduction lets you fish more often, compounding your earnings over time
- **Display your most valuable fish** — A Legendary fish in the Display Tank earns far more passive income than a Common one
- **Pearlescent fish are display gold** — They generate pearls instead of coins, which are much harder to earn otherwise
- **Collect your camp regularly** — Bait and display income cap out, so don't let resources go to waste
- **Salvage instead of hoarding** — Spare gear you'll never equip is worth more as a chest than as inventory clutter
