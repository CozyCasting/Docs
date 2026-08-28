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

- **Usage:** `/tank [user] [sort]`
- **Aliases:** `aquarium`, `fishtank`
- **Examples:** `/tank`, `/tank @friend`, `/tank sort:fertility`

Shows a paginated list of all fish you've kept. You can also view another player's tank. The tank view includes a **Bulk Sell** button. Toggle fish individually or by page, then confirm to sell all at once. Bulk-sell rows show each fish's fertility rather than its size, because that's the number that decides whether a fish is worth keeping to breed with.

**Sort** reorders the whole list, every page and the bulk-sell screen alike:

| Sort | Order |
|------|-------|
| `rarity` | Rarest first, then most valuable — the default |
| `value` | Most valuable first |
| `species` | Species A-Z |
| `fertility` | Highest fertility first |
| `size` | Largest first |
| `newest` / `oldest` | By when you caught it |

Sorting by **size** or by **catch date** also adds that value to each row (📏 42.5 cm, 📅 Jun 01), in your own units — the other sorts order by something the row already shows.

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

## /tournament leaderboard

See the live standings for your server's active tournament.

- **Usage:** `/tournament leaderboard`

If your server has a tournament running, this shows the top 10 standings, each angler's score (weight in kg or fish count depending on the mode), and how much time is left. When there's no tournament, it lets you know so and points admins at `/tournament start`.

Anyone can run this command — no permissions needed to view standings.
