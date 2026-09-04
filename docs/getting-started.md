# Getting Started

## Adding CozyCasting to Your Server

Use the `/invite` command in any server that already has the bot, or ask a server admin to add it.

### Permission checklist

CozyCasting **never needs Administrator**. Grant these and you're set:

| | Permission | Why |
|---|---|---|
| **Required** | View Channels | See the channels it's used in |
| **Required** | Send Messages | Reply to commands |
| **Required** | Embed Links | Every response is an embed |
| **Required** | Attach Files | Rendered fish images and profile cards |
| **Required** | Use Application Commands (`applications.commands` scope) | Slash commands — granted during install |
| Trades only | Create Public Threads | Accepted `/trade` sessions run in their own thread |
| Trades only | Send Messages in Threads | Posting inside that trade thread |
| Trades only | Read Message History | Discord requires it for thread workflows |

Permissions are **per channel**. A channel override can deny something the CozyCasting role grants, so one channel goes quiet while the rest work fine. See the [Server Admin guide](commands/server-admin.md#permissions-and-troubleshooting) for how to fix that.

### Direct messages (optional)

**Commands only work inside a server** — you can't fish in a DM with the bot. DMs are only how optional reminders and private invites reach you:

- Cooldown-ready, `/daily`, `/vote`, net-full and come-back reminders
- Trade requests and breeding alerts
- Guild invitations — these fall back to the channel if your DMs are closed, so a closed DM never blocks an invite

Nothing about core fishing needs DMs. To enable them, **right-click the server → Privacy Settings → Direct Messages** (Discord's exact wording varies by client and platform; your global privacy default can also be overridden per server). Once they're on, `/notifications` lets you choose which reminder types you actually get — or turn any of them back off.

## Your First Catch

1. **Type `/fish`** (or `!f fish`) to cast your line.
2. A fish will appear with its species, rarity, traits, and value.
3. Choose **Keep** to add it to your tank, or **Sell** to pocket the coins.
4. **Cast again.** Your first five casts of a session are guaranteed to land while you're under level 10, and your cooldown is only 2 minutes at level 1.

That's it — you're fishing!

## The Starter Chain

Your first few sessions come with a short guided chain — five one-off steps that pay out **the instant you finish them**, no claiming required. They appear on your catch results and at the top of `/quests`.

| Step | What to do | Reward |
|------|------------|--------|
| 🎣 First Cast | Catch your first fish | 100 coins |
| 💰 Cashing In | Sell a fish | 150 coins + 10 bait |
| 🐟 Your First Tank | Keep a fish in your tank | 200 coins |
| 🪱 Bait the Hook | Catch 3 fish while using bait | 250 coins |
| 🌊 A Real Haul | Catch 25 fish | 500 coins, 50 pearls, a Rare Chest |

Between them that's roughly enough to buy your first rod upgrade.

## The Early Game Is Faster

Two things are deliberately generous until level 10, then settle to the normal rules:

- **Cooldowns are short.** 2 minutes at level 1, rising gradually to the standard 15 minutes at level 10.
- **Sessions are safe.** Your first *five* casts can't escape (everyone gets three).

Level 10 is the point where the game opens up — nets, better rods, more locations — so the ramp is there to get you to it.

## Understanding the Catch Embed

When you catch a fish, you'll see:

- **Species** — The type of fish (depends on your location)
- **Rarity** — From Common to Unique (see [Rarities](reference/rarities.md)) — Unique is event-only, so most of your catches will be Common through Mythical
- **Traits** — Special modifiers like Shiny or Giant that affect value
- **Size** — Each fish has a random size
- **Value** — How many coins you'll get if you sell
- **XP** — Experience points earned for the catch

## What's Next?

- **Check your profile** with `/profile` to see your rendered fishing licence card and stats
- **View your tank** with `/tank` to see your fish collection
- **Visit the shop** with `/shop` to browse rods and bait
- **Claim daily rewards** with `/daily` for free coins and streak bonuses
- **Check your net** with `/net status` to see passively caught fish
- **Travel** with `/travel` to unlock new fishing spots as you level up
- **Track your journal** — `/profile` shows how many of the game's species you've caught, and `/collection` shows which ones are still missing. A catch that's new to your journal is flagged on the catch itself.
- **Invite a friend** with `/referral` — you both earn pearls when they reach level 10
- **Check your level** with `/level` to see progress toward the next milestone
- **Share your code** with `/referral` once you're a few levels in

!!! tip "Beginner's Luck"
    Your very first achievement unlock grants a 24-hour buff that makes bites come 75% faster — a great time to fish a lot.

## Slash Commands vs Prefix Commands

CozyCasting supports both styles:

- **Slash commands**: `/fish`, `/shop`, `/travel NA river`
- **Prefix commands**: `!f fish`, `!f shop`, `!f travel NA river` (default prefix: `!f`)

Most commands have short aliases too — for example, `!ff` is the same as `/fish` (prefix `!f` + alias `f`).

Server admins can change the prefix with `/settings prefix` (requires Manage Server permission).
