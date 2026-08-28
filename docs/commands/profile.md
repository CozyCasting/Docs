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

Renders your licence with a picker attached — a category dropdown and a background dropdown, one for your name style, a stamp picker, and a **Showcase fish** button. Only cosmetics you've actually unlocked appear in the menus. (Frames are still coming; there's no menu for them yet.)

- **Backgrounds** — every one you've unlocked, listed below. They're grouped by how you earned them — Starter, Level unlocks, Achievements, one group per journal region, and Seasonal & Shop — so pick the category first and the dropdown below it fills with that group. It opens on whichever group holds the background you're currently using.
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
| Caravan Trail | "Caravan Pathfinder" achievement (be the first to find a Roaming Trader) |
| Monster's Wake | "Monster Hunter" achievement (land a Monster Fish) |
| Zeb's Hunt | "Zebukiel's Chosen" achievement (land Zeb's Abyssal Dragonfish) |
| Cartographer's Sea | "The Complete Journal" achievement (catch every species at all 27 locations) |

Another **27 backgrounds** come from your collection journal — see below — and a set of
seasonal and shop backgrounds exists in the game but isn't obtainable yet; they'll arrive
with a future update.

**Journal Backgrounds**

Catch **every species** at a location and you unlock that location's artwork as a
background, named after the location itself. There's one for each of the 27 locations, so
a finished journal is a finished background collection. Check your progress anywhere with
[`/collection`](misc.md#collection), or `/collection <location>` for a single checklist.

Completing a location also pays **+0.5% rarity everywhere you fish**, and finishing all
nine in a region earns a **Naturalist** title. Only fish you caught yourself count — traded
fish and bred offspring don't.

Finish all 27 and you also earn the **World Cataloguer** title, **The Complete Journal**
achievement, and the **Cartographer's Sea** background listed above. If you'd already
finished the journal before that landed, run `/collection` once to claim it.

Listed in the order you can reach them, so you can read it as a route rather than
checking each location one at a time.

| Region | Background / Location | Level | Species to catch |
|--------|----------------------|-------|------------------|
| North America | Appalachian Stream | 1 | 19 |
| North America | Great Lakes Pond | 1 | 20 |
| North America | Mississippi River | 5 | 19 |
| North America | Lake Michigan | 10 | 19 |
| North America | Pacific Ocean | 20 | 19 |
| North America | Mammoth Cave | 25 | 18 |
| North America | Pacific Abyss | 35 | 19 |
| North America | Yellowstone Hot Springs | 45 | 18 |
| North America | Alaskan Arctic | 50 | 18 |
| Asia | Himalayan Stream | 15 | 17 |
| Asia | Japanese Garden Pond | 15 | 19 |
| Asia | Mekong River | 18 | 18 |
| Asia | Lake Baikal | 22 | 18 |
| Asia | South China Sea | 25 | 18 |
| Asia | Son Doong Cave | 30 | 18 |
| Asia | Mariana Trench | 40 | 19 |
| Asia | Mount Fuji Hot Springs | 50 | 18 |
| Asia | Siberian Arctic | 55 | 18 |
| Europe | Alpine Stream | 30 | 19 |
| Europe | English Garden Pond | 30 | 20 |
| Europe | Danube River | 33 | 17 |
| Europe | Lake Geneva | 37 | 18 |
| Europe | North Sea | 40 | 18 |
| Europe | Blue Grotto | 40 | 18 |
| Europe | Norwegian Trench | 50 | 19 |
| Europe | Icelandic Hot Springs | 55 | 18 |
| Europe | Svalbard Waters | 60 | 18 |

That's **497 catches** in total across all 27 locations. Level requirements and what each
location is like are in the [Locations Reference](../reference/locations.md).

**Name Styles**

| Name | Unlocked by |
|------|-------------|
| Plain | Everyone starts with this |
| Frostbitten | Reach level 30 |
| Ember | Reach level 35 |
| Gold Leaf | Reach level 50 |
| Prismatic | "Mythical Encounter" achievement (catch a Mythical fish) |

**Frames** — planned, not yet available. The picker shows as "coming soon".

| Name | Will unlock at |
|------|----------------|
| Brass Frame | Level 20 |
| Driftwood Frame | Level 40 |

!!! note
    Frames are specced but have no artwork yet, so there's no frame picker in `/card` for now. Every background listed above is painted and live.

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

Every calendar month, the server whose members catch the most fish (only `/fish` catches count — nets and breeding don't) wins **7 days of Champion's Bite (25% shorter wait for a bite) for everyone in it**. It can't be bought, and it stacks with a purchased Faster Bites — a winning server that already owns one waits 45% less. The leading server needs at least 100 attributed catches in the month to qualify. Watch the live race with `/leaderboard` → **Servers**.
