# Travel Commands

Explore different fishing locations across the world. Higher-level locations offer better fish and rarer catches.

## /travel

Travel to a different fishing location.

- **Usage:** `/travel <region> <location>`
- **Aliases:** `ftravel`, `goto`
- **Examples:** `/travel NA river`, `/travel asia ocean`

Regions: `NA`, `Asia`, `Europe`, `South America`. Each region has 11 location types (stream, pond, river, lake, reef, ocean, deep sea, cave, shipwreck, volcano, arctic). Locations unlock as you level up. When you level into a new stretch of water, your level-up message names it and points you at `/locations` and `/travel` — this includes every water you cross in one go if a big catch jumps you several levels at once.

## /location

View your current fishing location.

- **Usage:** `/location`
- **Aliases:** `loc`, `where`

Shows where you're currently fishing: the location name, description, its water traits, and the `/collection` checklist for that spot — every species that bites there, ticked off as you catch them. If you're still standing in the Appalachian Stream where you started, the top of your fishing session shows how many other waters are already open to you — this nudge disappears the first time you travel and never returns.

## /locations

View all available fishing locations.

- **Usage:** `/locations`
- **Aliases:** `locs`, `regions`, `places`

One embed with a map and all 44 locations, grouped by region and ordered by the level that unlocks them. Locations you can reach show the base value of the fish there and how much of their species pool you've logged; locked ones show the level you need. Your journal total and its rarity bonus are at the top. You no longer have to read this table to find out something unlocked — level up into new water and the game tells you.

For the species list at any one location, use `/collection <location>`. See the full [Locations Reference](../reference/locations.md) for details.
