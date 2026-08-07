# Guild Commands

Found a player-run guild, recruit members, manage your guild bank, and build guild camps to unlock server-wide bonuses.

## /guild

View a guild's profile including name, tag, level, member count, and current mission progress.

- **Usage:** `/guild [name]`
- **Aliases:** `guild info`
- **Examples:** `/guild`, `/guild Fishmongers`, `/guild FM`

If you don't specify a guild name, it shows your own guild's profile. To look up another guild, search by exact name or tag (case-insensitive).

---

## Guild Setup

### /guild create

Found a new guild using a Guild Token. Costs 1,000,000 coins.

- **Requires:** Guild Token (purchasable from `/shop`)
- **Rewards:** You become the Owner and can start inviting members

To create a guild:
1. Buy a Guild Token from `/shop` (1,000,000 coins)
2. Use `/guild create` or `/use guild_token`
3. Click **Found Guild**
4. Enter your guild name (2–24 characters: letters, numbers, spaces, apostrophes, hyphens, periods)
5. Enter your guild tag (3–5 letters or numbers only)

Both the name and tag must be unique (case-insensitive). If your name or tag is rejected, the token stays in your inventory — you can try again.

**One guild per player.** If you leave or are kicked, you must wait 24 hours before founding or joining another guild.

---

## Membership

### /guild invite

Invite a player to join your guild (Owner/Mod only).

- **Usage:** `/guild invite @user`
- **Cooldown:** None
- **Requires:** You must be the Owner or a Mod

The invitee receives a private message with **Accept** and **Decline** buttons. The invite expires after **7 days**.

If their DMs are closed, the invite posts in the channel instead.

**Pending invite cap:** A guild can have up to **20 outstanding invites**, and never more than the number of free roster slots.

### /guild members

View your guild's roster, paginated by 10 members per page.

- **Usage:** `/guild members`

**Members see:** Rank, join date

**Owner/Mod see:** Member level, last fish time, ⭐ guild XP contributed and 🪙 coins donated — ranked by XP contributed, so it doubles as a leaderboard for who's carrying the guild

---

### /guild promote

Promote a Member to Mod (Owner only).

- **Usage:** `/guild promote @member`

### /guild demote

Demote a Mod back to Member (Owner only).

- **Usage:** `/guild demote @mod`

### /guild kick

Remove a member from your guild (Owner/Mod only).

- **Usage:** `/guild kick @member`
- **Mod restriction:** Mods can only kick Members, not other Mods or the Owner

The removed member is notified via DM.

### /guild leave

Leave your guild voluntarily.

- **Usage:** `/guild leave`
- **Cooldown:** 24 hours before you can join or found another guild

If you're the Owner and no other Mods exist, the oldest Member becomes Owner. If no members remain, the guild is disbanded and the chest is destroyed with no refund.

### /guild disband

Disband your guild and destroy all its contents (Owner only, requires confirmation).

- **Usage:** `/guild disband`

**Warning:** This destroys the guild bank and chest contents with no refund. Confirm before proceeding.

---

## Guild Bank & Chest

### /guild chest

View the guild chest contents (items and balances).

- **Usage:** `/guild chest`

Shows all coins, pearls, logs, stone, and the 25+ item slots (capped by Storehouse tier).

### /guild chest add

Deposit items or currency into the guild chest (any member).

- **Usage:** `/guild chest add <item> <quantity>`
- **Examples:**
  - `/guild chest add coins 500000`
  - `/guild chest add pearls 100`
  - `/guild chest add worm 50`
  - `/guild chest add materials_bag 3`

Only **coins and pearls** can pay for `/guild upgrade`. Materials and items cannot.

Deposits are **not escrowed** — everything in the chest stays spendable on camp upgrades until `/guild upgrade` actually spends it.

### /guild chest remove

Withdraw items from the guild chest (Owner/Mod only).

- **Usage:** `/guild chest remove <item> <quantity>`

### /guild chest log

View an audit trail of all deposits and withdrawals (Owner/Mod only).

- **Usage:** `/guild chest log`

Shows paginated history of every coin, pearl, and item movement in the guild bank.

---

## Guild Camp

### /guild camp

View the guild camp: current building tiers, their buffs, and production status.

- **Usage:** `/guild camp`

Shows:
- **7 buildings:** Logging Camp, Stone Camp, Lure Workshop, Library, Chapel, Storehouse, Bait Hut
- **Each building's tier** (0–5) and current buff
- **Material production status** (logs/stone generation)
- **Item storage capacity**

### /guild camp upgrade

Upgrade a guild building to the next tier (Owner/Mod only).

- **Usage:** `/guild camp upgrade <building>`
- **Requirements:**
  - Building tier cannot exceed guild level (e.g., a level 3 guild cannot build tier 5 buildings)
  - Guild chest must have sufficient coins, logs, stone, and pearls
  - Costs are per building and paid from the guild bank

**Example progression:** Tier 1→2→3→4→5

All upgrades are permanent. After confirmation, costs are deducted from the guild bank immediately.

#### Building Specs & Costs

| Building | Tier 1 | Tier 2 | Tier 3 | Tier 4 | Tier 5 |
|----------|--------|--------|--------|--------|--------|
| **Lure Workshop** | 250K 🪙<br/>50 🪓<br/>40 ⛏️ | 750K 🪙<br/>150 🪓<br/>120 ⛏️ | 2M 🪙<br/>400 🪓<br/>320 ⛏️ | 5M 🪙<br/>900 🪓<br/>750 ⛏️<br/>50 💎 | 12M 🪙<br/>2K 🪓<br/>1.7K ⛏️<br/>150 💎 |
| **Library** | 250K 🪙<br/>50 🪓<br/>40 ⛏️ | 750K 🪙<br/>150 🪓<br/>120 ⛏️ | 2M 🪙<br/>400 🪓<br/>320 ⛏️ | 5M 🪙<br/>900 🪓<br/>750 ⛏️<br/>50 💎 | 12M 🪙<br/>2K 🪓<br/>1.7K ⛏️<br/>150 💎 |
| **Chapel** | 250K 🪙<br/>50 🪓<br/>40 ⛏️ | 750K 🪙<br/>150 🪓<br/>120 ⛏️ | 2M 🪙<br/>400 🪓<br/>320 ⛏️ | 5M 🪙<br/>900 🪓<br/>750 ⛏️<br/>50 💎 | 12M 🪙<br/>2K 🪓<br/>1.7K ⛏️<br/>150 💎 |
| **Bait Hut** | 250K 🪙<br/>50 🪓<br/>40 ⛏️ | 750K 🪙<br/>150 🪓<br/>120 ⛏️ | 2M 🪙<br/>400 🪓<br/>320 ⛏️ | 5M 🪙<br/>900 🪓<br/>750 ⛏️<br/>50 💎 | 12M 🪙<br/>2K 🪓<br/>1.7K ⛏️<br/>150 💎 |
| **Storehouse** | Same as above | Same | Same | Same | Same |
| **Logging Camp** | Same as above | Same | Same | Same | Same |
| **Stone Camp** | Same as above | Same | Same | Same | Same |

Key: 🪙 = coins, 🪓 = logs, ⛏️ = stone, 💎 = pearls

#### Building Effects

**Lure Workshop** — fish bite 3% sooner per tier for every member  
**Library** — +3% catch XP per tier for every member  
**Chapel** — +1% rare fish chance per tier for every member  
**Bait Hut** — +5% chance per tier that a catch doesn't consume your bait  
**Storehouse** — +25 guild chest item slots per tier (up to 150 total)  
**Logging Camp** — Produces logs daily: tier × active members × 2 (active = fished in last 3 days)  
**Stone Camp** — Produces stone daily: tier × active members × 2 (active = fished in last 3 days)

Materials are deposited automatically into the guild bank and capped at 500 per cycle.

---

## Guild Level & Bonuses

Guilds level up from **Level 1 to Level 5** with `/guild upgrade` (Owner/Mod only).

### /guild upgrade

Raise the guild one level. Requires **all three**:

- ⭐ **Guild XP** — earned automatically as members fish. It never goes down, and it is only *checked*, never spent.
- 🪙 **Coins** and 🦪 **Pearls** — **spent** out of the guild chest, permanently.

- **Usage:** `/guild upgrade`

`/guild info` always shows how you're tracking against all three.

### Level Thresholds

| Level | Guild XP | Coins | Pearls | Max Members | Sell Bonus | XP Bonus |
|-------|----------|-------|--------|-------------|-----------|----------|
| 1 | — | — | — | 10 | — | — |
| 2 | 350,000 | 25,000,000 | 250 | 20 | +2% | +2% |
| 3 | 1,000,000 | 75,000,000 | 750 | 30 | +4% | +4% |
| 4 | 2,000,000 | 200,000,000 | 2,000 | 40 | +6% | +6% |
| 5 | 3,500,000 | 500,000,000 | 5,000 | 50 | +8% | +8% |

Guild XP comes **only from fishing** — every point of catch XP a member earns is mirrored into the guild automatically, boosts included. Quest rewards, redeem codes and admin grants do not count. A member leaving never lowers the guild's total.

Each guild level above 1 grants all members a **+2% sell value** and **+2% catch XP** bonus (stacking with camp building bonuses).

---

## Weekly Guild Missions

Every week, all guilds compete on the same rotating mission. Completing it grants all members a **−5% fishing cooldown** buff for the following week.

### /guild mission

View the current week's mission, your guild's progress, and top contributors.

- **Usage:** `/guild mission`

Shows the mission name, goal, current progress, and a leaderboard of members' contributions.

### Mission Types

**Full Nets** — Catch fish with `/fish`. Goal: 100 per member (scaled by member count at week start)

**Market Rush** — Earn coins by selling. Goal: 50,000 coins per member

**Trophy Hunt** — Catch Rare-or-better fish with `/fish`. Goal: 10 per member

Missions rotate weekly. Only active `/fish` catches count — nets and breeding do not.

---

## Materials & Drops

### Materials Bags

While fishing, about **8% of successful catches** drop a free **Materials Bag** that doesn't consume a cast (fishing odds and chest chances are unaffected).

- **Usage:** `/use materials_bag`
- **Rewards:** 3–8 logs and 2–6 stone

Bags can also drop from Epic and Legendary chests. Materials go into a **Materials tab** in your `/inventory`.

### Guild Materials

Logs and stone are used for guild camp upgrades. The guild chest holds them as slotless balances.

---

## Tips

- **Founding costs 1 million coins** — save up or join an existing guild to start building immediately
- **Donating doesn't lock money away** — deposited coins and pearls stay spendable on camp until an upgrade spends them
- **Money alone can't level a guild** — you need guild XP too, and the only way to earn it is members fishing
- **Level matters for building** — you can't upgrade a building past your guild level
- **Active members count** — Logging/Stone camps produce more when more members have fished recently
- **Missions are global** — the same mission runs for every guild each week, so coordination helps
- **Materials scale** — budget time for high-tier camp upgrades; early tiers are cheap, tier 4–5 are expensive
