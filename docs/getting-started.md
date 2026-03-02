# Getting Started

## Adding CozyCasting to Your Server

Use the `/invite` command in any server that already has the bot, or ask a server admin to add it. The bot needs permissions to send messages, embed links, and use application commands.

## Your First Catch

1. **Type `/fish`** (or `!f fish`) to cast your line.
2. A fish will appear with its species, rarity, traits, and value.
3. Choose **Keep** to add it to your tank, or **Sell** to pocket the coins.

That's it — you're fishing!

## Understanding the Catch Embed

When you catch a fish, you'll see:

- **Species** — The type of fish (depends on your location)
- **Rarity** — From Common to Mythical (see [Rarities](reference/rarities.md))
- **Traits** — Special modifiers like Shiny or Giant that affect value
- **Size** — Each fish has a random size
- **Value** — How many coins you'll get if you sell
- **XP** — Experience points earned for the catch

## What's Next?

- **Check your profile** with `/info` to see your stats
- **View your tank** with `/tank` to see your fish collection
- **Visit the shop** with `/shop` to browse rods and bait
- **Claim daily rewards** with `/daily` for free coins and streak bonuses
- **Check your net** with `/net status` to see passively caught fish
- **Travel** with `/travel` to unlock new fishing spots as you level up
- **Check your level** with `/level` to see progress toward the next milestone

## Slash Commands vs Prefix Commands

CozyCasting supports both styles:

- **Slash commands**: `/fish`, `/shop`, `/travel NA river`
- **Prefix commands**: `!f fish`, `!f shop`, `!f travel NA river` (default prefix: `!f`)

Most commands have short aliases too — for example, `!ff` is the same as `/fish` (prefix `!f` + alias `f`).

Server admins can change the prefix with `/settings prefix` (requires Manage Server permission).
