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

That's it — you're fishing!

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
