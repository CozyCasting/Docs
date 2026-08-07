# Trading Commands

Send items to other players or open an interactive trade session.

## /give

Send one item (or currency) directly to another player — no acceptance required.

- **Usage:** `/give <target> <item> [quantity]`
- **Cooldown:** 60 seconds

| Parameter | Required | Description |
|-----------|----------|-------------|
| `target` | Yes | The Discord member you're sending to |
| `item` | Yes | What to send — see [Item Input](#item-input) below |
| `quantity` | No | How many to send (stackable items only, defaults to 1) |

After you run the command, a private confirmation embed shows what you're about to send. Click **Confirm** to complete the transfer or **Cancel** to abort. This cannot be undone.

**Examples:**

```
/give @Alice 500 coins
/give @Alice 2 energy drinks
/give @Alice ABC123DE
/give @Alice common chest 3
```

---

## /trade

Open a two-way interactive trade session with another player.

- **Usage:** `/trade <target>`
- **Cooldown:** 60 seconds

### How a trade works

1. **Invite** — You run `/trade @Bob`. An invite embed appears in chat and pings Bob.
2. **Accept** — Bob clicks **Accept**. A private trade thread opens off the invite message.
3. **Add items** — Both players type items into the thread (see [Item Input](#item-input)). The embed in the main channel updates in real time to show each side's offer.
4. **Remove items** — Type `remove <item>` in the thread, or `remove <fish code>` for a specific fish.
5. **Accept** — Each player clicks **Accept** on the trade embed when satisfied. The status shows who has accepted: *Alice ✅ — Bob ⏳*.
6. **Complete** — Once both players have accepted, the trade executes immediately.

!!! warning "Bait-and-switch protection"
    If either player adds or removes an item **after** the other has already accepted, both acceptances reset. You'll both need to re-accept the updated offer.

!!! info "Timeouts"
    The invite expires after **2 minutes** if not accepted. An open trade session expires after **5 minutes** of inactivity. All items stay with their original owners on timeout.

---

## Item Input

Both `/give` and the trade thread accept the same item formats:

| Format | Example | What it does |
|--------|---------|--------------|
| `<amount> coins` | `500 coins` | Offer coins |
| `<amount> pearls` | `50 pearls` | Offer pearls |
| `<amount> voting tickets` | `3 voting tickets` | Offer vote tickets |
| Fish short code | `ABC123DE` | Offer a specific fish from your tank |
| Gear short code | `a1b2c3` | Offer a specific gear item |
| Item name | `2 energy drinks` | Offer consumable(s) from your inventory |
| Item name | `common chest 3` | Offer chests from your inventory |

Fish codes are the 8-character codes shown on each fish (e.g. from `/fishinfo`). Gear codes are the 6-character codes shown in `/inventory`.

Item names support fuzzy matching, so `energy drink`, `energy drinks`, and `energy` all work.

---

## What Can Be Traded

**Tradeable:**

- Coins, Pearls, Vote Tickets
- Fish (from your tank, not in an active breeding session)
- Gear items
- Rods, bait
- Most consumables (XP boosts, rarity boosts, sell boosts, magnets, etc.)
- Chests (common, rare, epic, legendary, seasonal)

**Not tradeable:**

- Title Pouch
- Fishing Pass
- Fishing Journal
- Shopping Card
- Twin Hook Token
- Fish currently in an active breeding session

---

## Limits

- Up to **10 items per side** in a single `/trade` session (currencies do not count toward this limit)
- Both players must have an account (must have fished at least once)
- You can only be in one active trade at a time
- You cannot trade with bots or with yourself
