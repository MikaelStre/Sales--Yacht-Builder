# Baltic Yachts · Yacht Builder — workbench-v42 (complete)

The full app in one folder. Static HTML, no external dependencies — open a file, host it anywhere,
edit any page in the GitHub web editor.

## Structure
```
index.html        First landing page (hub). Engineering / Sales / Projects / Procurement (live) + coming-soon tiles.
engineering/      v38 (unchanged)
sales/            v40
projects/         v40 (unchanged)
procurement/      Procurement area (this round):
    index.html            Procurement hub — Project Material (live) + Suppliers/Top-Priority/Findings/Standard-Inventory (planned)
    project-material.html Project Material — material KPIs, the Still-to-Buy tile, projects table, outstanding long-lead items
    still-to-buy.html     the Still-to-Buy tool (per-project, ?p=HULL)
```

## The Procurement flow
Main hub → **Procurement** tile → **Procurement hub** (`procurement/index.html`) → **Project Material** tile
→ **Project Material** (`project-material.html`) → **Still to Buy** → the tool. Breadcrumbs walk back up the
chain; the whole area is the dark design we agreed on. No iframe — the tool opens as its own page.

## The Still-to-Buy tool
BOM (+add/remove) · still-to-buy list (purchasing-gated edit) · Change Orders (read-only, from the PM's
`pw_cos_<HULL>` register on `projects/change-orders.html`) · Analyze & Forecast (contingency + S-curve) ·
Trends · Priority items · Findings · Snapshots · allowance draw-down · month-compare · full-page report.
Per-hull data in `localStorage`: `pw_stb_<HULL>` · `pw_cos_<HULL>` · `pw_projinfo_<HULL>` · `pw_user` / `pw_role`.

## Composition
- Hub + Engineering = **v38** (your reference "good" version). Sales + Projects = **v40**.
- Procurement = the landing pages we designed (`Procurement.html` → hub, `Project_Material.html` → Project
  Material) + the Still-to-Buy tool, wired together as a top-level area.

## Preview / deploy
- Open `index.html`, or serve the folder (`python -m http.server`), or enable GitHub Pages.
- Vs your live site, the only new/changed pieces are the hub's one Procurement tile (now live) and the new
  `procurement/` folder. Sales / Projects / Engineering match v38/v40.
