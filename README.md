# Baltic Yachts · Yacht Builder — workbench-v42 (complete)

The full app in one folder. Static HTML, no external dependencies — open a file, host it anywhere,
edit any page in the GitHub web editor.

## Structure
```
index.html        First landing page (hub). Engineering / Sales / Projects / Procurement (now live) + coming-soon tiles.
engineering/      v38 (unchanged)
sales/            v40
projects/         v40 (unchanged — Procurement is its own area, not under Projects)
procurement/      NEW top-level area (this round)
```

## What's new in v42
- **Procurement is a live top-level area.** On the hub, the Procurement tile was flipped from
  *Coming soon* to live → `procurement/`. Everything else on the hub is the v38 hub, unchanged.
- **`procurement/`** — the Procurement landing (`index.html`: project picker + material-position stats +
  Still-to-Buy tile + outstanding long-lead items) → **Still to Buy** tool (`still-to-buy.html` wrapper +
  `still-to-buy-tool.html`). Change orders read **read-only** from the PM's register (`pw_cos_<HULL>`,
  maintained on `projects/change-orders.html`); the budget uses an agreed material figure on the tool's
  Setup tab; the list is purchasing-gated.
- **One fix:** `engineering/disciplines/index.html` had a pre-existing broken link `suite/` (404); repointed
  to `../suite/` (the Calculation Suite page). Revert if you prefer it untouched.

## Composition
- Hub + Engineering = **v38** (your reference "good" version).
- Sales + Projects = **v40** (your latest).
- Procurement = **v41 work**, placed as a top-level area.

## Preview / deploy
- Open `index.html`, or serve the folder (`python -m http.server`), or enable GitHub Pages.
- Azure: upload changed areas. New/changed here vs your live site: `index.html` (hub, one tile) and
  `procurement/` (new). Sales/Projects/Engineering match v38/v40.

## Per-hull data (browser localStorage)
`pw_stb_<HULL>` · `pw_cos_<HULL>` · `pw_projinfo_<HULL>` · `pw_user` / `pw_role`.
