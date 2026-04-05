# Fishing Commands

The core gameplay loop — cast, catch, keep or sell.

## /fish

Cast your line and catch a fish.

- **Usage:** `/fish`
- **Aliases:** `f`, `catch`
- **Cooldown:** 10 minutes base (reduced by better rods)

When you use `/fish`, a fishing session starts. You'll see a **Cast Line** button to begin your session. If you're on cooldown, you can still cast using a Fishing Ticket — the Cast button will be available, and one ticket will be consumed automatically when you cast.

After catching a fish, you'll see two buttons:

- **Keep** — Adds the fish to your tank
- **Sell** — Sells the fish for coins immediately

## /tank

View your fish tank and collection.

- **Usage:** `/tank [user]`
- **Aliases:** `aquarium`, `fishtank`
- **Examples:** `/tank`, `/tank @friend`

Shows a paginated list of all fish you've kept. You can also view another player's tank.

## /fishinfo

View detailed information about a specific fish.

- **Usage:** `/fishinfo <code>`
- **Aliases:** `fi`, `inspect`
- **Example:** `/fishinfo ABC123DE`

Each fish has a unique 8-character code shown in your tank. Use it to look up species, rarity, traits, size, value, and who originally caught it.

## /sell

Sell a fish from your tank for coins.

- **Usage:** `/sell <code>`
- **Aliases:** `sellfish`
- **Example:** `/sell ABC123DE`

Changed your mind about keeping a fish? Sell it from your tank at any time for its full coin value.

## /namefish

Give a custom name to one of your fish.

- **Usage:** `/namefish <code> <name>`
- **Aliases:** `rename`, `namef`
- **Example:** `/namefish ABC123DE Nemo`
