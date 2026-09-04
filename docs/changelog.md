# Changelog

All notable changes to CozyCasting will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.10.3] - 2026-09-04

### Changed

**The early game is much faster** — A brand new angler used to catch one fish and then wait a quarter of an hour with nothing to do, which is where most people quietly put the game down. The fishing cooldown now scales with level: **2 minutes at level 1**, rising gradually to the usual 15 minutes at **level 10**. Rod and gear reductions apply on top exactly as before, and `/gear` shows both the base you're on and where it's heading. Nothing changes for anyone at level 10 or above.

**Your first casts of a session can't escape** — The escape ladder used to start on cast two, so a session could end on a single fish through nothing but bad luck. The **first three casts of every session are now guaranteed** for everyone, at every location, with the ladder falling away much more steeply afterwards — the average session still lands about the same number of fish, but the floor is real. **Below level 10 you get five guaranteed casts.** A Shipwreck can still cut a session brutally short, but it can no longer send you home empty-handed.

**Every session gives you at least one real fish** — Guaranteed casts can turn up chests, and a player stacking chest bonuses could spend all of them on chests and land no fish at all (about one session in twenty-three at the 35% cap). If chests have eaten every guaranteed cast, the last one is a fish. Materials Bags are unaffected — they never spent a cast to begin with.

**Referrals pay out at level 10** — A referral used to complete when your friend reached level 5. It now completes at level 10. (Partly to combat abuse where people seemed to get their friends or alts to level 5 then immediately quit.)

**Monster Fish are one per server, not one per channel** — The 30-minute cooldown between Monster Fish was held per *channel*, so a server with several fishing channels quietly gave itself several times the spawn rate, and two monsters could run at once and split the same handful of anglers between them. The cooldown is now per server, and only one monster can be active in a server at a time. A spawn that fizzles for want of players still costs nothing, as before.

**The Roaming Trader always stocks Fertility Tonic** — He's the only source of it, so a bad rotation could put breeding out of reach for weeks. It's now guaranteed every Thursday and the other two consumable slots rotate as before.

**Bites come much faster below level 10** — A new angler's session was mostly spent watching the water: five guaranteed casts at up to twelve seconds each, before anything happened. Below level 10 the wait is now **1.5 to 6 seconds**. Every bite-speed bonus — rods, gear, potions, guild and server buffs — still applies on top, and nothing changes at level 10 or above.

### Added

**A starter chain for your first sessions** — Five one-off steps — catch a fish, sell one, keep one, use bait, land 25 — that pay out **the moment you finish them**, with no claiming. They show up on your catch results and at the top of `/quests`, each one naming the next thing to try. Between them they're roughly your first rod upgrade.

**New species are called out when you catch them** — Catching a species for the first time now says so on the catch itself, instead of it looking identical to the hundredth common you've sold. `/profile` also shows your journal completion, so there's a number to chase that isn't your coin balance.

**Nine more daily quests** — The early quest pool was three entries wide, so a new player saw nearly the same board every day. There are now quests for opening chests, catching uncommons, shorter catch and sell targets, smaller streaks, and — at level 10 — collecting from your net.

**Weekly server quests** — Your whole Discord server now shares one goal each week, rotating between **Full Harbour** (catch fish together), **Broad Waters** (land as many different species as you can) and **Deep Prizes** (Rare-or-better catches). The target scales with how many anglers your server actually has, so a small server gets a real target rather than an impossible one. Clear it and the whole server gets **Quest Current** — 10% faster bites — for the following week, and everyone who contributed at least 5 gets **2× Rabbit Foot**. Check progress any time with `/server quest`; the result is posted when the week rolls over, in whichever channel you've set for leaderboard results, rare catches or chest drops, falling back to your system channel.

**Pearls for voting** — Every **10th vote** now pays **10 pearls** on top of the usual voting ticket. It runs off your lifetime vote count, not your streak, so a missed day costs you nothing toward it. `/vote` shows how many votes are left until the next one.

**A nudge about invites at level 10** — Reaching level 10 now tells you that it's the same bar anyone you invite has to clear, and points you at `/referral`. The rewards were always there; almost nobody knew about them.

### Fixed

- Monster Fish fights now reliably preserve an active Fishing Frenzy, ordinary waters guarantee a real catch before a session can end, and streak quest completions appear in the session summary.

## [0.10.2] - 2026-09-01

### Added

**`/subscription` has buy buttons now** — Supporting CozyCasting used to end with the bot telling you to go and find its Store page yourself, which looks different on desktop, mobile and web and was easy to give up on. Every tier now has its own button right there in `/subscription`, with the name and price read straight from Discord, and checkout happens without leaving the chat. There's still a link through to the full store listing if you want the descriptions and the art before you decide. Anything you already subscribe to is left off — you'll only ever see what you don't have yet.

### Fixed

**Your river trout came back** — Every river in the game served a fish called "Brook Trout" up to 0.10.1, because a shared species id let the stream's trout overwrite the river's in the database. 0.10.1 untangled the two, so rivers correctly ask for the Rainbow Trout they were always meant to hold — and every trout you had already caught in one was still filed under the stream's name, leaving the Mississippi, the Mekong and the Danube one short of complete. The 1,183 trout caught in a river are renamed to Rainbow Trout, which is what they always were. Trout caught in a stream are untouched.

**`/locations` and `/collection` no longer disagree after new waters land** — When a content update was loaded into a running bot, `/locations` kept listing the world as it was before the update while `/collection` already counted the new waters, so the two commands told you different things until the bot was restarted. Every list built on top of game data is now rebuilt when that data is reloaded.

## [0.10.1] - 2026-09-01

### Added

**South America, and the level cap moves to 125** — A fourth region and the whole back half of the progression curve.

- **Eleven new locations**, from the Andean Meltwater at Lv 80 up to the Patagonian Ice Fields at Lv 125: the Rio Negro's blackwater, Lake Titicaca, the Galapagos Reef and Vents, the Humboldt Current, Cueva de los Tayos, a sunken Caribbean galleon, and the Peru-Chile Trench.
- **165 new species** — arapaima, payara, peacock bass, piranha, pacu, candiru, electric eel, silver arowana, and the pink river dolphin at the very top of the rarity table.
- **The level cap moves 100 to 125.** The XP curve itself is unchanged, so nothing about levels 1-100 is re-priced. Two new milestones land in the new band: **Deep Water** at 110 and **End of the Map** at 125.

**Three European locations now require higher levels** — The Norwegian Trench moves Lv 50 to 60, the Icelandic Hot Springs 55 to 68, and Svalbard Waters 60 to 75. This closes the empty stretch between the old top of the map and where South America begins.

**If you are already standing in one of them, you keep fishing there** — the requirement is only checked when you travel. Travel away and you will need the new level to return.

**Two new kinds of water: the Reef and the Shipwreck** — Six new locations, two in each of North America, Asia and Europe.

- **Reefs** are shallow, crowded and gentle: the Florida Keys (Lv 30), Raja Ampat (Lv 35) and the Mediterranean Reef (Lv 45). Bites come constantly and fish rarely escape, but everything you catch is small and doesn't sell for much. This is where you fill the journal.
- **Shipwrecks** are the exact opposite: the Edmund Fitzgerald (Lv 55), the Java Sea Wrecks (Lv 60) and Scapa Flow (Lv 65). Long waits, big fish, sharks, far more chests than anywhere else — and a session that can collapse under you with no warning.

**Your journal percentage will drop, and that's expected.** There are 44 locations now instead of 27, so the same collection is a smaller share of a bigger world. Two knock-on effects worth knowing:

- The full-journal rarity bonus ceiling went up with it, from +13.5% to +22%.
- **World Cataloguer** and the regional **Naturalist** titles now need the new waters too. **If you already have one, you keep it** — nothing is taken back. But anyone earning them from here needs the reefs and the wrecks as well.

**Nine new profile-card backgrounds for South America** — Every South American water now unlocks card art when you finish its journal, the same as everywhere else: the Andean Meltwater, the Pantanal Oxbow, the Rio Negro, Lake Titicaca, the Humboldt Current, Cueva de los Tayos, the Peru-Chile Trench, the Galápagos Vents and the Patagonian Ice Fields. Every location in the game now has one — South America was the last region where finishing a journal gave you nothing to show for it, and it held the nine hardest journeys in the game.

**Eight new profile-card backgrounds for the reefs and wrecks** — Complete a reef or a shipwreck's journal and you unlock its art in `/card`, the same as every other water: the Florida Keys, Raja Ampat and the Mediterranean Reef; the Edmund Fitzgerald, the Java Sea Wrecks and Scapa Flow; and in South America, the Galápagos Reef and the Caribbean Galleon.

**No more rarity bonus per location** — Each location listed a "Rarity Bonuses" but it was hard to find and generally didn't impact too much.

**Every water now fishes differently** — Until now the only thing separating one location from another was which fish lived there. Now the water itself has a character, and you'll feel it on the very first cast.

- **Ponds and streams** are nurseries: bites come easily and the fish rarely get away, but nothing you pull out is big.
- **Lakes** are the opposite — you'll wait longer and lose more, and the fish are worth the wait.
- **Caves** hide things. Bites are slow down there, but chests turn up far more often.
- **The deep sea, volcanoes and the arctic** all fight you in their own way: longer waits, more escapes, and the biggest fish in the game as the payoff.
- **Rivers and oceans are deliberately plain.** They're the yardstick everything else is measured against.
- `/travel` tells you what a water does before you commit to it, and `/fish` reminds you at the top of every session.

Nothing was taken away and no location got worse across the board — each one trades something for something else. Your gear, buffs and consumables all still apply exactly as before, on top of whatever the water is doing.

### Changed

**Every server's rare catches are on the website feed now, and the angler is anonymous unless the server opts in** — The feed used to be empty for almost everybody, because a server only appeared on it once an admin ran `/settings globalfeed`, and almost nobody did. Participation is now universal and the switch moved to the part that actually identifies someone.

- **Mythical and Unique catches from any server appear on the feed.** A catch entry carries the fish, its size, value and location, and nothing that names a person, a server, or a Discord ID.
- **`/settings globalfeed` now controls whether your server's anglers are named there** — still off by default, so a server that never touches it publishes catches that read "Anonymous Angler".

**Cancelling a breed within 15 minutes refunds the fertility** — Starting a breed still costs both parents 15 fertility, but if you cancel in the first 15 minutes it is given straight back (never above 100). Cancel later than that and the cost stands, as before.

### Fixed



## [0.10.0] - 2026-08-28

Note: Subscriptions/Purchases will be available on Sept 1st.

### Added

**Supporter subscription and the Server Pass** — Two optional purchases, both through Discord's store on the bot's profile.

- **Supporter** is a monthly subscription, run entirely from `/subscription`:
    - One of three items each week.
    - Two perks you pick each month.
    - A profile-card background each month, kept even if you cancel.
    - The Supporter parts of the website: your Dashboard and the species Journal.
        - This is meant as a way to monetize the game a bit to go towards development and hosting costs without restricting game-features. All info on the site is also available via discord; just in a less 'pretty' way.
- Supporter has two tiers. The higher one also grants **one 14-day Server Boost Pass a month** — one server buff of your choice, in one server.
- The **Server Pass** is a one-time purchase, not a subscription: activating it runs **every purchasable server buff for 30 days** in one server. It grants no website access.
- Neither pass expires.
- Discord shows the price and handles payment; we never see your card. Cancel any time and access lasts to the end of the period you paid for. The [Terms](https://cozycasting.github.io/Docs/terms/) and [Privacy Policy](https://cozycasting.github.io/Docs/privacy/) now state what is sold and what is kept about a purchase.

**The Contest Pier** — `/contest` is a free weekly competition where rod, bait, gear, level, location, buffs and consumables count for nothing.

- This will replace rewards previously provided to 'most-fish' leaderboards. That will now grant a title and recognition on the website 'Hall of Fame'.
- **10 casts a day.** They don't roll over and can't be earned, bought or refilled, so a full week is 70.
- **The water changes daily.** Each day of the week is a different location with its own species pool, and the whole schedule is posted in advance — a volcano day pays more than a stream day, for everyone equally.
- **Three competitions a week**, drawn from Biggest Catch, Smallest Catch, Richest Haul, Widest Variety and Target Size, and fixed for the whole week.
- **Nothing carries over.** Contest fish are released: no coins, XP, tank, journal or leaderboard credit.
- **Each win pays 🦪 50 Pearls, a 🎁 Unique Chest and that competition's title** — Pearls and chest every time, the title once.
- Each cast is recorded as it happens, so you can stop and come back. Ties are co-winners; casting earlier is worth nothing.
- Casts reset 00:00 UTC daily; the week settles Saturday 00:00 UTC (Friday evening in the Americas).

**Contest Pier page** — [/contest.html](https://cozycasting.app/contest.html), no sign-in.

- This week's seven waters, with today's marked.
- The three competitions running, their live standings, and the target size when that competition comes up.
- Every settled week with the titles it awarded.
- Tied anglers share a rank, as the pier does. `/globalfeed` opt-outs show as *Anonymous Angler*, keeping their rank and score.

**Gear sets** — Save a loadout and swap it back in one command.

- `/gearset save <name>` snapshots the rod and gear you have equipped; `/gearset equip <name>` puts it back on; `/gearset` lists your sets; `/gearset delete` removes one.
- A set is exact, so a slot left empty at save time comes back empty.
- Bait isn't included — it gets used up, so it stays on `/equip`.
- Three sets are free; more are in `/shop` → **Upgrades** for 🦪 pearls.
- If you traded or scrapped a piece since saving, the rest still equips and the command names what was missing.

**Server tournaments** — `/tournament start` runs a live competition in your server.

- **Heaviest Single Catch** or **Most Total Fish Caught**, 5 to 120 minutes.
- Every `/fish` catch in the server counts automatically — there's nothing to join.
- `/tournament leaderboard` shows standings and time left; the bot announces the top three in the starting channel when time runs out.
- Needs **Manage Server**, one at a time per server.
- Nets and breeding don't count, there are no prizes, ties go to whoever got there first, and a bot restart cancels a running tournament.

**Other additions**

- **Sort your tank** — `/tank` takes a **sort** option: rarity (the default, as before), value, species A–Z, fertility, size, newest or oldest. Your choice holds across every page and carries into the bulk-sell screen, so you can order by fertility and sell down the fish you don't want to breed with. Sorting by size or catch date puts that number on each row — 📏 42.5 cm or 📅 Jun 01 — in your own units. Works on other players' tanks. Tied fish now keep a fixed order instead of shuffling between pages.
- **You're told when someone gives you something** — `/give` now DMs the recipient with the sender's name and what arrived. It's the **trade** notification, so `/notifications` and your quiet hours control it like everything else. If your DMs are closed the gift still goes through; you just don't get the message.
- **The game now tells you where you can travel** — Levelling into a new location names it in the level-up message and points at `/locations` and `/travel`, including every location you cross if one catch jumps you several levels. If you've never left the Appalachian Stream, your fishing session says how many other waters are already open; that note disappears the first time you travel. `/travel` and `/locations` work as before.
- **Special Waters** — The Monster Fish and the three seasonal exclusives belong to no location, so they appeared nowhere in `/collection` or the web journal even after you caught them. Both now have a **Special Waters** section split into **Monster Waters** and **Seasonal Waters**, with your count on each and silhouettes for the rest. **It counts toward nothing** — not the rarity bonus, the region Naturalist titles, World Cataloguer or The Complete Journal — so journal percentages and rewards are exactly as they were. An ended season and an event you missed are out of reach for good, so nothing is gated behind them. Monster catches missing from your journal appear the next time you run `/collection`.

**New on the website**

- **A page for every species** — Every species has a public page at `/fish/<name>` with its art, size and weight ranges, colours and patterns, and every water it lives in. No sign-in required. There's an A–Z index at [/fish](https://cozycasting.app/fish), linked from every page's footer, and every species in the journal has a **Full page** link to share.
- **A page for every catch, and it unfurls in Discord** — Every fish has a page at `/c/<code>`, and pasting the link into a Discord channel renders a card with the fish, its rarity, size, weight and value, where it was caught and who caught it. It shows up as **Share this catch** on any fish you open, in the front page's rare-catch feed and in your logbook.
- **Leaderboard page, with the Hall of Champions** — Most fish caught, largest fish, most valuable fish, highest level and longest streak, across every server, over 7 days, 30 days or all time. It reads the same rankings `/leaderboard` does and refreshes about once a minute.  The second tab is the **Hall of Champions**: every past Weekly and Monthly Fishing Champion, newest first, with the period's dates and the winning count, as awarded — nothing is recomputed, and a period nobody won is listed as such. No sign-in. `/globalfeed` opt-outs appear as *Anonymous Angler*, keeping their rank and score. The contest running right now is still `/leaderboard` in Discord, scope **Contest**. 
    - Server-of-the-month winners stay in the Discord announcement; no server is named on the site.
- **The rare-catch feed** — A public page with a live feed of **Mythical and Unique** catches from servers that opt in. Admins turn it on with `/settings globalfeed enabled:True`; it's off until they do. Enrolling publishes the fish, its size, weight and value, the location and **the angler's name** to a page anyone can read without signing in; your server's name is never shown. Any player can remove themselves everywhere at once with `/globalfeed`, which overrides the server setting — it applies to future catches, and anything already on the feed ages off. Clicking a catch opens it larger with its size, weight, value, location, angler and date.
- **Game-wide totals on the front page** — Total fish caught across every server, how many anglers play, the split by rarity, how much of the species catalogue has ever been discovered, and the heaviest fish ever landed, plus a line showing fish caught in the last hour and anglers out today. 
- **Your logbook on the web (Supporter)** — Signing in gives you a page with more depth than a Discord embed holds:
    - Level and XP, coins, pearls, best single sale, session and daily streaks, and journal completion.
    - The last 90 days of catches as a daily line, your split by rarity, and which waters and rods you actually use.
    - Your equipped rod, bait and gear with the stats each piece rolled, and every achievement with the date you earned it.
    - **Every fish you have ever caught, including sold ones** — sortable by date, value, weight or length, filterable by rarity, each one opening for full detail.
- **The species journal on the web (Supporter)** — A map of all 27 locations grouped by region, each showing how much of its pool you've logged. Species you've never landed are silhouettes with hidden names; caught species show in colour with your count and first-catch date. It reads what `/collection` reads: traded fish don't count, selling doesn't undiscover one, bred fish don't count, and discovery is per location. Progress can be up to five minutes behind. The same journal is free in Discord through `/collection`.
- **Search in the species journal** — 497 journal entries across 27 locations, and the only way in was clicking waters until you found the fish. The journal now has a search box: type a species and it tells you which water to fish, type a water and it takes you there. Seasonal and monster species are searchable. Arrow keys and Enter work.

### Changed

**`/subscription` shows the dates that matter**

- When you subscribed, the start and end of the current billing period, and whether it will renew or has been canceled.
- This week's item and reset, and where this month's 14-day Server Boost Pass was used.
- **The weekly item is claimed here now**, from a menu on the same screen — the separate `/weekly` command is gone. What you get and the once-per-UTC-week rule are unchanged.
- Separately purchased 30-day Server Passes stay on `/serverpass`; they aren't subscription benefits.
- If Discord's billing status is unavailable, the command still shows the access dates the bot can verify itself.

**Server buffs**

- **Rarity Boost removed from the shop** — It was the one thing in the game where pearls bought a better chance at the fish everyone competes over. Rare-fish chance now comes only from your rod, bait, gear, consumables and guild.
- **New server buff: 🪝 Faster Bites** — Takes Rarity Boost's place in `/shop` → **Server Buffs** at the same price. Everyone in the server waits **20% less** for a bite. It doesn't change what you catch or how often you can fish.
- **The monthly top-server prize is now 🏆 Champion's Bite** — The server whose members catch the most fish in a calendar month wins **25% less bite wait for 7 days** instead of Rarity Boost. It can't be bought, and it stacks with a purchased Faster Bites for 45%. Qualifying is unchanged: most `/fish` catches in the month, minimum 100.
- **The weekly and monthly fish-caught races now pay titles** — Top of the weekly board earns **Full Time Fisher**, top of the monthly earns **Career Angler**. The Pearls and Unique Chests they used to pay are gone; those boards are run with whatever gear and buffs each player owns, so they're a status board, and the prizes moved to `/contest` where everyone starts level. The standings are unchanged and still in `/leaderboard`.

**Privacy**

- **Catch pages follow the same rule as the feed** — A `/c/<code>` page named the angler whenever they hadn't opted out of `/globalfeed`. It now also requires that the catch happened in a server enrolled with `/settings globalfeed`. A catch from an unenrolled server, or one with no server at all (a DM, a net, a bred fish), now reads *Anonymous Angler*. Only the name is withheld.

**Everything else**

- **Bulk sell shows fertility instead of size** — Deciding what to sell out of a full tank is usually a breeding decision, and size didn't help. Each row now reads 🥚 75% where it showed length. Nothing else about bulk sell changed. Size is still on `/tank` and `/fishinfo`.
- **`/locations` is one map, not three walls of text** — It sent three messages, one per region, each listing three fish names and "+16 more" per location. It's now a single embed with a world map and all 27 locations grouped by region, ordered the way you unlock them. Each location you can reach shows the base value of its fish, so you can see that Pacific Abyss pays more than Lake Michigan, and how much of its pool you've logged; locked ones show the level you need. Your total journal progress and the rarity bonus it currently pays sit at the top. Species names were dropped on purpose — truncated to three they were useless, and `/collection <location>` has the full checklist.

### Fixed
- **`/tank` no longer fails on a page of renamed fish** — Ten fish with custom names and several traits each could push a page past Discord's limit on how much text an embed section holds, and the command errored instead of showing anything. The page now continues into a second block. Nothing is hidden or shortened, and a normal tank looks as it did.

## [0.9.9] - 2026-08-26

### Fixed
- **The Roaming Trader's stall opens again** — If you walked up to the caravan this week, `/trader` gave you nothing: no stall, no wares, no way to buy. One of the items on offer, the Gilded Magnet, carries a two-part emoji, and Discord refuses to draw a button labelled with more than one — so the entire stall was thrown out rather than that one button. Buttons now take just the first emoji of an item's name and the stall renders as it should. Nothing was lost while it was broken: if you were the first to find this week's caravan, that discovery is still unclaimed and waiting for you, along with the Caravan Pathfinder title and the Caravan Trail card background.

## [0.9.8] - 2026-08-14

### Changed
- **Your rod now sets how far your cooldown can be cut** — Gear, potions, server buffs and guild buffs all still shorten your fishing cooldown exactly as before, but there's now a limit on how much they can take off in total, and that limit rises with the rod you're holding. Every rod from the Basic upward gets a bigger allowance than the one below it, so upgrading your rod pays twice: once for the rod's own reduction, and again for the extra headroom it unlocks. Nothing has been taken out of your inventory and no bonus has been reduced — the only thing that changes is that piling on past your rod's limit no longer buys you anything. Almost everyone is already under their limit and will notice nothing at all; if you're over it, `/gear` now says so on the cooldown line and tells you that a better rod raises it. This replaces a situation where a lucky run of crafted gear could out-cut a rod you hadn't earned yet, so a low-level angler could end up fishing faster than someone who had put in the work.
- **Frenzy Potions are now a proper burst** — A Frenzy Potion sets your fishing cooldown to a flat few seconds for its duration rather than shaving a percentage off it, which is how the server-wide Fishing Frenzy event has always worked. It ignores the rod limit above entirely, so it's now a far bigger jump from your normal pace than it used to be — and it stays that way no matter how the limit is tuned in future. Fishing Frenzy events are completely unaffected.
- **Chests hand out fewer duplicate buff potions** — Buff potions were dropping faster than anyone could realistically drink them, since only one potion of each kind works at a time. Common and Rare chests now give out fewer Lucky Magnets and Energy Drinks, and Fisherman's Schnapps has moved up to the chests that suit its strength. In their place, chests are more likely to hold 🎒 **Materials Bags**, which feed guild camp upgrades and were far harder to come by than they should have been. Chests still hand out the same number of items — you'll just see fewer potions you were never going to get through, and more of what your guild actually needs. Fisherman's Ale and Rabbit Feet are unchanged: they're the early-game versions of those buffs and still drop where they always did.

## [0.9.7] - 2026-08-13

### Added
- **A card for finishing the journal** — Catching every species at all 27 locations now unlocks **The Complete Journal** achievement and the **Cartographer's Sea** profile-card background, on top of the World Cataloguer title you already earned for it. All 497 entries in `/collection`, ticked. If you'd already finished the journal before this update, just run `/collection` once and it's yours.
- **Send new materials straight to your guild** — `/autodeposit` routes every 🪵 log and 🪨 stone you earn from then on — Materials Bags you fish up and ones you open from your inventory — directly into your guild chest, with an entry in `/guild chest log` saying where it came from. It only affects future rewards: nothing already in your inventory moves, and `/guild chest add` still works by hand. Off by default, and if you're not in a guild your materials keep landing in your inventory as usual.
- **Guild owners can tax fish sales** — `/guild tax <percent>` sets a whole-number cut, 0% to 15%, of every member's fish sale that goes straight into the guild chest. Off by default; the Owner is the only one who can change it, and `/guild info` always shows the current rate so members can see it before they sell. It applies to every sale — `/fish`, tank bulk sales and net auto-sells alike — in DMs and any server, and the coins you see credited are what you actually keep. Automatic credits are recorded in `/guild chest log` — a bulk sale writes one entry for the whole lot rather than one per fish.
- **`/fishinfo` now tells you where a fish came from** — Inspecting a fish by its code shows a **Provenance** line: 🥚 Bred if it hatched in your breeding tank, 🎣 Wild-caught if you reeled it in. It is fixed when the fish comes into being, so selling, trading or moving it never changes the label, and fish you bred before this update are labelled correctly too.
- **Your guild is on your profile** — `/profile` now shows the guild you belong to, name and tag, on your fishing licence card. Compact mode shows it as a **Guild** field on the embed instead, reading `No guild` if you haven't joined one. Looking up another angler shows *their* guild. Your **Home Waters** server is a separate thing and is unchanged.
- **Leaderboard results in your own channel** — Server admins can opt in with `/settings leaderboard-results #channel` to have the completed **Weekly Fishing Champion**, **Monthly Fishing Champion** and **Top Server of the Month** results posted there. Off unless you set it; run it with no channel to turn it back off. The leaderboards are bot-wide, so every server that opts in sees the same global champion. Winners are still DMed and rewards are granted regardless of whether the announcement gets through.
- **Setup and DM guidance during onboarding** — The message posted when CozyCasting joins a server now lists the permissions it actually needs (never Administrator), separates the thread permissions that only `/trade` uses, flags anything it can see is missing in that channel, and explains that a channel override can deny what your role grants. The first-time player welcome now says plainly that commands only work in a server, that DMs are optional, exactly which reminders and invites they carry, and how to switch them on — with `/notifications` to pick which ones you want. The [Getting Started](https://cozycasting.github.io/Docs/getting-started/) and Server Admin guides carry the same checklist.

### Changed
- **Fishing feels snappier** — Newly caught fish are drawn several times faster, so the picture appears sooner and the bot no longer stalls for everyone else while it renders one. Starting a session, keeping a fish and selling a fish also do far less database work, which shows up as quicker button responses through a long session.
- **Sell and XP potions now lock in when a fishing session starts** — Drinking a sell or XP potion partway through a session takes effect from your **next** session rather than the current one. Your measurement units setting works the same way. Cooldown reduction still picks up a potion immediately, rarity potions already worked this way, and **switching bait mid-session still changes your very next cast** as before.
- **Big amounts are quicker to type** — `/give`, `/trade` and `/guild chest add`/`remove` now understand `k` and `m` shorthand, in either case: `2.5k coins` is 2,500 and `1.25m coins` is 1,250,000. An amount that can't be a whole number, like `1.2 rabbit feet`, now tells you so instead of quietly handing over a single one.
- **Guild chest material deposits are quicker** — Use `/guild chest add all logs`, `all stone`, or `all materials` to deposit everything you currently own.
- **Guild levels now ask for more pooled XP** — The XP each guild level needs has gone up roughly fivefold, so the XP bar on `/guild` fills over about a week rather than a single day. Coin and pearl costs are unchanged, and no guild loses a level it already holds — guilds part-way to their next level keep every point they have earned, they just have further to go.
- **`/guild info` tells you what the weekly mission pays** — The Weekly Mission field now shows the buff completing it earns and how long it lasts, so members can judge whether it's worth chasing before they contribute rather than finding out at rollover.

- **`/tank` lists fertility instead of size** — The fish list now shows each fish's 🥚 fertility percentage, which is what you actually pick a breeding pair by. Size and weight are still on `/fishinfo` and the fish detail view.
- **Bulk sales tell you what the guild tax took** — `/tank sell` and the bulk-sell picker show the same kept-versus-tax line `/fish` does, covering the whole sale.
- **Fishing tells you what the guild tax took** — Selling a fish from `/fish` now shows what you kept, what the sale was worth before tax, and how much went to your guild's chest at what rate. The session summary shows the same for the whole session. The coins credited are unchanged — they were already net of the tax; now the embed says so instead of quietly disagreeing with the fish's listed value.
- **Fishing cooldowns now show as live countdowns** — The cooldown on the `/fish` session embed is a Discord timestamp, so it stays accurate as the message sits in the channel instead of freezing at whatever it said when it was posted.

### Fixed
- **`/gear` no longer errors out** — The command crashed for anyone with a gear item equipped that carries a bonus.
- **Fishing now explains missing channel permissions** — `/fish` and its session buttons identify the permissions CozyCasting needs instead of ending with a generic error when a channel override blocks access.
- **Slash commands now remain available on the development bot** — Dev command sync no longer immediately deletes the commands it just registered.
- **Seasonal fish no longer block a location from ever being finished** — Blossom Koi, Sunburst Angelfish and Frostbite Flounder were listed in the ordinary Pond, Ocean and Arctic species pools, but they can only be caught with seasonal bait during their season — so if you missed that season, those locations could never be completed, and the location bonus, naturalist titles, World Cataloguer, The Complete Journal and the Cartographer's Sea background were out of reach for good. They have been taken out of those pools, so every location is completable again. Run `/collection` once and anything you're now owed is granted.

    Two things you'll notice. Each Pond, Ocean and Arctic now asks for one fewer species, so the journal total drops from 506 to 497. And if you *had* caught a seasonal fish in its matching water, it no longer counts toward that location, so your caught number can go down too — an angler on 134/506 with both Arctic seasonals lands on 132/497. Nothing was taken away: those locations are now one fish short of a fish you can actually go and get, instead of one short of a fish you couldn't.

    Your seasonal catches are safe — still in your tank, still worth what they were, and seasonal bait works exactly as before. They just don't appear in the journal for now; they're getting their own section in a future update.
- **Every background you've earned is now reachable in `/card`** — The background menu could only ever show 25 options, so anglers who had unlocked more than that — anyone well into their collection journal — simply could not see or equip the rest. Backgrounds are now grouped by how you earned them, with a category menu above the picker, and it opens on whichever group holds the one you're currently using. The frames menu, which never had any art behind it, is gone for now; frames are still coming.
- **Double catches now mention Beginner's Luck** — Unlocking the Beginner's Luck buff on a double catch granted the faster bites but never said so. The keep/sell result now names it, exactly as a single catch already did.
- **`/gear` was understating your bonuses** — The **⚡ Combined Effects** panel worked out its own numbers instead of using the ones the game applies, and left your guild out entirely — anyone in a guild with an active mission buff saw a longer cooldown than they actually had. Every line now comes from the same place `/fish` reads, so cooldown, rarity, sell, XP and bait-saving all include your gear, potions, server buffs, guild buffs, lucky charm and journal completion. Each line now breaks down which source contributed what.

## [0.9.6] - 2026-08-07

### Changed
- **Pearl Bags are less common in high-tier chests** — Legendary and seasonal chests now award fewer Small and Medium Pearl Bags.

### Fixed
- **Extra Title Pouches now become Voting Tickets** — Opening a pouch after collecting every title now consumes it and awards one 🎟️ Voting Ticket instead of refunding the pouch and awarding coins. Opening several at once grants any remaining unique titles first, then one ticket for each extra pouch.

## [0.9.5] - 2026-08-07

### Changed
- **Guild levels now need your guild to actually fish** — `/guild upgrade` still spends 🪙 coins and 🦪 pearls out of the chest, but it now also requires ⭐ **guild XP**, and that can only be earned one way: members fishing. Every point of catch XP anyone earns is mirrored into the guild automatically — no new command, no "donate XP", nothing to remember. Quest rewards and redeem codes don't count; this counter measures fishing.
    - **A level now means something.** One rich member could bankroll every upgrade before. They still can't be stopped from covering the coins, but nobody can buy their way past the requirement that people actually turn up and fish. Thresholds are tuned so a typical roster clears a level in about **two weeks**.
    - **Guild XP never goes down.** If a member leaves or gets kicked, everything they earned stays banked in the guild.
    - **Existing guilds keep their level** — every guild has been credited with the XP for the level it already holds, so you start the next tier from a clean slate rather than being stranded.
    - **`/guild info` shows all three bars** — guild XP, coins and pearls, each with your progress, so you always know which one is holding you back. If you're short on an upgrade, the error names *everything* you're missing at once instead of one thing at a time.
    - **`/guild members` is a leaderboard now** — the detailed roster shows each member's ⭐ guild XP contribution and ranks by it, so carrying the guild is visible.

## [0.9.4] - 2026-08-07

### Added
- **Guilds are here** — Full write-up in the [Guilds guide](https://cozycasting.github.io/Docs/guides/guilds/) and the [command reference](https://cozycasting.github.io/Docs/commands/guilds/). Buy a 🏰 Guild Token from `/shop` → **Guild** for 🪙 1,000,000, then `/use guild_token` to name your guild and pick a tag. Invite people with `/guild invite` and they'll get a DM to accept or decline. `/guild members` shows the roster, `/guild promote` and `/guild demote` manage your Mods, and `/guild info` shows any guild's level, bank and buffs. You can be in one guild at a time, with a 24-hour wait before joining another after you leave.
    - **Level your guild up with `/guild upgrade`** — The Owner and Mods spend coins **and** pearls straight out of the guild bank to raise the level; you need both currencies, and `/guild info` always shows what the next level costs and what the bank is holding. The money is spent for good, so cycling deposits in and out can't cheat levels.
    - **Every guild level is worth having** — Each level adds **+10 roster slots** (10 at level 1, all the way to 50 at level 5) and gives every member **+2% sell value and +2% catch XP** per level, stacking up to +8% each.
    - **Build a guild camp** — `/guild camp` shows seven buildings you can raise to tier 5 with `/guild camp upgrade`, which asks you to confirm and shows exactly what the bank holds before it spends a coin. **Lure Workshop** makes fish bite sooner, **Library** boosts catch XP, **Chapel** boosts your rare-fish chance, **Bait Hut** gives a growing chance your catch doesn't use up your bait, **Logging Camp** and **Stone Camp** produce materials daily based on how many members have been fishing, and **Storehouse** expands the chest. Upgrades come out of the guild bank, never your own pockets, and a building can never outrank the guild itself.
    - **Share a guild bank** — `/guild chest` holds coins, pearls, logs, stone and 25+ item slots. Depositing is plain English: `/guild chest add 20 pearls`, `500 coins`, `3 logs`, `2 energy drinks`, or a fish/gear code — yes, you can stash fish and found gear in there too. Any member can add; only the Owner and Mods can remove, and `/guild chest log` records every movement so nobody has to guess who took what.
    - **A new guild mission every week** — Every guild works toward the same goal each week — catch fish, earn coins, or land Rare-or-better catches — scaled to your guild's size. Hit it and the whole guild gets a −5% fishing cooldown for the following week. `/guild mission` shows live progress and who's carrying.
- **Materials Bags while you fish** — Casts sometimes pull up a 🎒 Materials Bag full of 🪵 logs and 🪨 stone. It's a freebie: a bag doesn't use up a cast, so the fish after it is exactly as likely to stay on the line as if the bag had never shown up, and your chest luck is untouched. Epic and Legendary chests can also contain bags. Materials live in a new **Materials** tab in `/inventory` and fund your guild camp.
- **Daily quests now fit where you can travel** — Personal location quests only appear when you can reach that kind of fishing spot. You can also reroll one unstarted personal quest each day from `/quests` if you'd rather take a different challenge.
- **Find the Roaming Trader every Thursday** — He hides at one fishing location for 24 hours with two pieces of powerful Caravan Gear and three rotating consumables, all sold for voting tickets. Use `/trader` wherever you are to check; he won't reveal where he's hiding. New Fertility Tonic restores fertility with `/breed restore`, and Caravan Coffee makes fish bite faster.
- **Be first to find the Roaming Trader** — The first angler to discover each week's caravan earns the one-time Caravan Pathfinder achievement and its exclusive Caravan Trail profile-card background.
- **Monster fish get announced too** — Landing the beast at the end of a monster fight now posts to your server's rare-catch channel, the same way a Mythical or Unique catch from `/fish` does, ping role included. Set it up with `/settings rarecatch`.
- **Catch a Monster Fish to earn an exclusive profile background** — Your first successful monster catch unlocks the **Monster Hunter** achievement and the **Monster's Wake** background in `/card`. Anglers who already own a Monster Fish receive it too.
- **Look up any fish species with `/fishinfo`** — Search by fish name to see where it can be caught, location level requirements, typical size and weight in your preferred units, common colors and patterns, and seasonal bait availability. Fish and gear codes still work too.
- **See who used your referral code** — `/referral` now lists the people you've referred, split into ⏳ Pending with the level they're at so you can see who's close to paying out, and ✅ Completed. Anglers who haven't fished in 30 days drop off the list, so it stays a list of people worth nudging — your Completed and Pending counts still include everyone.

### Changed
- **Monster fights need 2 anglers instead of 3** — Too many monsters were swimming off because a third person didn't hit **Join the Fight!** in time. Two is now enough to start.
- **Leaderboard time filters renamed** — `/leaderboard` now says "Past 7 Days" and "Past 30 Days" instead of "This Week" and "This Month", matching the rolling windows it always used.
- **Monster fish are a little easier to land** — The chance for the top scorer in a monster fight to actually reel the beast in has gone from 3% to 5% (higher with a better rod). Nobody had caught one yet.
- **Seasonal chests are rarer now that nothing gates them** — When a chest drops from fishing, it used to be seasonal 20% of the time. That's now 10%. The scarcity moved out of the key and into the drop itself, so a seasonal chest is a real find rather than something you sat on waiting for a key.

### Removed
- **Chest Keys are gone** — Seasonal chests now open straight from `/inventory` with `/chest <type>`, exactly like Common, Rare, Epic and Legendary ones. No key, and no daily open limit tied to your level. **Every key you were holding has been turned into a Summer 2026 Chest, one for one** — nothing was lost and you don't need to do anything. Keys are no longer sold in `/shop` and can no longer be traded.
    - Vote Tickets keep their home with the **Roaming Trader** every Thursday, and more places to spend them are on the way.

### Fixed
- **Monster fish say where they came from** — A caught monster showed a raw internal id under **Caught At** in `/tank`. It now reads "Monster Event" with the region it happened in.
- **Event tokens can actually be bought** — The Events tab in `/shop` told you to use `/buy token <name>`, but the command rejected `token` as an invalid item type, so there was no way to buy a 🌊 Fishing Frenzy Token at all. It works now.
- **Energy drinks work when you drink them mid-session** — Using a 🥤 Energy Drink after you'd already started fishing did nothing to the cooldown you got at the end of that session, because the buff was checked when you cast rather than when you finished. It now counts. If your drink runs out partway through a session, you still keep the shorter cooldown for it.
- **Net catches count for your collection at the stream** — If you'd never used `/travel`, everything your net brought in was filed under a spot the collection journal didn't recognise, so `/collection` showed nothing for Appalachian Stream no matter how many nets you emptied. Those catches are now credited, including the ones you've already collected.
- **`/refer`, `/referral` and `/chest` stop timing out** — All three did their database work before telling Discord they'd been received, so on a slow day you got "The application did not respond" instead of your rewards. They now answer first and work second.
- **Come-back reminders reach lapsed anglers again** — A nightly cleanup was clearing the record of when you last fished after a week away, which quietly deleted you from the win-back reminder list, so the 14-day "we miss you" DM never arrived. Last-fished times have been rebuilt from your catch history and are never wiped again.

## [0.9.3] - 2026-07-31

### Changed
- **Shop gear can't be salvaged** — `/salvage` now only accepts gear you found, not gear you bought. Buying ten cheap items was a cheaper route to a chest than earning one. Shop gear no longer shows up in the salvage list; use `/destroy` to clear it out.

### Fixed
- **First-timers can claim community chests and join monster fights** — If you'd never used the bot before, clicking **Claim!** on a chest drop or **Join the Fight!** on a monster fish would fail to hand out the reward. Joining now signs you up as an angler, so the prizes actually land. Related: if the bot first met you through something other than `/fish` — a chest claim, `/profile` — you never received your starter rod. Your first `/fish` now hands it over.
- **`/card` opens again for everyone** — If you'd earned both the achievement and the title for your first catch, the stamp menu listed it twice and Discord refused to show the card at all. The menu now lists each stamp once.
- **`/card` menus stop snapping back to your old pick** — Choosing a new background updated the card but the menu jumped back to the one you started with, which then made it impossible to switch back. The menus now show what you actually have equipped.
- **Redeem codes name your rewards properly** — Claiming a code listed rewards by their internal id, so an Epic Chest showed up as "epic". It now shows the real item names.
- **Long fish names no longer eat the numbers on your profile card** — A very long species name pushed the coin value off the end of the **Most Valuable** line. The value now drops onto its own line underneath, so you see the whole name *and* what it's worth. The showcase caption keeps its size and value too.

## [0.9.2] - 2026-07-31

### Changed
- **`/profile` is a real slash command** — Your profile was `/info` in the slash menu and `/profile` only worked as a `!f` text command. It's `/profile` now, the way everyone was already typing it. `!finfo` and `!fme` still work.
- **Pearl fish are easy to spot** — Pearlescent fish now show a 🦪 wherever fish are listed, so you can tell at a glance which of your catches will earn pearls in the camp display tank. Bulk sell warns you before you sell one.
- **`/version` is shorter** — It now shows the version you're on plus buttons to the full patch notes: the new [Changelog page](https://cozycasting.github.io/Docs/changelog/) on the docs site, and the `#changelog` channel in our Discord.

### Added
- **Profile cards** — `/profile` now shows a rendered fishing licence: your avatar, level, lifetime catches, fish bred, contest wins, best streak, home server and your most valuable catch, with that fish shown off on the card. Use `/card` to pick a background, a frame, a name style, up to six stamps from the achievements and titles you've earned, and a different fish to display. Prefer text? `/compact` switches `/profile` back to a plain embed.
- **Collect every fish at a location** — Catch every species a location has to offer and you unlock three things: that location's artwork as a `/profile` card background (27 in all, one per fishing spot), a permanent **+0.5% rarity bonus** that applies *everywhere* you fish, and half of that at the halfway mark. Finish all nine locations in a region for a **Naturalist** title, or all 27 for **World Cataloguer** — and a fully complete collection is worth **+13.5% rarity**, stacked on top of your rod, bait and buffs. Your session summary tells you the moment you finish one, and `/fish` shows what your collection is currently worth. Only fish you caught yourself count; traded-in and bred fish don't.
- **Gear salvage** — `/salvage` turns 10 unequipped gear items into a chest: **60%** Rare, **30%** Epic, **10%** Legendary. Pick what to scrap from a paginated list, same as bulk selling fish. Equipped gear is never shown, so your loadout is safe. The chest lands unopened — you'll still need a key.
- **Contest leaderboards** — `/leaderboard` → **Contest** shows the live standings for the weekly and monthly "most fish caught" competitions, with a button to toggle between them. It shows the prize, the time left in the period, and where you're placed.
- **Rare catches can be announced in a thread** — `/settings rarecatch` now accepts a thread as well as a channel, so Mythical and Unique catches can go somewhere tidy instead of your main chat. Archived threads still work — the announcement wakes them back up.

### Fixed
- **Casts no longer die when Discord hiccups** — If Discord was briefly unavailable while your catch was being shown, the retry could fail outright and end your fishing session. It now retries properly.
- **Fewer double error messages** — When a command failed, some commands replied with two error messages at once. Now you get one.
- **Announcement channels are checked when you set them** — `/settings rarecatch` and `/settings channel` used to happily accept a channel the bot couldn't post in, then silently drop every announcement. They now tell you exactly which permissions are missing instead of confirming a setup that won't work.

## [0.9.1] - 2026-07-28

### Changed
- **Selling won't surprise your display tank** — Fish sitting in your camp display tank are now marked with 🖼️ in bulk sell and `/sell`, and you get a warning before you confirm the sale.

## [0.9.0] - 2026-07-27

### Added
- **Server of the Month** — The server whose members catch the most fish in a calendar month wins a **7-day Rarity Boost for everyone in it** (+15% rare fish chance). Watch the race live with `/leaderboard` → **Servers**. Only `/fish` catches count, so nets and breeding don't tip the scales.
- **Rare catch announcements** — Server admins can set a channel with `/settings rarecatch`, and every **Mythical** or **Unique** catch gets announced there with the fish, who caught it, and an optional role ping. Leave the channel off to turn it back off.
- **Referrals on your profile** — `/profile` now shows how many friends you've referred, with a nudge toward `/referral` if you haven't tried it yet.
- **A gift for coming back** — If you've been away a few days, we'll send you a DM. Your gift is waiting on your next `/fish`. Toggle these in `/notifications`.
- **A proper welcome** — New players now get the getting-started guide right after their first cast, so it can't be missed if your DMs are closed. It now points to `/quests`, `/travel` and `/referral` too.

### Changed
- **Frenzy Potion buffed** — Now cuts your fishing cooldown by **98%** (was 75%), and the minimum cooldown floor dropped from 60s to 15s so you actually feel it. Worth drinking at every rod tier.

### Fixed
- **Fishing lockout** — Casting in a channel the bot can't post in could leave you permanently stuck on "🎣 You already have a fishing session going!" until the bot restarted. Fixed, and any stuck session now clears itself. The bot also tells you plainly when it's missing channel permissions instead of asking you to try again.
- **Referral abuse** — Brand-new Discord accounts (under 30 days old) can no longer redeem referral codes.

## [0.8.4] - 2026-07-21

### Fixed
- **Event buffs no longer block your consumables** — Special event buffs (like a riddle's cooldown reduction) now sit in their own bucket. They no longer stop you from using a consumable buff of the same type, and the two stack. The one-at-a-time limit still applies between consumable buffs of the same type.

## [0.8.2] - 2026-07-13

### Added
- **Keep Fishing button** — When a Fishing Frenzy is active, the end-of-session summary now has a 🌊 **Keep Fishing** button. Tap it to jump straight into a new session on the same message — no need to type `/fish` again.

### Fixed
- **Community chest claim window** — The winner is now always drawn exactly 60 seconds after a chest drops. Previously, each **Claim!** click could push the draw back, so busy drops took much longer than 60s to pick a winner.
- **Consumed buff on duplicate** — Using a timed buff while one of the same type is already active no longer consumes the item. Your consumable now stays in your inventory when the activation is blocked.

## [0.8.0] - 2026-07-06

### Added
- **Summer 2026 Chest** — A brand-new seasonal chest is now the active season! Open it with a Chest Key for sun-soaked loot, including a chance at exclusive Summer 2026 seasonal titles.
- **Summer 2026 Sunglasses** — A limited-edition hat that grants a **+5% rarity boost**. It can *only* be found in the Summer 2026 Chest, with a **25% chance** to drop each time you open one.
- **Summer 2026 Seasonal Titles** — Eight new titles to collect from the Season Title Pouch (Summer 2026).
- **Sunburst Angelfish** — A vibrant new seasonal fish you can lure in using Seasonal Bait.

## [0.7.2] - 2026-07-03

### Added
- **Random Events** — Keep fishing and you might stumble into a mysterious encounter, appearing just for you when a session ends. A riddling stranger, a lucky frog, a wish upon a star... there are currently **10 to discover**.
- **Weekly & Monthly Leaderboards** — Compete for the most fish caught each week and each month! Check `/leaderboard` with the Weekly or Monthly filter.
- **Champion Rewards** — The top fisher (Globally) each period earns a brand-new **Unique Chest** plus pearls:
  - 🏆 Weekly #1 → **1 Unique Chest + 100 pearls**
  - 👑 Monthly #1 → **2 Unique Chests + 250 pearls**
- **Unique Chest** — A special reward chest that always contains a **Rare-or-better** crafted piece of gear. Open it with `/chest unique`.

### Improved
- **Monster Fish Catch Rate** — Your rod quality now meaningfully improves the chance to reel in a Monster Fish when you finish 1st. (It always did, but now it impacts it more!)

## [0.6.9] - 2026-06-08

### Added
- **Inactive Server Pruning** — New dev command to list or leave servers with no fishing activity, helping keep the bot focused on active communities.

### Improved
- **New User Notifications** — Owner notifications for new users now include which server they joined from.

## [0.6.8] - 2026-06-04

### Fixes
- **Duplicate Commands** — Fixed an issue where slash commands appeared twice when the bot joined a new server.

## [0.6.7] - 2026-05-31

### Fixes
- **Times** - Added some additional logic on times to ensure they should end when they do.

## [0.6.6] - 2026-05-27

### Fixes
- **Breeding Sessions No Longer Cancelled on Sell** — Selling a parent fish after the egg was produced no longer cancels the breeding session. Eggs, incubating sessions, and hatched offspring are now safe.
- **Monster Fish Join Phase** — The signup window now stays open for the full 60 seconds instead of closing early when 3 players joined.

### Changed
- **Monster Fish Tiebreaker** — Players with the same score now have a random chance at each placement instead of the earliest joiner always winning.

## [0.6.5] - 2026-05-24

### Added
- **Daily Summary Reports** — The bot now posts daily, weekly, and monthly activity summaries to the dev/log channel at midnight UTC. Includes new users joined and server join/leave stats.

## [0.6.4] - 2026-05-24

### Changed
- **Modified Various Timeouts** - Community Chest Claim is now 60 seconds | Monster Fish is 60 second join, 5 second rounds
- **Beginners Luck Extended** - New anglers now get 24 hours of reduced fish-waiting time. 

## [0.6.3] - 2026-05-22

### Added
- **Session Summary Recap** — The session-over screen now shows all achievements unlocked and quests completed during your fishing session.

### Changed
- **Quest Bonus Chest Rework** — Completing all 3 daily quests now rewards a random chest instead of always a Common Chest. Higher rarity chests have a small chance to drop.
- **Quest Completion Streak** — Completing all daily quests on consecutive days builds a streak. Higher streaks improve your odds of getting rarer bonus chests.

## [0.6.2] - 2026-05-18

### Changed
- **Pearlescent Fish Can't Breed** — Pearlescent fish now have 0 fertility, making them unable to breed.
- **Pearl Income Cap** — Display tank pearl income is now capped at 50 pearls per day (up to 150 for a full 3-day collection).
- **Pearly Fish** - Pearlescent fish now have their trait displayed in their name.

### Fixes
- Fix an issue where you could collect pearls/bait/coins indefinitely instantly
- Fix an issue where some locations didn't count towards travel achievements.

## [0.6.1] - 2026-05-10

### Added
- **Documentation Site** — A new player-facing documentation site at https://cozycasting.github.io/Docs with guides, command references, and tips. The `/docs` command provides a direct link.
- **Feedback Command** - Users can now send feedback to the developer via the `/feedback` command.

## [0.6.0] - 2026-05-09

### Added
- **Fish Appearance Rendering** — Every fish you catch now gets a unique rendered image based on its species, colors, pattern, traits, and rarity. No more generic fish pictures!
- **Colorized Fish Bodies** — Fish are tinted with their primary color, with secondary colors shading the belly region.
- **Pattern Overlays** — Spotted, striped, banded, marbled, gradient, speckled, and seasonal patterns are visually rendered on each fish.
- **Trait Effects** — Bioluminescent glow, iridescent shimmer, scars, pearlescent highlights, albino, and golden traits all have unique visual effects.
- **Rarity Glow** — Epic and above fish display a colored glow outline (purple, gold, red, or rainbow).
- **Fish Images in Embeds** — Catch results and `/fishinfo` now display the fish's unique rendered image.

## [0.5.3] - 2026-05-01

### Fixes
- Fix an issue with voting not counting
- Fix an issue with `/info` not working

## [0.5.2] - 2026-04-30

### Added
- **Player Trading** — Two new commands for moving items between players:
  - `/give <target> <item> [quantity]` — One-way transfer. Supports fish (8-char short code), gear (6-char short code), bait, consumables, chests, keys, and currency (coins, pearls, voting tickets). Shows a sender-only confirmation before transferring.
  - `/trade <target>` — Interactive multi-item trade. Both players type items into chat to add them to their offer, review the window, and accept. Adding or removing any item resets both acceptances to prevent bait-and-switch. Atomic finalization with full re-validation.
- **Trade cooldown** — 60-second per-user cooldown on `/give` and `/trade` initiation.
- **Beginner's Luck** — New players receive a 1-hour buff after their first achievement that makes bites come 75% faster, helping them get hooked on fishing right away.

## [0.4.3] - 2026-04-22

### Added
- **Monster Fish Event** — A massive monster fish can now appear while fishing! When one spawns, players join a cooperative boss fight — a 45-second reaction minigame where you strike the monster's weak spot each round. Top 3 players earn chest rewards (Legendary + Seasonal, Epic, Rare), and the #1 player has a rare chance to catch the monster as a Unique-rarity fish. Better rods improve your catch odds.
- **30 Monster Fish Species** — 10 unique monster species per region (NA, Asia, Europe) with custom descriptions and stats. These powerful fish are only obtainable through the Monster Fish event.
- **Catch The Monster** - Small chance for the 1st place winner to catch the fish. Chance is dependant on their rod.

## [0.4.1] - 2026-04-02

### Added
- **Top.gg Stats Autopost** — Bot server count and shard count are now automatically posted to Top.gg every 30 minutes.

## [0.4.0] - 2026-03-24

### Added
- **Fish Breeding** — Pair two compatible fish in your Breeding Tank to produce offspring! Use `/breed start <code1> <code2>` to begin.
- **Genetic Inheritance** — Offspring inherit species, rarity, and traits from their parents. Higher-rarity parents produce higher-rarity offspring.
- **Breeding-Only Mutations** — Three new traits exclusive to breeding: **Gilded** (golden shimmer), **Bioluminescent** (glowing teal), and **Colossal** (massive size beyond Giant).
- **Egg Hints** — When your breeding pair produces an egg, you'll get hints about the offspring's species and rarity before hatching.
- **Breeding Notifications** — Receive DMs when your egg is ready to hatch and when your offspring is ready to collect. Toggle with `/settings`.
- **Breed Commands** — `/breed`, `/breed start`, `/breed hatch`, `/breed collect`, `/breed cancel` for full breeding management.

## [0.3.6] - 2026-03-23

### Added
- **Spring 2026 Season** — New seasonal chest with exclusive spring-themed rewards! Find 🌸 Spring 2026 Chests while fishing.
- **8 New Seasonal Titles** — Collect bloom-themed titles from Season Title Pouches: Petal Caster, Bloom Angler, Spring Tide, Garden Fisher, Blossom Reeler, Verdant Hook, Rainwater Rod, and the legendary Eternal Bloom.
- **Blossom Koi** — A rare cherry-blossom patterned koi exclusive to seasonal bait. High value and only found in rare+ rarities!

### Changed
- **Season Rotation** — Winter 2026 season has ended. Existing Winter chests can still be opened, but new chest drops are now Spring 2026.

## [0.3.5] - 2026-03-23

### Added
- **Leaderboard Navigation** — `/leaderboard` now has category buttons to switch between Fish Caught, Largest Fish, Most Valuable, Highest Level, and Highest Streak without retyping the command.
- **Tank Expansion** — Tank upgrades now go up to **100 slots** (was 60).
- **Auto-updating Cooldown Timer** — `/cooldown` now shows a live countdown that updates automatically.
- **Quest Reward Scaling** — Quest coin rewards now scale with your level, making quests more rewarding as you progress.
- **Reset Timers** — `/quests` and `/daily` now show when they reset with a live countdown.

### Fixed
- **Net Collection Display** — Fixed a bug where keeping fish from a net that also contained chests showed incorrect "Kept" / "Sold" labels.

## [0.3.4] - 2026-03-06

### Added
- **Bulk Sell** — Your `/tank` now has a 💰 Bulk Sell button. Toggle individual fish or entire pages for sale, then confirm in one click. No more copying short codes!
- **Referral System** — Share your referral code with friends using `/referral`. New players use `/refer <code>` before level 4. When they reach level 5, you get **150 pearls** and they get **100 pearls**!

### Fixed
- **Session Bugs** - Triggering a session, not casting, no longer triggered cooldown after timing out. 
- **Increased Net Catch** - From 1 hour to 2 hours

## [0.3.3] - 2026-03-03

### Added
- **Categorized inventory** — `/inventory` now has category tabs (Rods, Baits, Chests, Items, Gear) instead of one giant list. Click tabs to switch between sections.
- **Mid-session bait switching** — Change your bait between catches during a fishing session. A "Bait" button appears after each catch or chest, letting you swap without ending your session.

## [0.3.2] - 2026-03-02

### Added
- **Fish anytime** — `/fish` is now always available, even on cooldown. If you're on cooldown, you can use a 🎟️ Fishing Ticket to start casting right from the session screen.
- **Highest Streak leaderboard** — New `/leaderboard` category showing the top session streaks.
- **Admin notifications** — Bot owners can now receive alerts when a player reaches a level milestone (every 5 levels) or catches a high-value fish (300k+ coins). Configure with `!fnotifyconfig level` and `!fnotifyconfig highvalue`.

### Changed
- **Tank slot pricing rebalanced** — Base cost increased from 1,000 to 2,000 coins with a steeper 1.8× multiplier per purchase.
- **Fishing Ticket drop rates reduced** — Tickets are now rarer drops across all chest types, making each ticket feel more valuable.

## [0.3.1] - 2026-03-01

### Added
- **Session summary** — When a fishing session ends (miss, timeout, or manual end), a summary embed shows total fish caught, kept/sold split, coins earned, XP earned, chests found, and best streak.
- **Best sell value achievements** — Profitable Catch (1k+), Big Fish Energy (10k+), Whale Hunter (100k+) — track your single best fish sale and unlock titles.
- **Streak quests** — Hot Hands (5 streak) and Can't Stop (10 streak) daily quests reward session streaks.
- **Fishing frenzy recording** — Fish catches now properly record to the frenzy service for community frenzy events.
- **Ticket usage notification** — When a Fishing Ticket is auto-used to skip cooldown, the session start embed now shows a 🎟️ indicator.
- **Streak rarity bonus** — Each consecutive catch in a session grants +1% rarity bonus, capped at +10%. Displayed in the catch embed.
- **Double catch in sessions** — Double catches now trigger inline within the fishing session (4-button Keep Both / Sell Both / mix), no separate view spawned.
- **Streak achievements** — Hot Streak (5 catches, 500 coins), On Fire (10 catches, 2,000 coins + consumables), Unstoppable (25 catches, "Unstoppable" title).
- **Steady Hands Potion** 🧴 — New consumable that reduces fish escape chance by 10% for 1 hour. Drops from Epic and Legendary chests.

### Fixed
- **Gear cooldown reduction** not applying to new fishing mode fixed.

### Changed
- **Location fish ordering** — Regional fish now appear before shared species in `/locations` display, making each region look distinct.
- **Quest targets bumped** for session-based fishing: Casual Fisher 5→10, Dedicated Angler 15→30, Quick Seller 3→8, Tank Builder 3→8, Baited 5→10, Ocean/Cave/River location quests 3→5.
- Epic chest loot table now includes Steady Hands Potion.
- Legendary chest loot table now includes Steady Hands Potion.

## [0.3.0] - 2026-03-01

### Added
- **Fishing Sessions** — `/fish` now starts an active session! Press Cast Line, wait for a bite, then Keep or Sell your catch — and Cast Again to keep going. Consecutive catches build a streak.
- **Escalating escape rate** — First cast is a guaranteed catch. Each subsequent cast has an increasing chance the fish escapes, ending the session.
- **Fishing Ticket on miss** — If a fish escapes and you have a Fishing Ticket, you can use it to continue the session with a guaranteed next catch.
- **Chest catches** — During a session, you may reel in a chest instead of a fish (same drop rate as before). Chests count toward your streak.
- **Streak tracking** — Current session streak and all-time best streak are now tracked on your profile.
- **Escape Reduction** — New `ESCAPE_REDUCTION` effect type for future consumables that lower the escape rate.

### Changed
- **Base cooldown** increased from 10 minutes to 15 minutes (applied once per session, not per cast).
- Fishing is now session-based: one cooldown per session instead of per catch.
- Bait is consumed only on successful fish catches (not on chest catches or misses).

## [0.2.7] - 2026-02-28

### Added
- **Frenzy Potion** ⚡ — New consumable that reduces your fishing cooldown by 75% for 5 minutes. Semi-rare drop from Seasonal (Winter 2026) chests.
- **Quest completion notifications** — The keep/sell result embed now shows a "📋 Quest Complete!" field when one or more quests are completed by that action.
- **Immediate cooldown reduction** — Using an Energy Drink (or any COOLDOWN_REDUCTION consumable) now instantly reduces your remaining fishing cooldown by 50% in addition to activating the future buff.
- **Lucky Magnet** — New consumable that increases chest drop chance by +5% for 1 hour. Drops from Common and Rare chests.
- **Gilded Magnet** — Premium consumable that increases chest drop chance by +15% for 1 hour. Drops from seasonal chests only (Winter 2026+).
- **Chest Drop Chance effect** — New `CHEST_CHANCE` effect type. Stacks additively with the base 7% drop rate; capped at 35% total.
- **Double Catch mechanic** — A chance to reel in two fish on one cast. Each fish is an independent rarity/species roll.
- **Lucky Double Worm** 🪱🪱 — New bait with 15% double catch chance and +5% rarity bonus. Drops from Rare chests and Level-3+ Bait Bin.
- **Twin Hook Token** 🪝 — New consumable granting 10% double catch chance for 1 hour. Drops from Epic and Legendary chests (not tradeable).
- **Double catch UI** — A 4-button view (Keep Both / Sell Both / Keep 1st Sell 2nd / Sell 1st Keep 2nd) fires for double catches with full quest, achievement, and level-up tracking for each fish.

### Changed
- **Level-appropriate personal quests** — Your personal daily quest is now filtered to quests appropriate for your level (e.g. beginners won't get "catch epic fish"). Shared quests remain basic quests all players can do.
- **Quest progress on first fish** — Quests are now assigned automatically when you keep/sell a fish, so the fish that triggers quest generation also counts toward progress.

## [0.2.6] - 2026-02-28

### Added
- **Daily Quest System** — 3 quests per day (2 shared globally + 1 personal random). Quests include catch targets, rarity hunts, location-specific catches, selling goals, and bait usage. Rewards scale with level (XP + coins). Complete all 3 to earn a bonus Common Chest. View and claim via `/quests`.

### Changed
- **Fish Value Scaling Overhaul** — Values can no longer expotentially grow (Had epic fish worth 8+ million)
- **Chest Key ticket cost** reduced from 20 to 15 tickets
- **Fishing timeout** — Embed now greys out and shows "The fish managed to slip away..." when catch expires, buttons are removed
- **/gear command** — Each gear slot now shows its bonus inline (e.g. `Coral Crown — Rarity Boost +3.0%`)
- **/inspect command** — Now works for both fish and gear items (auto-detects by short code)

### Fixed
- **Gear short code collisions** — Added salt-based retry logic matching the fish collision handling



## [0.2.5] - 2026-02-25

### Changed
- **Economy Rebalance** — Tightened endgame values to prevent runaway inflation:
  - Legendary rarity sell multiplier reduced from 30x to 20x
  - Mythical rarity sell multiplier reduced from 100x to 50x
  - Volcano location base value reduced from 80 to 60
  - Arctic location base value reduced from 100 to 75
- **Rod prices increased** to slow mid/late-game progression:
  - Carbon Fiber: 8,000 → 25,000
  - Titanium: 25,000 → 75,000
  - Legendary: 100,000 → 250,000
  - Mystic: 500,000 → 1,000,000 (rarity bonus 50% → 40%)
- **Bait rebalance** — Golden Lure and Magic Bait are now single-use premium baits:
  - Squid cost increased from 100 to 500
  - Golden Lure: now single-use, cost 5,000 → 2,500, rarity bonus 5% → 20%
  - Magic Bait: now single-use, cost 10,000 → 6,000, rarity bonus 35% → 30%
- **Display tank income nerfed** to cap passive income:
  - Daily income rate reduced from 10% to 5% of fish value
  - Max accumulation reduced from 7 days to 3 days
  - Per-fish daily cap: 25,000 + 10,000 per display level (25k at L1, 65k at L5)
  - Total daily cap across all fish: 100,000 coins
- **Camp building costs increased ~1.5x**: 10k/25k/50k/100k/200k → 15k/40k/75k/150k/300k
- Renamed `amount` parameter to `quantity` in `/use`, `/chest`
- **Fishing embed** now shows `@player Title caught a Fish!` instead of generic "You caught a..."
- **Keep/Sell result** now reminds the player if they also found a chest with that catch

### Fixed
- Shop now correctly shows "Owned" status for purchased rods instead of "Available"
- Shop now correctly shows "Equipped" status for the user's current net
- Short code hash collisions no longer cause crashes — retries with a salted hash using savepoints

## [0.2.4] - 2026-02-25

### Added
- `/destroy <codes>` command to permanently destroy unwanted gear (aliases: `/scrap`, `/discard`)
  - Accepts comma-separated gear codes (e.g. `/destroy a3f2e1,b4c5d6`)
  - Shows confirmation before destroying; auto-unequips equipped gear
- `/sell` now accepts comma-separated fish codes (e.g. `/sell A3F2E1C9,B4C5D6E7`)
  - Shows total value and confirms before selling all
- `/camp upgrade` now shows building autocomplete suggestions
- Configurable notification roles for server events (admin-only, requires Manage Server)
  - `/settings notify-events @Role` — ping a role when Fishing Frenzy (or future events) start
  - `/settings notify-chest @Role` — ping a role when Community Chest Drops appear
  - Reset with `/settings notify-events-reset` and `/settings notify-chest-reset`
  - Roles shown in `/settings view`

### Changed
- Fish value now scales relative to each species' own base size/weight instead of a hardcoded baseline — small rare species (e.g. Fire-Bellied Toad) are no longer penalized for being naturally tiny
- Fish weight now factors into value calculation — heavier specimens within a species are worth more
- Locations that require a higher level to unlock now give increased coin value (+3% per level required) and XP (+2% per level required) — Asia/Europe locations are more rewarding than their NA equivalents

### Fixed
- Fishing Frenzy scheduled trigger could fire after 8 PM (e.g. right after a manual frenzy ended during the 8 PM hour). Now checks once at 8 PM and waits 24h if prerequisites aren't met.
- Fishing Frenzy had no cooldown between casts — the 10-second frenzy cooldown was immediately bypassed on the next `/fish`. Now properly enforces the 10s cooldown during frenzy.

## [0.2.3] - 2026-02-24

### Added
- 395 new region-specific fish species across all 3 regions (NA, Asia, Europe) and all 9 location types (~15 per location per region)
- New species include salamanders, frogs, turtles, crabs, shrimp, and other aquatic creatures alongside traditional fish
- Notable catches: Hellbender, Japanese Giant Salamander, Olm, Whale Shark, Greenland Shark, Basking Shark, Beluga Sturgeon, and more
- Realistic sizes and weights for all new species
- Adds 'Fishing Frenzy' Event at 8 PM Guild time + Small chance of randomly triggering during /fish.
    - During this event, all cooldowns are reduced to 10 seconds for 5 minutes.
    - Fishing Tickets are not consumed during Fishing Frenzy.
- Fish codes now displayed in chest outputs

### Fixes
- Fix bug where buying keys doesn't show purchase currency.

## [0.2.2] - 2026-02-23

### Added
- Lucky Charm now applies its +2% rarity bonus per level when fishing
- Lucky Charm level shown in `/gear` display when purchased
- Voting now enabled, use `/vote` for more info.
- `/net collect` now shows fish IDs for each fish.
- Leaderboards now show the fish codes for fish-related leaderboards.
- Adds Most valuable Fish leaderboard.

### Changed
- Seasonal Bait rework: 50% chance to catch the current season's exclusive species (e.g., Frostbite Flounder), otherwise catch a normal fish with 2x trait chance as consolation

### Fixes
- Tank and Lucky Charm upgrade levels now persist correctly across sessions
- Shop upgrade display now shows correct current level instead of always "level 1"
- `/buy upgrade tank_slot 5` now properly rejects quantity > 1 for upgrades
- `/gear` cooldown display now includes active effects and guild buffs (previously showed rod + gear only)
- Updates 'First Vote' Achievement to give 5 energy drinks and 5 fishing brochures.

## [0.2.1] - 2026-02-21

### Added
- Notification Toggles - See `/notifications` for more information.
- Fishing Nets - Passively catch fish over time. See `/shop` nets tab for more information.(Requires Level 10)
- Server Buffs - Buffs that can be purchased for a server. See `/shop` server buffs tab for more information.
- Net Full DM Notification - Get notified when your fishing net is full. Toggle via `/notifications`.

### Fixes
- Fix for selling fish from tank


## [0.2.0] - 2026-02-19

### Added
- **Chest system** — Loot chests with weighted rarity tables (Common → Legendary); daily key limits; seasonal chest support
- **Redeem codes** — Promotional codes granting coins, pearls, XP, items, and titles; managed via `!fcreatecode` / `!fdeactivatecode`
- **Title system** — Achievement titles with rarity tiers; `/title list`, `/title equip`, `/title unequip`; Early Supporter legendary title for beta redeemers
- **GameDataService** — Centralised in-memory cache for all game content (titles, fish, items, chests, consumables); hot-reloadable via `!freload_game_data`
- **Voting system** — `/vote` command with streak tracking and ticket rewards
- **Leaderboards** — `/leaderboard` with fish count, coins, and level rankings
- **Consumables** — XP boosts, energy drinks, rabbit's feet, schnapps, fishing tickets
- **Version command** — `/version` shows current bot version and changelog highlights
- **Guild settings** — Per-guild custom prefix support; admin commands for configuration
- **Developer tools** — `!fgivechest`, `!fgivekey`, `!fgiveconsumable`, `!fdebuguser`, `!fsqlquery`, `!freload_game_data`, `!fcreate_code`

### Changed
- XP system rebalanced — higher base XP with rarity multipliers for more rewarding catches
- Shop updated to support pearl-only items; seasonal bait chest-only (not purchasable)
- Pearl Rod is pearl-currency only
- Chest loot tables tuned — reduced consumable drop rates; currency only via bags/purses
- Command syncing improved — dev guilds sync instantly on startup; global commands cleared in dev mode

### Fixed
- `AttributeError` on `Rod` missing `currency` attribute
- `AttributeError` on `Bait` missing `shop_available` attribute
- Bot startup failure when `EventsCog` had missing attribute
- Database authentication errors resolved with proper async connection pooling
- Duplicate `/equip title` commands — `/title equip` (titles) and `/equip` (gear) are now clearly separate

## [0.1.0] - 2025-01-15

### Added
- Initial release of CozyCasting Discord bot
- Core fishing mechanics with cast and catch system
- Fish model with 7 rarity tiers (Common to Unique)
- Fish traits system (Albino, Golden, Giant, etc.)
- Visual patterns (Solid, Spotted, Striped, etc.)
- Size and weight variance for each catch
- Personal aquarium/tank for displaying fish
- Basic progression system with XP and levels
- Economy system with coin rewards
- Equipment system (rods and bait)
- Shop for purchasing equipment
- Multiple fishing locations across regions
- Location-based fish availability
- Level-gated content progression
- Hybrid commands (slash + prefix support)
- SQLAlchemy async database layer
- Docker support for deployment
- Comprehensive test suite

### Technical
- discord.py 2.4+ with hybrid commands
- SQLAlchemy 2.0+ async ORM
- PostgreSQL (production) / SQLite (development)
- Pydantic configuration management
- pytest-asyncio test framework

[Unreleased]: https://github.com/youruser/cozycasting/compare/v0.2.0...HEAD
[0.2.0]: https://github.com/youruser/cozycasting/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/youruser/cozycasting/releases/tag/v0.1.0
