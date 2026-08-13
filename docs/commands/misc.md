# Misc Commands

Daily rewards, chests, consumables, camp, breeding, and utility commands.

## /daily

Claim your daily reward.

- **Usage:** `/daily`

Grants coins based on your level and current streak. Consecutive days build a streak bonus (+25 coins per day, plus +5 coins per level). There's also a 10% chance to receive a bonus chest.

## /quests

View and claim your daily quests.

- **Usage:** `/quests`

You get 3 quests per day: 2 shared globally across all players, plus 1 personal quest scaled to your level. Quest types include catching a number of fish, hunting specific rarities, fishing at certain locations, selling goals, and bait usage. Rewards are XP + coins scaled to your level. Quests and the daily reward reset at midnight UTC — a live countdown is shown.

Complete all 3 to earn a bonus chest — usually Common, but a **quest completion streak** (finishing all 3 every day) shifts the odds toward rarer chests the longer it runs, capping out at 30 days.

## /referral

View and share your referral code.

- **Usage:** `/referral`

Share your personal referral code with friends. New players can enter it with `/refer <code>` before reaching level 4. When they hit level 5, you receive **150 pearls** and they receive **100 pearls**. Your referral count also appears on `/profile`.

## /refer

Use a referral code from another player.

- **Usage:** `/refer <code>`

Must be used before you reach level 4. Earns you 100 pearls when you reach level 5.

!!! note "Alt-account protection"
    Referral codes can't be redeemed from a Discord account under 30 days old.

## /chest

Open a chest from your inventory.

- **Usage:** `/chest <type> [amount]`

Chests drop randomly when you catch fish (~6% chance). Core chests (Common, Rare, Epic, Legendary) and seasonal event chests all open directly with no key and no daily limit. Loot includes coins, pearls, bait, consumables, titles, and gear. You can open up to 25 chests at once.

The **Unique Chest** is a special case — it isn't found while fishing. It's the prize for winning a weekly/monthly [contest](profile.md#contests) or placing top 3 in a Monster Fish event, and always contains a Rare-or-better piece of crafted gear.

## /salvage

Trade in spare gear for a chest.

- **Usage:** `/salvage`

Scrap **10 unequipped gear items** for one chest: **60%** chance Rare, **30%** Epic, **10%** Legendary. Pick which 10 to scrap from a paginated list, the same way you'd bulk-sell fish — equipped gear is never shown, so your loadout can't accidentally get scrapped. The chest lands in your inventory unopened, ready for `/chest`.

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

- **Usage:** `/net status` or `/net collect`

Your net automatically gathers fish and occasional items or chests over time while you are away. Use `/net status` to view your current net capacity and what's waiting for you, and use `/net collect` to claim your catches!

### How Net Catches Work

Your net fills gradually with "slots" over time, but **the fish themselves are not decided until you collect**. Here's what that means:

- **Location determines species** — When you press `/net collect`, the fish are generated based on your **current location**, not where you deployed the net
- **Species pool from that location** — You'll get species that normally spawn at wherever you're standing
- **No equipment bonuses** — Net fish are generated with a basic rod and no bait, so they don't get rod/bait/gear bonuses (only your net's own rarity bonus applies)
- **Affects collection journal** — Catches count toward the location where you collect, not the location where the net was soaking

**Practical tip:** If you leave a net soaking at one location and want to collect from a different one, travel there first! The fish will come from the new location and credit your collection journal there. See the [Fishing Guide](../guides/fishing.md#how-net-fishing-works) for more details.

## /collection

View your fishing collection by location.

- **Usage:** `/collection [location]`
- **Aliases:** `journal`, `col`

Track which fish species you've caught at each location. `/collection` shows all 27 locations with a progress bar and what your journal is currently worth; `/collection [location]` shows that location's full checklist and how many species you still need (e.g. `/collection na_stream`).

Filling it out pays off everywhere you fish:

- **Half a location's species** — **+0.25%** rarity
- **All of a location's species** — **+0.5%** rarity, plus that location's artwork as a `/profile` card background ([full list, with how many species each one needs](profile.md#cosmetic-unlocks))
- **All nine locations in a region** — a **Naturalist** title
- **All 27 locations** — the **World Cataloguer** title, **The Complete Journal** achievement with the **Cartographer's Sea** card background, and **+13.5%** rarity in total

The rarity bonus applies at every location, not just the one that earned it, and stacks on top of your rod, bait and buffs. Only fish you caught yourself count — fish received in trades and bred offspring don't.

!!! tip "Net catches count toward collection"
    When you collect fish from your net, they count toward the **location where you collected**, not where the net was deployed. See the [`/net` command](#net) for details.

## /redeem

Redeem a promotional code.

- **Usage:** `/redeem <code>`

Enter a code to claim rewards like coins, bait, consumables, or exclusive items.

## /notifications

Manage your DM notification preferences.

- **Usage:** `/notifications`

An interactive panel with per-type toggles: Master, Fishing Cooldown, Daily Reminder, Vote Reminder, Net Full, and Come Back (win-back) reminders. Turning off the master toggle stops all DMs at once.

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

See the full **[Server Admin guide](server-admin.md)** for all subcommands including notification roles, chest drop channels, rare catch announcements, timezone, and prefix configuration.

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
