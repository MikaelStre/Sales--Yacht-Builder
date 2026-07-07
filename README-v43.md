# Baltic Yachts Workspace — v43 (Projects → Yacht Life)

This package **adds the Yacht Life addition to the Projects area** of the v42 workspace.
It is a precise **overlay**: apply these two files onto your existing **workbench-v42** to
produce **v43**. Every other page — engineering, procurement, sales, and all the existing
**projects** tools — is left exactly as it was.

## What changed
1. **`index.html`** (hub landing) — the **Projects** tile now opens the new Projects landing
   (`projects/landing.html`) and its blurb mentions Yacht Life. Nothing else on the hub changed.
2. **`projects/landing.html`** (NEW) — the new **Projects landing**: choose **Projects in Build**
   or **Yacht Life**.
   - **Projects in Build** → opens your existing `projects/index.html` (the current spec /
     change-orders / planning hub) — unchanged.
   - **Yacht Life** → the delivered-fleet app: Warranty, After Sale, Service Team, Communication
     (two-way tickets), Request a Quote, Manual & Docs; plus the Baltic-only **Service Desk**
     (fleet summary, SLA, analyze, fleet schedule) and **Tools** (Worklist → linked Board & Gantt,
     Planning, Offers & RFQs).
   - **← Workspace** (top-right) returns to the hub.

## How to apply (produces v43)
Copy into your **workbench-v42** folder, overwriting only the hub index:
```
workbench-v42/index.html                ← replace with this index.html
workbench-v42/projects/landing.html     ← add this new file
```
Then re-zip / re-upload as **workbench-v43**. Do not delete or change any other file.

## Notes
- **Demo version.** The Yacht Life data (fleet, tickets, warranty, worklist, plans) is sample
  data held in the browser (localStorage) so the demo is fully clickable offline. In the next
  phase this binds to the **SharePoint structure** per the scoping document
  (`Yacht-Life-Hub-Integration-Scoping.docx`).
- **Styling** matches v42 (ocean-blue `#0e5a8a`, slate ink, Calibri, 16px radius, v42 logo).
- The single-yacht owner share link is `projects/landing.html#yacht=<id>` (owner mode hides the
  Baltic-only nav). In production this becomes a permission-scoped page.
