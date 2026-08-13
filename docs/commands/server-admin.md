# Server Admin Commands

Commands for configuring CozyCasting in your server. All `/settings` subcommands require the **Manage Server** permission.

---

## /settings view

Show all current server settings at a glance.

- **Usage:** `/settings view`

Displays your prefix, response visibility, chest drop channel, rare catch announcement channel, leaderboard results channel, notification roles, and server timezone.

---

## Prefix

### /settings prefix

Set a custom command prefix for your server.

- **Usage:** `/settings prefix <new_prefix>`
- **Example:** `/settings prefix !c`

Changes the prefix used for text-style commands (e.g. `!c fish`). The default is `!f`. Must be 1–10 characters. Slash commands always work regardless of prefix.

### /settings prefix-reset

Revert to the default prefix (`!f`).

- **Usage:** `/settings prefix-reset`

---

## Response Visibility

### /settings ephemeral

Toggle whether a command's response is visible only to the user who ran it (ephemeral) or to the whole channel.

- **Usage:** `/settings ephemeral <command> <true|false>`
- **Commands:** `leaderboard`, `profile`, `inventory`
- **Example:** `/settings ephemeral leaderboard true`

Useful for keeping the channel clean in busy servers. `/locations` is always ephemeral.

Note: This only applies to slash commands. Text based actions such as `!fish` will always be visible to the whole channel due to Discord limitations.

---

## Community Chest Drops

Random chest drops periodically appear in a designated channel for anyone to claim.

### /settings channel

Set which channel receives community chest drops.

- **Usage:** `/settings channel <#channel>`
- **Example:** `/settings channel #fishing`

### /settings channel-reset

Disable community chest drops.

- **Usage:** `/settings channel-reset`

---

## Rare Catch Announcements

Automatically announce every **Mythical** or **Unique** catch, with the fish, who caught it, and an optional role ping.

### /settings rarecatch

Set (or clear) where rare catches are announced.

- **Usage:** `/settings rarecatch [channel] [role]`
- **Examples:** `/settings rarecatch #big-catches`, `/settings rarecatch #big-catches @RareCatchFans`

`channel` accepts a regular text channel **or a thread** — including an archived one, which the announcement will automatically un-archive. Leave `channel` empty to turn announcements back off.

---

## Leaderboard Results

Post completed **Weekly Fishing Champion**, **Monthly Fishing Champion** and **Top Server of the Month** results in a channel of your choice. Opt-in — off unless you set it.

### /settings leaderboard-results

Set (or clear) where completed leaderboard results are announced.

- **Usage:** `/settings leaderboard-results [channel]`
- **Example:** `/settings leaderboard-results #announcements`

Results post once per period, right after the winners are decided at midnight UTC. Leave `channel` empty to turn it back off. Announcements are best-effort: rewards are always granted regardless of whether the message gets through.

The leaderboards are bot-wide, not per-server — every server that opts in sees the same global champion.

---

## Notification Roles

Roles that get pinged when events fire. Generally best to have a way for userse to self-assign these roles. 

### /settings notify-events

Set the role to ping when server events start — including **Fishing Frenzy** and **Monster Fish** spawns.

- **Usage:** `/settings notify-events <@role>`
- **Example:** `/settings notify-events @Events`

### /settings notify-events-reset

Disable event pings.

- **Usage:** `/settings notify-events-reset`

### /settings notify-chest

Set the role to ping when a community chest drop appears.

- **Usage:** `/settings notify-chest <@role>`
- **Example:** `/settings notify-chest @ChestAlerts`

### /settings notify-chest-reset

Disable community chest drop pings.

- **Usage:** `/settings notify-chest-reset`

---

## Server Timezone

### /settings timezone

Set the server timezone. This controls when the **8 PM Fishing Frenzy** scheduled trigger fires relative to your community's local time.

- **Usage:** `/settings timezone <IANA timezone>`
- **Examples:** `/settings timezone America/New_York`, `/settings timezone Europe/London`, `/settings timezone UTC`

Uses standard [IANA timezone names](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones). Defaults to `UTC` if not set.

---

## Permissions and Troubleshooting

CozyCasting **never requires Administrator**.

**Required everywhere:** View Channels, Send Messages, Embed Links, Attach Files, and Use Application Commands (the `applications.commands` scope, granted when the bot is installed). Attach Files is what renders fish images and profile cards — without it, catches come through as text.

**Feature-specific:** Create Public Threads, Send Messages in Threads and Read Message History, needed only for accepted `/trade` sessions, which run in their own thread.

### One channel doesn't work but the rest do

Discord permissions are **effective per channel**. A channel override can deny a permission the CozyCasting role grants server-wide, which is almost always the cause when a single channel goes quiet.

1. **Server Settings → Roles → CozyCasting** — confirm the required permissions above are granted at the role level.
2. **Right-click the channel → Edit Channel → Permissions** — check for a red ✗ on the CozyCasting role or on `@everyone` for that channel.
3. Category overrides cascade to new channels inside them; check the category too.
4. Removing and re-adding the bot is not necessary — role and channel overrides can be fixed in place.

!!! info "Permission checks"
    `/settings channel`, `/settings rarecatch` and `/settings leaderboard-results` all check that the bot can actually post in the channel (or thread) you pick — send messages, embed links, and attach files — before saving it. If something's missing, you'll get told exactly which permission to grant instead of a setup that silently never announces anything.

### Members aren't getting reminders

Reminders are DMs, and DMs are opt-in per player. CozyCasting does not accept gameplay commands in DMs — they only carry cooldown/daily/vote/net-full/come-back reminders, trade requests, breeding alerts, and guild invitations (which fall back to the channel). Players enable them with **right-click the server → Privacy Settings → Direct Messages**, then tune which types they get with `/notifications`.

## Recommended Setup

A typical server admin setup looks like this:

1. **Check permissions first** — confirm CozyCasting has View Channels, Send Messages, Embed Links and Attach Files in the channel you plan to use. See [Permissions and Troubleshooting](#permissions-and-troubleshooting) above; everything below silently does nothing without them.
2. **`/settings channel #fishing`** — designate your fishing channel for chest drops
3. **`/settings rarecatch #fishing`** — announce Mythical+ catches in the same channel, or pick a quieter one
4. **`/settings leaderboard-results #announcements`** — post the weekly and monthly champions where people will see them
5. **`/settings notify-events @Events`** — create an opt-in role and assign it here
6. **`/settings notify-chest @Events`** — use the same role or a separate one for chests
7. **`/settings timezone America/New_York`** — set your community's timezone
8. **`/settings prefix !f`** — leave as default or pick your own

Run **`/settings view`** afterwards to confirm everything landed.

Members who want event pings can self-assign the role via your server's role menu. Reminders (cooldown, daily, vote, net-full) reach players by DM and are opt-in per player — see [Members aren't getting reminders](#members-arent-getting-reminders) if someone says they get nothing.
