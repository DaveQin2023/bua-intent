# Data Dictionary — Annuity Marketplace

| Table.Column | Meaning | Consumed by |
|---|---|---|
| products.product_id | Stable catalog key, kebab-case | UI repo (`products.js`), rules repo (rate-bands) |
| products.rate_pct | Current declared rate, percent | UI product cards, promo banners |
| products.term_years | Surrender period in years | UI term filter; rules `checkLiquidityHorizon` |
| products.min_premium | Minimum single premium, USD | UI cards; rules `checkPremiumToNetWorth` |
| products.states_blocked | CSV of state codes lacking approval | rules `checkStateAvailability` |
| products.am_best_rating | Carrier AM Best rating | UI cards (trust signal) |

Rule of thumb for the UI team: anything shown on a product card originates in
`products` and must not be hardcoded in the UI repo.
