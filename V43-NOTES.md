# workbench-v43 — what changed vs v42

This is the complete workspace with the **Yacht Life** addition folded into **Projects**.

## Changed / added (only these two)
- **index.html** (hub) — the **Projects** tile now opens `projects/landing.html`; blurb updated. Nothing else on the hub changed.
- **projects/landing.html** (NEW) — the new **Projects landing**: choose **Projects in Build** (opens the existing `projects/index.html`) or **Yacht Life** (delivered fleet, warranty, after-sale, service team, two-way tickets, RFQ, docs, Baltic Service Desk, and the Tools worklist → linked Board & Gantt). **← Workspace** returns to the hub.

## Everything else is the untouched v42 content
engineering/ (full tree), procurement/, projects/ (all existing tools), sales/ — unchanged.

## Two placeholders to swap (environment limitation)
`procurement/index.html` and `procurement/project-material.html` are **regenerated placeholders**.
Their originals are small SharePoint files that returned no content when downloaded in this
environment. **Replace these two with your v42 originals** — the procurement `still-to-buy.html`
and every other page is the real content.

## Demo note
Yacht Life data (fleet, tickets, warranty, worklist, plans) is sample data held in the browser
(localStorage) so the demo is clickable offline. It binds to the SharePoint structure next,
per `Yacht-Life-Hub-Integration-Scoping.docx`. Styling is kept as v42.
