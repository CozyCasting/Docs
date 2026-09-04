# Misc Commands

Daily rewards, chests, consumables, camp, breeding, and utility commands.

## /daily

Claim your daily reward.

- **Usage:** `/daily`

Grants coins based on your level and current streak. Consecutive days build a streak bonus (+25 coins per day, plus +5 coins per level). There's also a 10% chance to receive a bonus chest.

## /quests

View and claim your daily quests.

- **Usage:** `/quests`

You get 3 quests per day: 2 shared globally across all players, plus 1 personal quest scaled to your level. Quest types include catching a number of fish, hunting specific rarities, fishing at certain locations, selling goals, bait usage, opening chests, session streaks, and — once you own one — collecting from your net. Rewards are XP + coins scaled to your level. Quests and the daily reward reset at midnight UTC — a live countdown is shown.

If you haven't finished the **starter chain** yet, its current step sits at the top of this embed. Starter steps are one-off, pay out the instant you complete them, and don't need claiming. See [Getting Started](../getting-started.md#the-starter-chain).

Complete all 3 to earn a bonus chest — usually Common, but a **quest completion streak** (finishing all 3 every day) shifts the odds toward rarer chests the longer it runs, capping out at 30 days.

## /referral

View and share your referral code.

- **Usage:** `/referral`

Share your personal referral code with friends. New players can enter it with `/refer <code>` before reaching level 4. When they hit level 10, you receive **150 pearls** and they receive **100 pearls**. Your referral count also appears on `/profile`.

## /refer

Use a referral code from another player.

- **Usage:** `/refer <code>`

Must be used before you reach level 4. Earns you 100 pearls when you reach level 10.

!!! note "Alt-account protection"
    Referral codes can't be redeemed from a Discord account under 30 days old.

## /chest

Open a chest from your inventory.

- **Usage:** `/chest <type> [amount]`

Chests drop randomly when you catch fish (~6% chance). Core chests (Common, Rare, Epic, Legendary) and seasonal event chests all open directly with no key and no daily limit. Loot includes coins, pearls, bait, consumables, titles, and gear. You can open up to 25 chests at once.

The **Unique Chest** is a special case — it isn't found while fishing. It's the prize for winning a Contest Pier competition or placing top 3 in a Monster Fish event, and always contains a Rare-or-better piece of crafted gear.

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

Abort a breeding session and return both parents to normal status. Useful if you need the parents for fishing or another session. Cancel within 15 minutes of starting and the fertility cost is refunded to both parents; after that, fertility is not refunded.

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

Track which fish species you've caught at each location. `/collection` shows all 44 locations with a progress bar and what your journal is currently worth; `/collection [location]` shows that location's full checklist and how many species you still need (e.g. `/collection na_stream`).

Filling it out pays off everywhere you fish:

- **Half a location's species** — **+0.25%** rarity
- **All of a location's species** — **+0.5%** rarity, plus that location's artwork as a `/profile` card background ([full list, with how many species each one needs](profile.md#cosmetic-unlocks))
- **All eleven locations in a region** — a **Naturalist** title
- **All 44 locations** — the **World Cataloguer** title, **The Complete Journal** achievement with the **Cartographer's Sea** card background, and **+22%** rarity in total

The rarity bonus applies at every location, not just the one that earned it, and stacks on top of your rod, bait and buffs. Only fish you caught yourself count — fish received in trades and bred offspring don't.

### Special Waters

Below the 44 locations is **Special Waters**, holding the fish that belong to no location: the 31 **Monster Fish** you win from an event, and the **seasonal exclusives** you catch with seasonal bait. `/collection special_monster` and `/collection special_seasonal` show each checklist.

**Special Waters counts toward nothing** — not the rarity bonus, not the Naturalist titles, not World Cataloguer, not The Complete Journal, and not the percentage at the top of `/collection`. A season that has ended and an event you weren't around for are both permanently out of reach, so no reward is gated behind them. It exists so the fish you caught have somewhere to be.

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

## /globalfeed

Choose whether your rare catches appear on the public website feed.

- **Usage:** `/globalfeed`

CozyCasting's website carries a live feed of **Mythical and Unique** catches from across every server. Entries show the fish, its size, weight and value, and the location — publicly, to anyone, with no sign-in.

**The angler's name is the part that is opt-in.** Your catches are named there only where a server admin has turned names on with `/settings globalfeed`; everywhere else they read "Anonymous Angler". A catch on its own names nobody: no name, no Discord ID, no server.

`/globalfeed` is your own switch, and it is the stronger one — opting out keeps your catches off the feed altogether, in every server, immediately, whatever an admin has set. It applies to **future catches**, and it also **takes your name off the catches already on the feed**, straight away. Those fish stay there unnamed until they age off — the feed holds the most recent 200 catches, so that happens on its own.

The same page also carries **game-wide totals** — how many fish have been caught across every server, how many anglers play, the split by rarity, and the heaviest fish ever landed. Those are aggregates only: they never name anyone, so `/globalfeed` has nothing to do with them and there is nothing to opt out of. The heaviest-fish tile shows the fish and never who caught it.

## /contest

Visit the **Contest Pier** — the weekly competition where nothing you own matters.

- **Usage:** `/contest`
- **Aliases:** `pier`

Your rod, bait, gear, level, current location, buffs and consumables count for **nothing** at the pier. Every angler casts the same water and rolls from the same species. A level 1 player and a level 100 player have identical odds.

### Ten casts a day

You get **10 casts a day**, reset at **00:00 UTC**. They **do not roll over** — an unused cast is gone at midnight, and no attempt is ever earned, bought or refilled. Fish all seven days and that is 70 casts for the week.

Every cast is recorded the instant it happens, whether or not the message gets through, so you can stop and come back — `/contest` is always the authoritative count.

### The pier moves every day

Each day of the week is a **different stretch of water** with its own species — an Appalachian stream one day, a volcanic caldera the next — and the whole week's schedule is posted in advance on `/contest` and on the [website](../website.md).

That schedule is the only decision the contest offers. Fish from a deep or volcanic water are appraised higher than a stream's, so where the pier stands decides what a day's ten casts are worth. It is the same water and the same timetable for everybody.

### The competitions

Three of these five run each week, picked when the week opens and locked in for its duration:

| Competition | Wins with |
|---|---|
| 🐋 Biggest Catch | Your single longest fish of the week |
| 🐟 Smallest Catch | Your single shortest fish of the week |
| 💎 Richest Haul | The appraised value of everything you land |
| 📖 Widest Variety | How many different species you land |
| 🎯 Target Size | One fish as close to the posted target length as you can get |

Exact ties are **co-winners** — casting earlier breaks nothing.

### What you get, and what you don't

Contest fish are measured, photographed and released. **No coins, no XP, no tank, no journal, no achievements, no leaderboard progress** — nothing from the pier touches your normal game.

Winning a competition pays 🦪 **50 Pearls** and a 🎁 **Unique Chest**, plus that competition's **permanent title**. The Pearls and the chest are paid on every win, including a repeat; the title you only earn once. Titles cannot be traded and change nothing about how you fish. Three competitions run each week, so a clean sweep is 150 Pearls and three chests.

The week runs **Saturday 00:00 UTC to Saturday 00:00 UTC** — Friday evening across the Americas — and settles the moment it ends.

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
