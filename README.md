# CRAFT_LOG 🃏

> A community-powered Sorare card craft tracker with built-in Craft Helper — built to help managers make smarter crafting decisions through shared data.

---

## What it does

CRAFT_LOG lets you log every card craft you do on Sorare, automatically fetch live market prices, and compare your results against the community average. The more people use it, the more accurate the analytics become.

---

## Features

### Craft Tracker
- 🔐 **User accounts** — each manager has their own private craft history
- 🔍 **Live player search** — autocomplete with player image, team and price as you type
- 💰 **Automatic market value** — fetches floor price and average of last 3 sales from Sorare
- 📊 **Per-scarcity analytics** — Limited, Rare and Super Rare tracked completely separately
- 💎 **Draw type tracking** — Standard and Special draws logged independently
- 🧪 **Essence cost calculator** — automatically calculates essence cost based on clues used
- 📈 **EV per 1,000 essence** — key efficiency metric for evaluating craft value
- 🌍 **Global vs personal stats** — community-wide averages alongside your own results
- 📱 **Mobile friendly** — works on phone and desktop

### Craft Helper
- 🎯 **10-card craft simulator** — see pool stats for each of your 10 craft cards
- 🔢 **Tier probabilities** — STAR/T1–T5 breakdown with player counts per tier
- 🏆 **Top 3 players** — highest value players per card with photo and price
- 🔎 **Per-card filters** — filter each card independently by league and nationality
- 💶 **Price overview** — Highest, Average and Lowest price per card

---

## How to use

### Craft Tracker
1. Open the app and create an account
2. Select your draw type (Standard / Special) and scarcity (Limited / Rare / Super Rare)
3. Start typing a player name — autocomplete suggestions appear instantly
4. Select the player — market value is filled automatically
5. Select your clues to calculate the essence cost
6. Hit **+ Add Craft** to save

### Craft Helper
1. Click the **🎯 Craft Helper** tab
2. Select rarity and draw type
3. Choose 5 or 10 cards
4. Filter each card by league or nationality
5. Use the pool stats and Top 3 players to decide which card is the best pick

---

## Market Value Formula

```
Market Value = (Floor Price × 65%) + (Avg last 3 sales × 35%)
```

Floor Price and sales data are fetched daily from the Sorare marketplace.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla HTML / CSS / JavaScript |
| Database | Supabase (PostgreSQL) |
| Auth | Supabase Auth |
| API Proxy | Supabase Edge Functions (Deno) |
| Pool Cache | Supabase Edge Functions + pool_cache table |
| Card Pricing | Sorare GraphQL API |
| Hosting | GitHub Pages |

---

## Data Updates

Pool data (player list, prices, tiers) is refreshed daily via the `update-pool` Edge Function. The data is cached in Supabase so the app stays fast and independent.

---

## Disclaimer

CRAFT_LOG is not affiliated with, endorsed by, or officially connected to Sorare. All card data and pricing is fetched from publicly available sources. Use at your own discretion.

---

## Contributing

Use the app and log your crafts — every entry makes the community analytics more accurate. 🙌

If you find a bug or have a feature request, open an issue.
