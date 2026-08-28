# The CozyCasting website

CozyCasting has a website. It's read-only — everything you *do* still happens
with slash commands in Discord — but a few things are easier to look at on a
page than in an embed.

## What's on it

**The front page** carries the live feed of **Mythical and Unique** catches from
every server that has opted in with `/settings globalfeed enabled:True`, and a
line saying how many fish have been caught in the last hour and how many anglers
have been out today. Both are open to everyone.

**Game-wide totals** — how many fish have been caught across every server, how
many anglers play, the split by rarity, how much of the species catalogue anyone
has ever discovered, and the heaviest fish ever landed — are a **Supporter**
feature. They are totals only; nothing in them names anybody.

**The species journal** is the website version of `/collection` and `/fishinfo`,
and it is a **Supporter** feature. The same journal and the same progression stay
free in Discord on `/collection`; the website adds the visual, searchable layout.
It opens on a map of all 27 locations grouped by region, each showing how much
of its species pool you have logged — the same numbers `/collection` gives you,
all on one screen. Pick a stretch of water and its whole pool lays out below the
waterline. Species you have never landed are silhouettes with their names
hidden; the ones you have caught come out of the dark with your personal count
and the date you first caught one. Click any fish — caught or not — for its size
and weight range, its colours and patterns, everywhere else it lives, and how
many of them everybody has ever landed.

Below the 27 locations sits **Special Waters**: the 30 Monster Fish and the 3
seasonal exclusives, which belong to no location and so appear nowhere else.
**It counts toward nothing** — not the rarity bonus, not the Naturalist titles,
not World Cataloguer, not The Complete Journal. A finished season and a missed
event are both permanently out of reach, so nothing is gated on them. It is
there so the fish you caught have somewhere to be.

Every location is a link, so `?loc=na_deep_sea` on the end of the address goes
straight there — `?loc=special_monster` too.

**Your dashboard** is your own numbers, in more depth than a Discord embed holds,
and it is a **Supporter** feature. Everything on it is also in Discord for free
with `/profile`, `/gear`, `/collection` and `/achievements`. Sign in and it
shows:

- **Where you stand** — level and XP, coins and pearls, your best single sale,
  your session and daily streaks, how many species you have logged, and how
  many locations you have completed.
- **What you have been catching** — the last 90 days as a day-by-day line, your
  catches split by rarity, and which waters and rods you actually use.
- **What you are fishing with** — your rod, bait and equipped gear with the
  stats each piece rolled, and what they add up to.
- **Achievements** — every badge with the date you earned it and how rare it
  is, earned ones first, in a box you can scroll and filter by name.
- **Your catch history** — every fish you have ever landed, **including the ones
  you sold**, sortable by date, value, weight or length and filterable by
  rarity. Click any of them for the full detail: size, weight, the value it was
  worth, where and when you caught it, its traits and its code.

The dashboard only ever shows **you**. There are no public profiles, no lookup by
name, and no way to ask the site for somebody else's numbers — the page reads
who you are from your sign-in and nothing else.

**The Contest Pier** is the week at the pier, read from outside Discord: the
seven waters with today's marked, the three competitions running and their live
standings, the target size when that competition comes up, and every settled
week with the titles it awarded. No sign-in needed.

It is worth reading *before* you spend a day's casts — the schedule is what
tells you whether tomorrow's water is worth waiting for. Tied anglers share a
rank here, the same way the pier awards co-winners. Your own casts and rank stay
in Discord on `/contest`.

Two different things on this site are called a contest, and they are not the
same. The pier is the one where gear and level count for nothing. The
leaderboard and the Hall of Champions are the fish-count race, where they count
for everything.

**The Hall of Champions** is the record of every past Weekly and Monthly Fishing
Champion, newest first, with the dates of the period and how many fish it took
to win it. It is exactly what was awarded at the time — nothing is recomputed,
and a period nobody won says so rather than disappearing. No sign-in needed.

The race running *now* — your rank, the prize, the time left — stays in Discord
on `/leaderboard`, scope **Contest**. If you have opted out of the rare-catch
feed with `/globalfeed`, your name is withheld here too: your win still shows,
as **Anonymous Angler**, with its fish count intact. Server-of-the-month winners
are announced in Discord only; no server is named on the website.

## Caught, held, and in your tank

Three different numbers that are easy to confuse, so the dashboard labels them
apart:

- **Fish caught, all time** is every fish you have ever landed. Selling one does
  not remove it from this — it is your history.
- **Fish you hold now** is what is currently yours, sold ones excluded. A fish
  someone traded to you counts here but never toward what you caught.
- **In your tank** is narrower still: the ones actually in the tank.

## Signing in

The public pages — species pages, shared catches, the rare-catch feed, the
game-wide totals, the leaderboard, the Hall of Champions and the Contest Pier —
need no sign-in at all. Two pages need a sign-in **and** an active Supporter
subscription: the journal and the dashboard. Sign in with Discord and your
catches light up.

Signing in asks for the **`identify`** scope and nothing else — your Discord id,
your name and your avatar. It does not read your messages, your email or the
list of servers you are in, and no Discord token is ever stored. Signing out
clears the session. See the [Privacy Policy](privacy.md) for the full detail.

## What counts as caught

The journal reads exactly the same data `/collection` does, so the two always
agree:

- It counts the fish **you** caught. A fish somebody traded to you doesn't count
  toward your journal — the credit stays with whoever landed it.
- **Selling a fish doesn't un-discover it.** Once you've caught a species
  somewhere, it stays logged.
- **Bred fish don't count.** Offspring inherit their parent's location, so
  breeding can't fill in a pool you never fished.
- A species is logged **per location**. Sunfish live in both the Appalachian
  Stream and the Great Lakes Pond; catching one in the stream doesn't tick the
  pond.
- Pools are **region-specific**. The Himalayan Stream and the Appalachian Stream
  are both streams, and they hold different fish.

## Cost

Most of the site is free and needs no account: species pages, shared catch pages,
the rare-catch feed, the game-wide totals, the leaderboard, the Hall of Champions
and the Contest Pier.

Two parts need an active **Supporter** subscription: your dashboard and the
species journal. Both are a deeper look at information the Bot already gives you
for free in Discord. See the
[FAQ](faq.md#what-can-i-actually-buy) for what a subscription costs and covers.

Your progress on the page can be up to five minutes behind — if you've just
landed something new and it isn't lit up yet, give it a moment and refresh. The
dashboard's headline totals refresh faster, within a minute, and your catch
history is always current.
