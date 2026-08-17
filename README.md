# CyTECH Universal

A fully customizable shop management app — one file, works offline, syncs to your own Supabase cloud.

Built on the CyTECH Electronics app but opened up: you can make it your own business tool.

## What you can customize (no coding)

- **Branding** — your shop name, address, phone, currency, browser tab title, sidebar logo (PNG upload), tab icon (PNG upload)
- **Appearance** — light / dark / blue modes plus a full color picker (accent, background, cards, text, borders, income/expense colors)
- **Modules** — rename the built-in Repairs / Purchases / Sells, change their icon and color, pick which fields appear on the form, and add brand-new modules (e.g. "Buys") from a template. Every module gets its own records, printing, dashboard section and calendar entries
- **Cloud** — bring your own free Supabase project (URL + anon key in a one-time setup screen)

## Built-in modules

| Module | Template | Type |
| --- | --- | --- |
| Repair Jobs | Repair (status pipeline, deposit, final payment, parts cost, signatures) | Income |
| Purchases | Purchase (seller, items with prices, add-to-stock) | Expense |
| Sells | Sale (items with price and cost, stock linking) | Income |
| Stock | In/out tracking with values | — |
| Calendar / People / Dashboard | Profit per day, customer history, live totals | — |

## First-time setup (your own Supabase)

1. Sign up free at [supabase.com](https://supabase.com) and create a project.
2. Project Settings → API → copy the **Project URL** and the **anon / publishable key**.
3. Open the app → the setup screen appears → paste both → **Save & continue**.
4. In the Supabase SQL Editor, run the contents of [`supabase.sql`](supabase.sql) once (creates the sync table with row-level security).
5. Optional: deploy the `delete-account` Edge Function (`supabase/functions/delete-account`) so users can delete their cloud account.

The cloud is optional — the app works fully offline. Connect later from Settings.

## Deploy

Static hosting works (GitHub Pages, Netlify, Vercel, etc.). Just publish the repository contents. The app is a PWA — it can be installed and the included workflow can build an APK.

## License

Proprietary. This software is sold, not shared. No redistribution, resale or public fork of this repository is permitted without written permission from the author.