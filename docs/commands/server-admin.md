# Server Admin Commands

Commands for configuring CozyCasting in your server. All `/settings` subcommands require the **Manage Server** permission.

---

## /settings view

Show all current server settings at a glance.

- **Usage:** `/settings view`

Displays your prefix, response visibility, chest drop channel, notification roles, and server timezone.

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

## Recommended Setup

A typical server admin setup looks like this:

1. **`/settings channel #fishing`** — designate your fishing channel for chest drops
2. **`/settings notify-events @Events`** — create an opt-in role and assign it here
3. **`/settings notify-chest @Events`** — use the same role or a separate one for chests
4. **`/settings timezone America/New_York`** — set your community's timezone
5. **`/settings prefix !f`** — leave as default or pick your own

Members who want event pings can self-assign the role via your server's role menu.
