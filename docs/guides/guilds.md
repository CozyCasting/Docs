# Guilds Guide

Player-run guilds are communities that pool resources, build upgrades, and compete on weekly missions. Guilds are end-game content for experienced players looking for cooperative gameplay and shared benefits.

## When Should You Join or Start a Guild?

### Good times to join:
- You've reached **level 10+** and understand fishing basics
- Your server has active players forming a guild
- You want passive bonuses every member shares — sell value and XP from guild level, plus catch XP, rare chance, faster bites and saved bait from camp buildings
- You want to help complete **weekly missions** for cooldown buffs

### Good times to found:
- You have **1 million coins** saved up
- You want to be Owner and lead a community
- Your server has several active players interested in joining

### Solo fishing is fine too:
Guilds are entirely optional. Solo players can level, collect fish, and enjoy the game without joining.

---

## Guild Ranks & Permissions

Guilds have three ranks with different permissions:

### Owner
- Invite and kick any member
- Promote Members to Mod, demote Mods to Member
- Manage guild camp (view, upgrade buildings)
- Manage guild chest (view, deposit, withdraw, audit log)
- Disband the guild
- Leave (hands ownership to oldest Mod, then oldest Member)

### Mod
- Invite Members and Mods
- Kick Members only (not other Mods or Owner)
- Manage guild chest (view, deposit, withdraw, audit log)
- Manage guild camp (view, upgrade buildings)
- View guild roster with detailed stats

### Member
- Deposit items/currency to the guild chest
- View guild roster (basic info only)
- View guild chest contents
- View guild profile and current mission
- Leave voluntarily (30-minute cooldown before joining another guild)

---

## Founding & Joining

### Founding a Guild

1. Buy a **Guild Token** from `/shop` for **1,000,000 coins**
2. Use `/guild create` or `/use guild_token`
3. Click **Found Guild** in the prompt
4. Enter your **guild name** (2–24 characters: letters, numbers, spaces, apostrophes, hyphens, periods)
5. Enter your **guild tag** (3–5 letters or numbers: `FM`, `CFH`, `WAVE`, etc.)

The name and tag must be unique (case-insensitive). The token is only consumed on success.

**You become the Owner.** One guild per player.

### Joining a Guild

An Owner or Mod invites you with `/guild invite @you`. You'll receive:
- A **private DM** with Accept/Decline buttons (if DMs are open)
- Or an **in-channel invite** if your DMs are closed

You have **7 days** to accept. Click **Accept** to join immediately.

**Invite cap:** A guild can have up to **20 pending invites**, limited by free roster slots.

### Leaving or Being Kicked

- **Leave voluntarily** with `/guild leave` (24-hour cooldown before joining/founding another)
- **Kicked by Owner/Mod** (24-hour cooldown applies)
- **Owner leaves** → hands control to oldest Mod, then oldest Member
- **Guild becomes empty** → guild disbands and chest is destroyed

---

## Guild Level & Thresholds

Guild level (1–5) is raised by the Owner or a Mod running `/guild upgrade`. It never goes up on its own, and it never goes down.

An upgrade requires **all three** of:

| Requirement | Where it comes from | Spent? |
|---|---|---|
| ⭐ **Guild XP** | Members fishing | **No** — checked only |
| 🪙 **Coins** | The guild chest | Yes, permanently |
| 🦪 **Pearls** | The guild chest | Yes, permanently |

### Guild XP — the one you can't buy

Every point of catch XP a member earns is mirrored into the guild automatically, boosts and all. There's no "donate XP" command; playing the game **is** the contribution. XP from quests, redeem codes and admin grants does not count — this counter measures fishing.

Guild XP is a lifetime total that **never decreases**. If a member leaves or is kicked, everything they earned stays banked in the guild.

The XP requirement is tuned so that a typical roster clears about one level every **two weeks**. This is deliberate: one rich member can cover the coin cost overnight, but nobody can shortcut the requirement that people actually fish together.

### Thresholds

| Level | Guild XP | Coins | Pearls |
|-------|----------|-------|--------|
| 2 | 350,000 | 25,000,000 | 250 |
| 3 | 1,000,000 | 75,000,000 | 750 |
| 4 | 2,000,000 | 200,000,000 | 2,000 |
| 5 | 3,500,000 | 500,000,000 | 5,000 |

Each level's cost is paid fresh — nothing carries over from the previous tier.

`/guild info` shows all three bars with your current progress, so you always know which one is holding you back. `/guild members` shows each member's XP contribution, ranked.

**Deposits are not escrowed** — coins and pearls in the chest stay spendable on camp buildings right up until `/guild upgrade` actually spends them. Withdrawing money never demotes a guild.

### Membership & Slots

- **Level 1:** 10 member slots
- **Level 2:** 20 slots (+10 per level)
- **Level 3:** 30 slots
- **Level 4:** 40 slots
- **Level 5:** 50 slots

### Member Bonuses

Each level grants all members (including Owner):

| Level | Sell Bonus | XP Bonus |
|-------|-----------|----------|
| 2 | +2% | +2% |
| 3 | +4% | +4% |
| 4 | +6% | +6% |
| 5 | +8% | +8% |

These stack with individual rods, buffs, and camp building bonuses — they're pure guild-wide additions.

---

## Guild Bank & Chest

The guild chest stores:

- **Coins** (slotless balance)
- **Pearls** (slotless balance)
- **Logs** (slotless balance)
- **Stone** (slotless balance)
- **Items** (25 slots, +25 per Storehouse tier, up to 150 max)

### Deposits

Any member can deposit with `/guild chest add <item> <quantity>`:
- Coins and pearls are what `/guild upgrade` spends
- Materials (logs, stone) and items can't pay for a level, but are essential for camp upgrades
- Depositing is free and instant

### Withdrawals

Only Owner/Mod can remove items with `/guild chest remove <item> <quantity>`. You need sufficient balance in the chest.

### Audit Log

Owner/Mod can view a full audit trail with `/guild chest log` showing every deposit and withdrawal with timestamps.

### Disbanding Warning

If the guild is disbanded (Owner only), **all chest contents are destroyed with no refund**. There's no selling leftovers or returning to members — it's gone.

---

## Guild Camp: Buildings & Production

The guild camp has **7 buildings**, each upgradeable independently from tier 1–5. Buildings provide member buffs and/or resource generation.

### Buff Buildings

These give members passive bonuses when the building is upgraded:

**Lure Workshop** (🪝)  
Fish bite 3% sooner per tier. Tier 5 = fish bite 15% sooner for every member.

**Library** (📚)  
+3% catch XP per tier. Tier 5 = +15% XP for every member.

**Chapel** (⛪)  
+1% rare fish chance per tier. Tier 5 = +5% rarity boost for every member.

**Bait Hut** (🪱)  
+5% chance per tier that a catch doesn't consume your bait. Tier 5 = 25% chance to save bait.

### Production Buildings

These auto-generate materials every 24 hours:

**Logging Camp** (🪓)  
Produces logs: tier × active members × 2 per day.

**Stone Camp** (⛏️)  
Produces stone: tier × active members × 2 per day.

"Active" means the member fished within the last 3 days. Materials are deposited automatically, capped at 500 per day.

Example: A guild with Logging Camp tier 3 and 10 active members produces 3 × 10 × 2 = 60 logs per day.

### Storage

**Storehouse** (🏚️)  
+25 item slots per tier. Default 25, tier 5 = 150 total slots.

### Building Tier Caps

A building's tier **cannot exceed the guild's level**. A level 2 guild can build tier 2 buildings at most. Leveling up the guild unlocks higher tiers.

### Upgrade Costs

All buildings use the same cost ladder (per tier):

| Tier | Coins | Logs | Stone | Pearls |
|------|-------|------|-------|--------|
| 1 | 250,000 | 50 | 40 | — |
| 2 | 750,000 | 150 | 120 | — |
| 3 | 2,000,000 | 400 | 320 | — |
| 4 | 5,000,000 | 900 | 750 | 50 |
| 5 | 12,000,000 | 2,000 | 1,700 | 150 |

The guild chest must have all required materials (coins, logs, stone, pearls). Costs are deducted on confirmation.

### Budget Example: Lure Workshop

To max out Lure Workshop (tier 5):
- Tier 1: 250K coins + 50 logs + 40 stone
- Tier 2: 750K coins + 150 logs + 120 stone
- Tier 3: 2M coins + 400 logs + 320 stone
- Tier 4: 5M coins + 900 logs + 750 stone + 50 pearls
- Tier 5: 12M coins + 2K logs + 1.7K stone + 150 pearls
- **Total: 20M coins + 3,500 logs + 2,930 stone + 200 pearls**

This is a multi-month project for most guilds.

---

## Weekly Guild Missions

Every week, one global mission is assigned to all guilds. Completing it grants **−5% fishing cooldown** (faster fishing) for all members the following week.

### Mission Mechanics

- **Goal scales by member count** at the start of the week (snapshotted, so changes mid-week don't affect progress)
- **Only active `/fish` catches count** (not nets, not breeding)
- **Any member can contribute** to progress
- **Progress is visible** in `/guild mission` with a leaderboard of top contributors

### Three Rotating Missions

**Full Nets** (🐟)  
Catch fish. Goal: 100 per member (e.g., 10-member guild needs 1,000 catches).

**Market Rush** (🪙)  
Earn coins from selling. Goal: 50,000 coins per member (e.g., 10-member guild needs 500,000 coins total).

**Trophy Hunt** (✨)  
Catch Rare-or-better fish. Goal: 10 per member (e.g., 10-member guild needs 100 rare+ catches).

### Bonus Timing

The cooldown buff applies for **7 days** starting the week after completion. If a guild fails the mission, they don't get the buff that week — try again next week.

---

## Materials & Fishing Drops

### Materials Bags

About **8% of successful fishing catches** drop a free **Materials Bag**.

- **Doesn't count as a catch** — it's a bonus on top, so your next fish is exactly as likely to stay on the line
- **Chest odds unaffected** — the bag doesn't change your 6% chest chance
- **Usage:** `/use materials_bag` opens it for 3–8 logs and 2–6 stone
- **Also drop from chests** — Epic and Legendary chests can contain Materials Bags

### Materials Tab

Logs and stone appear in a **Materials tab** in your `/inventory`, separate from regular items.

---

## Coordination Tips

### For Owners

- **Set a donation target** — Levels cost 25–500M coins + 250–5K pearls out of the chest (shared effort)
- **Recruit anglers, not wallets** — guild XP only comes from members fishing, so an active roster is the one thing money can't replace
- **Plan camp upgrades** — Start with Lure Workshop or Library for universal buffs
- **Assign Mods early** — Mods can invite and manage the chest while you're offline
- **Communicate with members** — Use your server chat to coordinate material farming and mission pushes

### For Mods

- **Help manage invites** — Keep the roster full during mission weeks (more members = easier goals)
- **Oversee the bank** — Audit withdrawals regularly with `/guild chest log`

### For Members

- **Just fish** — every point of catch XP you earn is mirrored into the guild automatically; no command to remember
- **Donate regularly** — Small deposits from everyone add up to the coin and pearl costs fast
- **Fish during missions** — Even 20 catches per person makes a difference
- **Stock materials** — If you fish a lot, save your materials bags for camp upgrades

### Donation Psychology

People often worry that depositing coins "locks money away." **Emphasize:** Deposits are **not escrowed**. The same coins sit in the bank and can be withdrawn for camp upgrades — nothing is consumed until an Owner or Mod actually runs `/guild upgrade`.

---

## Endgame Value

At full build (level 5, all buildings tier 5):

- **Member bonuses:** +8% sell, +8% XP (from guild level alone)
- **Lure Workshop:** fish bite 15% sooner (tier 5)
- **Library:** +15% XP (tier 5)
- **Chapel:** +5% rarity (tier 5)
- **Bait Hut:** 25% bait save chance (tier 5)
- **Materials:** Daily log/stone production fuels long-term growth
- **Cooldown buff:** −5% weekly (if missions pass)

**Totals at full build:** +8% sell value (from guild level), +23% catch XP (8 from level, 15 from Library), +5% rare chance, a 25% chance to keep your bait, and bites arriving 15% sooner — for every member of the guild.

---

## Troubleshooting

**Q: I was kicked. Can I rejoin?**  
A: Not immediately. You must wait 24 hours before joining another guild.

**Q: What happens if the Owner is inactive?**  
A: They can still manage the guild, but Mods can handle day-to-day ops (invites, withdrawals, upgrades).

**Q: Can I be in multiple guilds?**  
A: No. One guild per player at a time.

**Q: What if the guild runs out of materials for upgrades?**  
A: Pause upgrades and farm materials via fishing. Logging/Stone camps auto-generate if tier 1+.

**Q: Does my personal camp interfere with a guild camp?**  
A: No. They're separate systems. Your camp is personal, the guild camp is shared.

**Q: Do I keep my guild rank if I'm promoted to a new rank?**  
A: Ranks are Guild, Member, Mod, Owner. You have one rank per guild. Promoting changes your role.
