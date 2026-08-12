# Annuity Business Rules

Business function / rule engine for the Annuity Marketplace. This repository is
the single source of truth for **eligibility, suitability, and rate-banding
rules** applied before any annuity product can be offered to a customer.

## What lives here

- `src/rules/eligibility.js` — age and state-availability checks per product type
- `src/rules/suitability.js` — premium-to-net-worth and liquidity suitability checks (NAIC model rule)

## Consumers

The UI repo (`bua-product`) calls these rules through the quote service; rules
are never duplicated in the UI layer.
