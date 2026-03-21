# CRAFT_LOG 🃏

> A community-powered Sorare card craft tracker — built to help managers make smarter crafting decisions through shared data.

---

## What it does

CRAFT_LOG lets you log every card craft you do on Sorare, track the market value at the time of crafting, and compare your results against the community average. The more people use it, the more accurate the analytics become.

---

## Features

- 🔐 **User accounts** — each manager has their own craft history
- 📊 **Per-scarcity analytics** — Limited, Rare and Super Rare are tracked completely separately
- 💎 **Draw type tracking** — Standard and Special draws logged independently
- 🧪 **Essence cost calculator** — automatically calculates essence cost based on clues used
- 📈 **EV per 1,000 essence** — the key efficiency metric for evaluating craft value
- 🌍 **Global vs personal stats** — see community-wide averages alongside your own results
- 🔗 **Sorare API integration** — fetch live market prices directly from Sorare
- 📱 **Mobile friendly** — works on phone and desktop

---

## How to use

1. Open the app and create an account
2. Select your draw type and scarcity
3. Enter the player name and use **⟳** to fetch the current market value from Sorare
4. Select your clues to calculate the essence cost
5. Hit **+ Add Craft** to save

---

## Market Value Formula

The market value is calculated using the average of the last 5 IN_SEASON manager-to-manager sales — excluding auctions and direct buy-now prices which would inflate the real market value.

```
Market Value = Average of last 5 IN_SEASON sales
```

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla HTML / CSS / JavaScript |
| Database | Supabase (PostgreSQL) |
| Auth | Supabase Auth |
| API Proxy | Supabase Edge Functions (Deno) |
| Card Pricing | Sorare GraphQL API |
| Hosting | GitHub Pages |

---

## Disclaimer

CRAFT_LOG is not affiliated with, endorsed by, or officially connected to Sorare. All card data and pricing is fetched from the public Sorare API. Use at your own discretion.

---

## Contributing

Use the app and log your crafts — every entry makes the community analytics more accurate. 🙌

If you find a bug or have a feature request, open an issue.
