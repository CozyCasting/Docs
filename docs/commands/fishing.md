# Fishing Commands

The core gameplay loop — cast, catch, keep or sell.

## /fish

Cast your line and catch a fish.

- **Usage:** `/fish`
- **Aliases:** `f`, `catch`
- **Cooldown:** 15 minutes base (applied once per session, not per cast; reduced by better rods)

When you use `/fish`, a fishing session starts. You'll see a **Cast Line** button to begin your first cast — it's guaranteed to catch a fish or chest. Subsequent casts have an increasing escape chance.

Consecutive catches build a **streak** with **+1% rarity bonus per catch** (capped at +10%). If you're on cooldown, a **Fishing Ticket** button appears to skip it. Your session ends on a miss or manual stop, and you'll see a summary showing fish caught, kept/sold split, coins earned, XP, chests found, and best streak.

After catching a fish, you'll see two buttons:

- **Keep** — Adds the fish to your tank
- **Sell** — Sells the fish for coins immediately

## /tank

View your fish tank and collection.

- **Usage:** `/tank [user]`
- **Aliases:** `aquarium`, `fishtank`
- **Examples:** `/tank`, `/tank @friend`

Shows a paginated list of all fish you've kept. You can also view another player's tank. The tank view includes a **Bulk Sell** button. Toggle fish individually or by page, then confirm to sell all at once.

## /fishinfo

View detailed information about a specific fish.

- **Usage:** `/fishinfo <code>`
- **Aliases:** `fi`, `inspect`
- **Example:** `/fishinfo ABC123DE`

Each fish has a unique 8-character code shown in your tank. Use it to look up species, rarity, traits, size, value, and who originally caught it.

## /sell

Sell a fish from your tank for coins.

- **Usage:** `/sell <code>` or `/sell <code1>,<code2>,<code3>`
- **Aliases:** `sellfish`
- **Examples:** `/sell ABC123DE` or `/sell ABC123DE,XYZ456FG,QWE789OP`

Changed your mind about keeping a fish? Sell it from your tank at any time for its full coin value. You can also sell multiple fish at once by passing comma-separated codes.

## /namefish

Give a custom name to one of your fish.

- **Usage:** `/namefish <code> <name>`
- **Aliases:** `rename`, `namef`
- **Example:** `/namefish ABC123DE Nemo`
