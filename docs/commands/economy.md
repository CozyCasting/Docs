# Economy Commands

Buy gear, manage your inventory, and check your wallet.

## /shop

Browse the shop for rods, bait, and upgrades.

- **Usage:** `/shop`
- **Aliases:** `store`, `market`

The shop shows available items organized by category (rods, bait, gear, etc.) along with prices, level requirements, and stats.

## /buy

Purchase items from the shop.

- **Usage:** `/buy <type> <item> [quantity]`
- **Aliases:** `purchase`
- **Examples:** `/buy rod wooden_rod`, `/buy bait worm 10`

Item types include `rod`, `bait`, `gear`, and `consumable`. Quantity defaults to 1.

## /wallet

Check your currency balances.

- **Usage:** `/wallet`
- **Aliases:** `bal`, `balance`, `money`

Shows your current coins, pearls, and tickets.

## /inventory

View your items and equipment.

- **Usage:** `/inventory`
- **Aliases:** `inv`, `items`, `bag`

Displays all your rods, bait, chests, consumables, and gear in a categorized view.

## /equip

Equip a rod or bait from your inventory.

- **Usage:** `/equip <type> <item>`
- **Aliases:** `wear`
- **Examples:** `/equip rod wooden_rod`, `/equip bait worm`

You can equip one rod and one bait at a time. Better rods reduce cooldown and boost rarity chances. Bait is consumed on each cast.

## /unequip

Unequip your current bait.

- **Usage:** `/unequip <type>`
- **Aliases:** `remove`
- **Example:** `/unequip bait`

## /gear

View your equipped gear and its stats.

- **Usage:** `/gear`

Shows your currently equipped rod and bait along with their bonuses.

## /gearinfo

View detailed information about a specific piece of gear.

- **Usage:** `/gearinfo <item>`

Shows full stats for any rod or bait including cooldown reduction, rarity bonus, cost, and level requirement.
