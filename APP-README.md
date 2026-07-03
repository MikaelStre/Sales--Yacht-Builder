# Baltic Yachts · Yacht Builder — full app

Self-contained static web app for the build lifecycle: **Sales**, **Projects**, **Engineering**.
Every page is one HTML file with inline CSS/JS and **no external dependencies** — open it in a browser,
host it anywhere static, edit it directly in the GitHub web editor.

## Areas
- `sales/` — create projects, ongoing pipeline, pricing, specification.
- `projects/` — realized projects: specification, change orders, planning, price calculation, **Procurement & Still-to-Buy**.
- `engineering/` — disciplines, project solutions, risks, calculation suite.

## Procurement / Still-to-Buy (the new work — all built in)
- `projects/procurement.html` — per-project Procurement landing: material-position stats, tools, outstanding long-lead items.
- `projects/still-to-buy.html` — full-screen wrapper that opens the tool for the selected hull.
- `projects/still-to-buy-tool.html` — the tool: BOM (+add/remove), still-to-buy list (purchasing-gated edit), Change Orders
  (read-only from the PM), Analyze & Forecast (contingency + S-curve, both shown), Trends, Priority items, Findings,
  Snapshots, allowance draw-down, month-compare, full-page report.
- Every project page has a **Still to buy** item in the sidebar.

Per-project data is browser `localStorage`, keyed by hull: `pw_stb_<HULL>`, `pw_cos_<HULL>` (change orders,
read-only in the tool), `pw_projinfo_<HULL>`, `pw_user` / `pw_role`.

## Preview
- Open any `.html` in a browser, or serve the folder: `python -m http.server` → `http://localhost:8000/projects/`.
- Or enable **GitHub Pages** (Settings → Pages → deploy from `main`, root) to view the whole app from anywhere.

## Try the Still-to-Buy flow
`projects/procurement.html?p=B121-01` → **Still to Buy** tile → in the tool, switch **Acting as → Purchasing team**
to edit the list; the **Change Orders** tab shows the PM's COs read-only.

## Note
The `engineering/` pages are the current build; a few reference internal assets that may show placeholders
outside the Baltic network. The Sales and Projects areas are fully self-contained.
