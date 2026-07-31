# Profile Commands

View your stats, track your progress, and see how you compare.

## /profile

View a user profile and stats.

- **Usage:** `/profile [user]`
- **Aliases:** `!fme` (prefix only)
- **Examples:** `/profile`, `/profile @friend`
- **Cooldown:** 10 seconds

Renders your **fishing licence** — a card image with your avatar, level, and stats — plus an embed for your wallet and equipped gear. See [Profile Cards](#profile-cards) below for what's on it.

!!! tip "Prefer plain text?"
    Turn on **compact mode** to skip the card image and get the classic text-only embed instead — handy on a slow connection or with a screen reader.

## Profile Cards

`/profile` renders your profile as a **fishing licence** card alongside its embed. The card shows:

| Field | What it means |
|-------|---------------|
| Avatar & name | Your Discord avatar and display name |
| Title | Your currently equipped title (`/title`) |
| Level & XP bar | Current level and progress to the next |
| Licence No. | A stable ID derived from your account |
| Issued | The date of your **first catch** — not when you joined. A fish you were *traded* doesn't count, so trading into a fresh account won't backdate this |
| Fish Caught | Fish **you personally caught**. Fish you acquired by trade don't count, and fish you've since traded away still do |
| Fish Bred | Offspring you've collected from breeding — tracked separately from Fish Caught, the two never overlap |
| Tournaments Won | Weekly/monthly contest wins (see `/leaderboard` → Contest). Shows "None yet" instead of 0 |
| Best Streak | Your all-time best fishing session streak |
| Home Waters | The server where you've caught the most fish, falling back to your most recently active server if you don't have enough catches attributed anywhere yet. Reads "Unknown" if neither is available |
| Most Valuable | Your single most valuable fish currently in your tank |
| Showcase fish | The fish shown on the card with its species, size, rarity, and value — defaults to your most valuable fish, but you can pick a different one with `/card` |
| Stamps | Up to six postmarks representing achievements and titles you've unlocked |

Viewing someone else's card with `/profile @user` shows *their* stats and *their* chosen cosmetics.

## /card

Customise your profile card.

- **Usage:** `/card`
- **Cooldown:** 10 seconds

Renders your licence with a picker attached — one dropdown per cosmetic slot (background, frame, name style), a stamp picker, and a **Showcase fish** button. Only cosmetics you've actually unlocked appear in the menus.

- **Stamps** — pick up to six from your unlocked achievements and titles. If you have more than 25 unlocks, the picker shows your 25 most recent.
- **Showcase fish** — opens a box for a fish's short code. Leave it blank to reset to automatic (your most valuable fish). You can only showcase a fish you currently own — one you've since traded away stops appearing.

### Cosmetic Unlocks

Everything below is preset art and effects — there's no way to upload your own background, and cards don't currently support animation, permalinks, or per-server variants.

**Backgrounds**

| Name | Unlocked by |
|------|-------------|
| Standard Issue | Everyone starts with this |
| Dockside | Reach level 10 |
| Sakura Dusk | Reach level 25 |
| Deep Blue | Reach level 40 |
| Sunset Pier | Reach level 60 |
| Volcanic | "Volcano Venturer" achievement (reach level 45) |
| Arctic | "World Traveler" achievement (fish in all 9 location types) |
| Summer 2026 | A seasonal drop — not yet obtainable, coming in a future update |

**Name Styles**

| Name | Unlocked by |
|------|-------------|
| Plain | Everyone starts with this |
| Frostbitten | Reach level 30 |
| Ember | Reach level 35 |
| Gold Leaf | Reach level 50 |
| Prismatic | "Mythical Encounter" achievement (catch a Mythical fish) |

**Frames**

| Name | Unlocked by |
|------|-------------|
| No frame | Default |
| Brass Frame | Reach level 20 |
| Driftwood Frame | Reach level 40 |

!!! note
    Most background art hasn't been painted yet, so most cards still render on a plain generated background today even once unlocked — the unlock itself is live now, the artwork is catching up.

## /stats

View detailed fishing statistics.

- **Usage:** `/stats`
- **Aliases:** `statistics`, `mystats`

A deeper breakdown of your fishing history: catches by rarity, biggest fish, most valuable catch, and more.

## /level

View level progress and upcoming rewards.

- **Usage:** `/level`
- **Aliases:** `lvl`, `xp`, `progress`

Shows your current XP, progress bar to the next level, and the next achievement milestone.

## /achievements

View your unlocked achievements.

- **Usage:** `/achievements [category]`

Lists all achievements organized by category (Level, Fishing, Collection, Exploration, Economy, Voting, Daily). Unlocked achievements show their reward; locked ones show progress toward the goal. Unlocked achievements (and titles) are also available as [profile card](#card) stamps.

## /title

Equip or change your display title.

- **Usage:** `/title <title>`

Titles are earned through achievements and rare chest drops. Your equipped title appears on your profile.

## /referral

View your referral stats and code — see the [Trading & Referrals](misc.md#referral) section for details. `/profile` also shows a quick summary, with a nudge toward `/referral` if you haven't shared your code yet.

## /leaderboard

View the server leaderboard.

- **Usage:** `/leaderboard [scope] [time_filter]`

**Scopes:**

| Scope | Shows |
|-------|-------|
| Global | Rankings across every server the bot is in |
| This Server | Rankings for your current server only |
| Servers | The live monthly race for [Server of the Month](#server-of-the-month) — which server's members have caught the most fish this month |
| Contest | Live standings for the in-progress weekly/monthly **most fish caught** contest — see [Contests](#contests) below |

**Categories** (Global / This Server scopes): Fish Caught, Largest Fish, Most Valuable, Highest Level, Highest Streak — switch between them with the navigation buttons on the embed, no need to retype the command.

**Time filter:** All Time, This Month, This Week (applies to the Global/This Server scopes).

### Contests

Every week and every month, whoever catches the most fish (globally) wins a prize once the period ends:

| Period | Prize |
|--------|-------|
| Weekly #1 | 🏆 1x Unique Chest + 100 pearls |
| Monthly #1 | 👑 2x Unique Chests + 250 pearls |

`/leaderboard` → **Contest** shows the live in-progress standings, your current rank, and the time left — with a button to toggle between the weekly and monthly view. Rewards are paid out automatically once the period ends and count toward your [Tournaments Won](#profile-cards) stat.

### Server of the Month

Every calendar month, the server whose members catch the most fish (only `/fish` catches count — nets and breeding don't) wins a **7-day server-wide Rarity Boost (+15% rare fish chance) for everyone in it**. The leading server needs at least 100 attributed catches in the month to qualify. Watch the live race with `/leaderboard` → **Servers**.
