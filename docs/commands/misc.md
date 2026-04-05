# Misc Commands

Daily rewards, chests, consumables, camp, breeding, and utility commands.

## /daily

Claim your daily reward.

- **Usage:** `/daily`

Grants coins based on your level and current streak. Consecutive days build a streak bonus (+15 coins per day). There's also a 10% chance to receive a bonus chest.

## /chest

Open a chest from your inventory.

- **Usage:** `/chest <type> [amount]`

Chests drop randomly when you catch fish (~5% chance). Core chests (Common, Rare, Epic, Legendary) open directly with no key required. Seasonal event chests require a Chest Key and have a daily limit based on your level. Loot includes coins, pearls, bait, consumables, titles, and gear. You can open up to 25 chests at once.

## /use

Use a consumable item.

- **Usage:** `/use <item>`

Consumables grant timed buffs like XP boost, rarity boost, or cooldown reduction. View available consumables in your `/inventory`.

## /effects

View your active effects and remaining duration.

- **Usage:** `/effects`

Shows all currently active timed buffs and when they expire.

## /cooldown

Check your fishing cooldown timer.

- **Usage:** `/cooldown`

Shows how much time remains before you can fish again. Better rods reduce your cooldown.

## /camp

View and manage your fishing camp.

- **Usage:** `/camp`

Your camp generates passive income. Upgrade buildings like the Bait Bin, Tackle Shop, Breeding Tank, and Display Tank to increase earnings.

## /breed

Manage your fish breeding sessions.

- **Usage:** `/breed` or `/breed status`

View your active breeding sessions, eggs, and ready-to-hatch fish. Shows breeding tank capacity and how many slots are in use.

### /breed start

Start breeding two compatible fish.

- **Usage:** `/breed start <code1> <code2>`

Begin a breeding session with two fish from your tank. Both fish must be in your tank (not displayed), have fertility ≥ 10, and be compatible (different sexes). Breeding takes 12–24 hours depending on parent rarities. Parents are locked during breeding and cannot be sold or used in other breeding sessions.

### /breed hatch

Begin incubating a ready egg.

- **Usage:** `/breed hatch [session_id]`

Move an egg to the hatching phase. Hatching time depends on the offspring's rarity (0.5–96 hours before tank level reduction). If you have only one egg ready, the session ID is optional.

### /breed collect

Collect a fully hatched fish into your tank.

- **Usage:** `/breed collect [session_id]`

Claim your hatched offspring and add it to your tank. The offspring inherits species, rarity, and traits from its parents, and may have rare breeding-only mutations. If you have only one fish ready to collect, the session ID is optional.

### /breed cancel

Cancel an active breeding session.

- **Usage:** `/breed cancel [session_id]`

Abort a breeding session and return both parents to normal status. Useful if you need the parents for fishing or another session. Fertility is not refunded.

## /net

Manage your passive fishing net.

- **Usage:** `/net status`, `/net collect`

Your net automatically gathers fish and occasional items or chests over time while you are away. Use `/net status` to view your current net capacity and what's waiting for you, and use `/net collect` to claim your catches!

## /redeem

Redeem a promotional code.

- **Usage:** `/redeem <code>`

Enter a code to claim rewards like coins, bait, consumables, or exclusive items.

## /units

Toggle between metric and imperial units.

- **Usage:** `/units`

Switches fish size and weight display between **metric (cm / kg)** and **imperial (in / lbs)**. Your preference is saved per-user. Defaults to imperial.

## /lookup

Look up info about any item.

- **Usage:** `/lookup <query>`
- **Aliases:** `wiki`, `iteminfo`
- **Examples:** `/lookup shrimp`, `/lookup rabbit foot`, `/lookup bamboo rod`

Search for detailed stats on any rod, bait, or consumable. Supports fuzzy matching — you don't need the exact name. Shows rarity boost, cost, level requirement, and other relevant stats for the matched item.

## /settings

Manage server settings (requires Manage Server permission).

- **Usage:** `/settings view`, `/settings prefix <new_prefix>`, `/settings prefix-reset`, `/settings ephemeral <command> <enabled>`

**Subcommands:**

- `/settings view` — View current server settings
- `/settings prefix <new_prefix>` — Set a custom command prefix (1-10 characters)
- `/settings prefix-reset` — Revert to the default prefix
- `/settings ephemeral <command> <enabled>` — Toggle ephemeral (private) responses for specific commands

## /help

Show the interactive help menu.

- **Usage:** `/help [command]`
- **Aliases:** `h`, `commands`

Browse all commands by category or search for a specific command. Use `/help fish` to see details about a particular command.

## /ping

Check bot latency.

- **Usage:** `/ping`

## /invite

Get the bot invite link.

- **Usage:** `/invite`

Share CozyCasting with other servers.
