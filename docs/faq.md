# Frequently Asked Questions

## General

### How do I start playing?

Use `/fish` to cast your first line — no setup required. See the [Getting Started](getting-started.md) guide for a quick walkthrough.

### Is CozyCasting free?

Yes, completely free to play. Pearls (the premium currency) are earned in-game by displaying Pearlescent fish in your camp.

### Does CozyCasting work in DMs?

No, CozyCasting is a server-based bot. All commands must be used inside a Discord server.

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

### What do I do with spare gear I'll never equip?

Use `/salvage` to trade in 10 unequipped gear items for a chest (60% Rare / 30% Epic / 10% Legendary odds). Equipped gear is never shown as an option, so your current loadout is always safe.
