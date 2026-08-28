# Frequently Asked Questions

## General

### How do I start playing?

Use `/fish` to cast your first line — no setup required. See the [Getting Started](getting-started.md) guide for a quick walkthrough.

### Is CozyCasting free?

The game is free to play, and stays free. Every command works without paying, and pearls — the premium currency — are earned in-game by displaying Pearlescent fish in your camp. **Pearls cannot be bought.**

There is an optional **Supporter** subscription and a one-time **Server Pass** (below). Every command the Bot has stays free — the paid parts are extras on top and a deeper view of the website.

### What can I actually buy?

Two things, both through Discord's own store on CozyCasting's bot profile:

- **Supporter** — a monthly subscription, all of it on `/subscription`: one item of three each week, two perks you pick each month, a monthly profile-card background you keep forever, and the Supporter parts of the website: your Dashboard and the species Journal. Supporter comes at two levels; the higher one also gives you **one 14-day Server Boost Pass a month** to switch on a server buff wherever you play.
- **Server Pass** — a one-time purchase, not a subscription. Activate it and **every purchasable server buff runs for 30 days** in one server of your choosing. It's consumed when you activate it, and it doesn't grant website access.

Discord shows the current price at the point of purchase. Cancel a subscription any time from the same place; you keep access to the end of the period you paid for, and any backgrounds you were granted are yours permanently.

### What does buying *not* get me?

A better chance at rare fish, coins, pearls, or anything random. There are no paid chests, no loot boxes and no surprise rewards — everything sold tells you its exact effect and duration before you buy or activate it. See the [Terms of Service](terms.md#6-purchases) for the full statement.

### Do I need to pay to see my stats?

No. `/profile`, `/collection`, `/gear`, `/achievements` and `/leaderboard` are free in Discord and always will be. The website's Dashboard and Journal are the deeper, sortable version of the same numbers, and those are the Supporter part. The public website — species pages, shared catches, the rare-catch feed, the leaderboard, the Hall of Champions and the Contest Pier — needs no sign-in and no subscription.

### Can I pay for a better chance at rare fish?

No, and this is deliberate. Rare-fish chance comes from your rod, bait, gear, consumables and guild — all earned. The one thing that could be bought with pearls, a server-wide Rarity Boost, was **removed** for exactly this reason, and nothing that can be bought with money touches it either. See the changelog for 0.10.0.

### Does CozyCasting work in DMs?

No, CozyCasting is a server-based bot. All commands must be used inside a Discord server.

DMs are used for one thing only: optional reminders and private guild invitations. Enabling them is not required to play — see [Direct messages](getting-started.md#direct-messages-optional) for what they carry and how to turn them on, and use `/notifications` to control which types you receive.

### What's the image on my `/profile`?

That's your profile card — a rendered "fishing licence" showing your level, stats, and a showcase fish. Customise its background, frame, name style, and stamps with `/card`. If you'd rather see plain text (slow connection, screen reader, or just preference), compact mode replaces it with the classic text-only embed.

### Why is my leaderboard stat different from my profile (`/profile`)?

Leaderboards are cached and update every 5 minutes to keep the bot fast. Your `/profile` profile is always instantly up to date!

---

## Fishing

### Why can't I fish?

You're on cooldown. Use `/cooldown` to see how long until you can cast again. Upgrading your rod reduces the cooldown, and Vote Tickets skip it entirely.

### How do I catch rarer fish?

Three things help: a better **rod** (rarity bonus), **bait** (rarity bonus per cast), and fishing at **higher-level locations**. Stack all three for the best odds.

### What's the difference between Keep and Sell?

- **Keep** — The fish goes into your tank (`/tank`). You can sell it later with `/sell <code>`, display it in your camp, or use it for achievements.
- **Sell** — Immediately converts the fish to coins. You can't get it back.

### What is a fish code?

Each fish you keep gets a unique 8-character code (e.g. `ABC123DE`). Use it with `/fishinfo`, `/sell`, `/namefish`, and `/camp display add`.

### Can I fish at multiple locations?

You can only be at one location at a time. Use `/travel` to move. Higher-level locations have better species, base values, and rarity odds.

### How do I use a Net (Passive Fishing)?

Nets automatically gather fish and items over time without you needing to cast. Use `/net status` to see what your net has collected, and `/net collect` to claim them.

### How do Seasonal Fish work?

During special seasonal events, you have a chance to catch limited-time fish variations. You can use **Seasonal Bait** to get a 50% chance of guaranteeing a Seasonal Variant on your next cast!

### What's a Monster Fish event?

A rare cooperative boss fight that can spawn in your channel while people are fishing. Anyone can join during a 60-second window, then everyone competes in a short reaction minigame. Top 3 finishers win chests, and whoever finishes 1st has a chance to catch the monster itself as a Unique-rarity fish. See the [Fishing Guide](guides/fishing.md#monster-fish) for the full breakdown.

### What are Random Events?

Occasional surprise encounters that can appear when a fishing session ends — a riddle, a lucky frog, a wishing well, and more. They're always a win or a wash; you can never lose anything from one.

---

## Economy

### What are Vote Tickets?

Vote Tickets are a currency earned by voting for CozyCasting on bot listing sites. Spend them with the Roaming Trader, who appears at a fishing location every Thursday with gear and consumables. More places to spend them are coming soon.

### What are Fishing Tickets?

Fishing Tickets are consumables found in chests. When you try to `/fish` while on cooldown and have one in your inventory, it's automatically consumed to skip the cooldown instantly.

### How do I earn Pearls?

Display fish with the **Pearlescent** trait (marked with 🦪 wherever your fish are listed) in your camp's Display Tank. Pearlescent fish generate pearls as passive income instead of coins. The Pearl Rod (bought with pearls) is what gives fish the Pearlescent trait.

### When should I upgrade my rod?

As soon as you can afford it. Rod upgrades reduce cooldown (letting you fish more often) and boost rarity odds. The compounding effect makes them the best long-term investment.

### What do I spend coins on first?

1. **Rod upgrade** — biggest impact on earnings
2. **Camp** (level 15+) — passive income
3. **Bait** — situational, save for high-level locations

---

## Camp

### When does the camp unlock?

At **level 15**, for **75,000 coins**.

### What's the best building to upgrade first?

The **Bait Bin** for free bait, or the **Display Tank** if you have Pearlescent fish. The **Tackle Shop** discount pays off over time if you buy a lot of bait, and it also applies a discount to the cost of other camp building upgrades!

### How often should I collect from camp?

At least once every 3 days — that's when Display Tank income caps. Bait Bin stacks up to 12 cycles (every 2 hours), so collecting daily is ideal.

---

## Trading

### How do I send items to another player?

Use `/give @player <item>` for a quick one-way transfer (no acceptance needed), or `/trade @player` to open an interactive session where both sides can put up multiple items and accept when ready.

### What items can I trade?

You can trade coins, pearls, vote tickets, fish (from your tank), gear, rods, bait, chests, and most consumables. A few consumables are not tradeable: Title Pouch, Fishing Pass, Fishing Journal, Shopping Card, and Twin Hook Token.

### Can I cancel a trade after accepting?

Not after both players have accepted — the trade executes immediately and cannot be undone. However, if only you have accepted and the other player hasn't yet, either player can cancel. Adding or removing any item also resets both acceptances.

### Why did my acceptance reset?

If either player modifies their offer after you accepted, both acceptances clear automatically. This prevents bait-and-switch. Just review the updated offer and accept again when you're happy with it.

---

## Items & Commands

### How do I look up item stats?

Use `/lookup <name>` — it searches rods, baits, and consumables with fuzzy matching. Example: `/lookup shrimp` or `/lookup bamboo`.

### How do I change my fish size display to metric?

Use `/units` to toggle between imperial (in/lbs) and metric (cm/kg).

### How do I open a chest?

Use `/chest <type>` — for example `/chest common` or `/chest rare 5`. Every chest, core or seasonal, opens straight from your inventory with no key and no daily limit.

### What do consumables do?

Consumables grant timed buffs: XP boost, rarity boost, sell boost, or cooldown reduction. Rare items like **Magnets** and **Lucky Double Worms** give special effects, like drawing in specific traits or a 15% chance to catch two fish at once! Use them with `/use <item>` and check active effects with `/effects`.

**Only one buff of each type runs at a time**, so drinking a Schnapps while an Ale is active isn't possible — finish or wait out the first. That's why the stronger version of a buff simply replaces the weaker one rather than stacking with it. **Frenzy Potions** are the exception to the usual cooldown rules: they set your cooldown to a flat few seconds rather than reducing it by a percentage, ignoring the [rod cooldown limit](guides/fishing.md#your-rod-caps-your-total-cooldown-reduction) completely.

### What do I do with spare gear I'll never equip?

Use `/salvage` to trade in 10 unequipped gear items for a chest (60% Rare / 30% Epic / 10% Legendary odds). Equipped gear is never shown as an option, so your current loadout is always safe.
