# Company repo catalog

Generated 2026-08-12T12:07:20 by scan-repos.ps1. Mechanical excerpts only.

## bua-product
- url: https://github.com/DaveQin2023/bua-product.git
- (no README.md)

## bua-rules
- url: https://github.com/DaveQin2023/bua-rules.git
- README excerpt:
  ```
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
  ```

## bua-database
- url: https://github.com/DaveQin2023/bua-database.git
- README excerpt:
  ```
  # Annuity Marketplace Database
  
  Schema definitions and data dictionary for the Annuity Marketplace platform.
  **No application code lives here** — only DDL, migrations, and the data
  dictionary that the UI and rules repos rely on.
  
  ## What lives here
  
  - `schema/products.sql` — the `products` table backing the marketplace catalog
  - `docs/data-dictionary.md` — every column, its meaning, and which repo consumes it
  
  ## Change policy
  
  Schema changes require a migration script and a data-dictionary update in the
  same pull request.
  ```

