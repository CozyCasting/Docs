# Privacy Policy

**Effective Date:** May 1, 2026  
**Last Updated:** August 28, 2026

This Privacy Policy explains how Cozy Casting ("we," "us," or "our") collects, uses, and protects your information when you use the CozyCasting Discord bot (the "Bot"), the CozyCasting website at [cozycasting.app](https://cozycasting.app) (the "Website"), and this documentation site.

> **What changed on August 13, 2026:** we launched the Website. It adds sign-in with Discord (Section 2b), a single sign-in cookie (Section 2c), and a public feed that can show your name alongside your rarest catches (Section 5). The feed is off unless a server administrator turns it on, and you can remove yourself from it at any time with `/globalfeed`.
>
> **What changed on August 24, 2026:** Section 5 now describes **every** place the Website can show your name, not only the feed — the leaderboard, the Hall of Champions and shared catch pages were live but undocumented, which was our omission. Nothing about what the site publishes changed on that date, except that shared catch pages now check your server's enrolment as well as your own opt-out. **`/globalfeed` is the single switch for all four surfaces.**
>
> **What changed on August 28, 2026:** paid subscriptions and a one-time Server Pass went on sale through Discord. We now store a record of what Discord tells us you hold (Section 2d) so the Bot and the Website can answer "is this a Supporter?" without asking Discord on every request. We still never see or store your payment details. Section 6 describes what is sold and what we keep.
>
> Two corrections landed the same day. **The game-wide totals on the Website are public** — earlier drafts of this policy and our Terms described them as a Supporter feature. They are aggregates that name nobody, so there was never anything there to gate or to opt out of, and the pages now match the description. And the Supporter extras that used to have their own commands are all claimed on **`/subscription`** now; the records we keep about them (Section 2d) are unchanged.

---

## 1. Who We Are

CozyCasting is a Discord fishing bot operated by Cozy Casting, based in the United States. You can reach us at [cozycasting@proton.me](mailto:cozycasting@proton.me) with any privacy-related questions.

---

## 2. What Data We Collect

We only collect data that is necessary to operate the Bot. All data is tied to your **Discord user ID** — we never collect your email address, real name, or payment information directly.

### Data you provide by using the Bot

| Category | Examples |
|---|---|
| **Discord Identity** | Your Discord user ID and display name |
| **Game Progress** | Level, XP, coins, pearls, current location |
| **Inventory** | Rods, baits, chests, consumables, and quantities |
| **Fish Collection** | Species, rarity, size, value, traits, catch location, tank status |
| **Achievements & Titles** | Unlocked achievements and equipped titles |
| **Guild Membership** | Which in-game guild you belong to, your rank |
| **Trade History** | Completed trades (items exchanged, both participants' user IDs) |
| **Settings & Preferences** | Notification preferences, display settings |
| **Server Settings** | Per-Discord-server configuration set by server administrators |
| **Vote History** | Whether you have voted for the Bot on top.gg (timestamp only) |

### Data you provide by signing in to the Website {#2b}

Signing in is **optional** — the public parts of the Website work without it. If you do sign in, we use Discord's OAuth2 flow with the `identify` scope only, and Discord gives us:

| Category | Examples |
|---|---|
| **Discord Identity** | Your Discord user ID, your display name, and your avatar image URL |

We ask for nothing else. We do **not** request the `email` scope, and we do **not** request access to your list of servers.

We do **not store the access token** Discord issues. It is used once, immediately, to read the three fields above, and is then discarded. We do not request a refresh token. Nothing on the Website can act on your behalf on Discord.

### Cookies {#2c}

The Website sets **one cookie**, named `cc_session`. It holds only the three fields above, is cryptographically signed so it cannot be altered, expires after 30 days, and is marked `HttpOnly` and `SameSite=Lax`. It exists solely to keep you signed in.

We use **no** analytics, advertising, or tracking cookies, and no third-party trackers of any kind. Signing out (or clearing your cookies) removes it.

### Purchase and subscription records {#2d}

If you buy a Supporter subscription or a Server Pass (Section 6), Discord tells us about it and we store what it told us. We never receive your card details, billing address, or the amount you were charged.

| Category | Examples |
|---|---|
| **Entitlement record** | Discord's entitlement id, the SKU id (which product), Discord's entitlement type, the start and end dates of the entitlement, whether Discord has revoked it (refund or chargeback), whether a one-time purchase has been used up, and when we last heard from Discord about it |
| **Server Pass record** | Which kind of pass, the Discord entitlement and billing period it came from, which Discord server you activated it in, which buff you chose, when you activated it, and whether we have told Discord it was used |
| **Supporter claims** | Which weekly item you claimed in a given week, which perks you selected in a given month, and which profile-card backgrounds you have been granted — all claimed on `/subscription` |

This is a **mirror of Discord's billing decisions, not a source of truth** — Discord decides who has paid, and we record the answer. Revoked and refunded entitlements are kept rather than deleted, so a refund or chargeback leaves an audit trail (see Section 7).

### Technical data

When you visit the Website, our server and the reverse proxy in front of it briefly process your **IP address** in order to apply rate limits and block abuse. IP addresses are not written to your game record and are not used to build any profile of you.

### Data we do NOT collect

- Your email address or real name
- Payment card numbers or billing details (handled entirely by Discord and Stripe — see Section 6)
- Your Discord OAuth access or refresh tokens (used once at sign-in, never stored)
- Your list of Discord servers, or anything else beyond the `identify` scope
- Messages you send outside of Bot commands
- Data from any other bot or application

---

## 3. How We Use Your Data

We use your data solely to operate and improve the Bot:

- **Provide game features** — fishing, progression, inventory, trading, guilds, etc.
- **Persist your progress** — so your fish, coins, and achievements are saved between sessions
- **Send you notifications** — cooldown reminders and other opt-in alerts via Discord DM
- **Prevent abuse** — enforcing cooldowns, trade limits, and other fairness systems
- **Improve the Bot** — aggregated, non-identifiable usage patterns (e.g., which locations are most popular)
- **Sign you in to the Website** — keeping you signed in between visits, and showing you your own data (see Section 2b)
- **Publish rare catches** — only where both permissions in Section 5 are in place

We do not use your data for advertising, profiling, or any purpose outside of operating CozyCasting.

---

## 4. Data Sharing and Third Parties

We do not sell your data. We share limited data only with the services required to run the Bot:

### Discord
The Bot operates on Discord's platform. Discord receives all messages and interactions you send to the Bot. Discord's own [Privacy Policy](https://discord.com/privacy) governs what Discord does with that data.

### top.gg
If you vote for the Bot on [top.gg](https://top.gg), top.gg sends us your Discord user ID and a vote timestamp so we can grant your in-game reward. We store only the vote timestamp. top.gg's [Privacy Policy](https://top.gg/privacy) applies to their platform.

### Discord Monetization / Stripe
Supporter subscriptions and Server Pass purchases are handled entirely through **Discord's built-in monetization system**, which uses Stripe as its payment processor. We never see or store your payment card details, billing address, or the amount charged — Discord tells us only that an entitlement exists, for which product, and when it starts and ends (Section 2d). Discord and Stripe's respective privacy policies govern payment data:

- [Discord Privacy Policy](https://discord.com/privacy)
- [Stripe Privacy Policy](https://stripe.com/privacy)

### Hosting / Infrastructure
Game data is stored on servers we control. The Website is served from behind a reverse proxy / content delivery provider, which processes your IP address and request headers in order to route traffic and absorb abuse. We do not use third-party analytics platforms (e.g., Google Analytics) on the Website or this documentation site, and we run no advertising.

---

## 5. Information Published on the Website

Two things on the Website are visible to anyone, without signing in. They are very different, and the difference matters.

### The rare-catch feed — can show your name, and is opt-in

The Website carries a live feed of **Mythical and Unique** catches from across servers that have joined it. Each entry shows the fish, its size, weight and value, the location it was caught in, **the name you were using when you caught it**, and how long ago it happened.

Two separate permissions must both be in place before any catch of yours appears there:

1. **A server administrator has enrolled that server** with `/settings globalfeed`. This is off by default. No server participates until an administrator turns it on.
2. **You have not opted out.** Any player can run **`/globalfeed`** to remove themselves from the feed entirely, in every server at once. Your choice overrides the server's.

Both checks happen at the moment a fish is caught. If either says no, nothing about that catch is ever published or stored for the feed.

The feed **never shows** which Discord server a catch happened in, your Discord user ID, or your avatar. It holds only the most recent 200 catches; older entries are discarded automatically.

Opting out applies to **future catches**. Entries already published keep the name they were published with until they age off the feed, which happens on its own as new catches arrive.

### The leaderboard and the Hall of Champions — can show your name, and are global

The Website publishes a public leaderboard at [cozycasting.app/leaderboard.html](https://cozycasting.app/leaderboard.html) and a Hall of Champions of past winners. **Neither needs a sign-in to read.** Anyone with the link, including a search engine, can see them.

What they show: your **rank**, the **name you last used**, and the **score for that category** — nothing else. Five categories (fish caught, largest fish, most valuable fish, highest level, best streak), each over an all-time, monthly or weekly window, and up to 100 places per board.

**These are global, not per-server.** They rank every player of the Bot together, so unlike the rare-catch feed there is no single server whose administrator could enrol you or keep you out. That means **there is no server-level switch here** — the only control is your own.

**`/globalfeed` covers these too.** If you opt out, your name is replaced with **"Anonymous Angler"** everywhere on the site. Your rank and score stay on the board: removing the row entirely would renumber everyone below you and make the board wrong. Opting out takes effect on the next refresh of the page — it is not limited to future catches, because unlike the feed, nothing here is published once and frozen.

The leaderboard and the Hall of Champions **never show** your Discord user ID, your avatar, or which server you play in. The Hall of Champions also has "server of the month" periods; those are **not** published on the Website at all.

### Shared catch pages — the link the Bot gives you

Every fish you catch has a short code, and the Bot prints it in the catch message. That code opens a public page for that catch at `cozycasting.app/c/<code>`, which is what makes a link unfurl with a picture when you paste it into Discord.

The page shows the fish, its rarity, size, weight, value, where it was caught and when. **It shows your name only if both of the same permissions in the feed rules above are in place** — your server enrolled with `/settings globalfeed`, and you have not run `/globalfeed`. If either is missing, or if the fish was not caught in a server at all (a DM, a net, or breeding), the page reads **"Anonymous Angler"** instead. It never shows your Discord user ID.

The catch details themselves are visible to anyone holding the code. Codes are random, not sequential, so a page is not findable by guessing — but a code you paste into a public channel is readable by everyone in it.

### Game-wide statistics — never about a person

The Website also shows totals: how many fish have been caught across all servers, how many players there are, the split by rarity, and the heaviest fish ever landed. These are **aggregates only**. Nothing in them identifies anyone — including the heaviest-fish figure, which shows the fish and never who caught it. There is nothing to opt out of, because no individual appears.

---

## 6. Purchases and Virtual Currency

Coins and pearls are **in-game virtual currencies** with no real-world monetary value. Neither can be purchased, transferred, withdrawn, or exchanged for cash.

Two things can be bought, both sold by Discord: a recurring **Supporter** subscription, and a one-time consumable **Server Pass**. The [Terms of Service](terms.md), Section 6, describes what each one grants.

Purchases are processed by Discord, which uses Stripe as its payment processor. Cozy Casting receives a payout from Discord but does not process, see, or store payment information. All billing disputes should be directed to Discord support.

What we keep about a purchase is listed in Section 2d: an entitlement record, a pass record if you were granted a pass, and your Supporter claims. **A Supporter subscription is what unlocks the Dashboard and the species Journal on the Website.** When you open one of those pages, we check your entitlement record; the answer is cached briefly so that cancelling takes effect within about fifteen minutes rather than instantly.

---

## 7. Data Retention

We retain your game data for as long as your account is active. If you request deletion of your data (see Section 8), we will remove it within 30 days.

Website sign-in sessions expire after 30 days, and sooner if you sign out. Rare-catch feed entries are discarded automatically once 200 newer catches have been published, and are not retained anywhere else.

Completed trade logs are retained to allow for dispute resolution and may be kept for up to 90 days after your account is deleted.

Purchase and entitlement records (Section 2d) are retained for as long as we may need them to resolve a billing dispute, honour a refund, or answer a chargeback, and are not deleted when an entitlement expires or is revoked — a deleted entitlement is marked as such rather than removed. If you request deletion of your account, we remove your game data as described above; a minimal purchase record may be retained where we are required to keep it for tax, accounting, or dispute-resolution purposes.

---

## 8. Your Rights

Regardless of where you are located, you may:

- **Access** — Request a summary of the data we hold about you
- **Correct** — Ask us to fix inaccurate data
- **Delete** — Request deletion of your account and associated data
- **Opt out of DM notifications** — Use `/notifications` in the Bot to turn off cooldown and event reminders
- **Opt out of being named on the Website** — Use `/globalfeed` in the Bot. One command covers all four public surfaces: the rare-catch feed, the leaderboard, the Hall of Champions and shared catch pages. You become "Anonymous Angler" on every one of them (see Section 5)
- **Sign out of the Website** — Use the Sign out button in the site header, which deletes the `cc_session` cookie

To make a request, email us at [cozycasting@proton.me](mailto:cozycasting@proton.me) with your Discord username and user ID. We will respond within 30 days.

**California residents:** Under the CCPA, you have the right to know what personal information we collect, request deletion, and opt out of sale (we do not sell data). Contact us at the email above to exercise these rights.

---

## 9. Children's Privacy

CozyCasting is not directed at children under the age of 13. We rely on Discord's age verification, which requires users to be at least 13 years old to create a Discord account. If you believe a child under 13 has provided us data, please contact us at [cozycasting@proton.me](mailto:cozycasting@proton.me) and we will delete it promptly.

---

## 10. Changes to This Policy

We may update this policy as the Bot evolves. When we make material changes, we will update the **Last Updated** date at the top of this page. Continued use of the Bot after changes are posted constitutes your acceptance of the updated policy.

---

## 11. Contact Us

Questions, concerns, or data requests:

**Email:** [cozycasting@proton.me](mailto:cozycasting@proton.me)

We aim to respond to all inquiries within 5 business days.
