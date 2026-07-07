# workbench-v43 — changes vs v42

Complete workspace with the **Yacht Life** addition and the new **Project Follow-up / Project Reporting**.

## Changed / added
- **index.html** (hub) — Projects tile opens `projects/landing.html`. (only line changed on the hub)
- **projects/landing.html** (NEW) — Projects landing: **Projects in Build** (opens existing `projects/index.html`) or **Yacht Life**.
- **projects/project-follow-up.html** (NEW) — **Project Reporting**: the monthly project-reporting sheet (Contract / Hours / Procurement / PnL: Business approval vs Current forecast) rebuilt from `B121-01 Project reporting.xlsx`. The PM fills the highlighted cells each month and **Saves the month** → monthly history; includes an **Analyze** tool (profit-% trend, forecast-profit trend, hours-over-time, business-vs-forecast). Contract sales price + budgeted production/engineering hours are flagged **“from sales.”**
- **projects/*.html nav** — a **Project Follow-up** tab added after *Price calculation* on every project page (nav link only).
- **Yacht Life app** — on the **Service Desk** matching items and the yacht ticket/warranty/RFQ lists, a **👁 View** button opens a **read-only** look at the ticket / warranty / service info (easy at-a-glance), with **Open full** to edit.

## Untouched v42 content
engineering/, sales/, all existing projects tools (page bodies unchanged; only the nav gained one tab).

## Project-tile landings (2026-07-07)
- **procurement/index.html** — now a **project-tiles landing** (Yacht-Life style) for in-build projects; each tile opens `still-to-buy.html?p=HULL` (and Project Material). This REPLACES the old placeholder — only `procurement/project-material.html` remains a placeholder.
- **sales/ongoing.html** &amp; **sales/resting.html** — rebuilt as **project tiles** (ongoing / resting sales projects); each tile opens `pricing.html?p=HULL` / `specification.html?p=HULL`.

## One placeholder to swap
`procurement/index.html` + `procurement/project-material.html` are regenerated placeholders (small SharePoint files returned no content in this environment). Replace with your v42 originals; everything else is real.

## Demo note
Yacht Life and Project Reporting data are held in the browser (localStorage) for the demo; they bind to the SharePoint structure next. Styling kept as v42.
