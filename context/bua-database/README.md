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
