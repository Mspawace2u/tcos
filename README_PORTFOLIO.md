# Portfolio Pack — Host Instructions

This folder contains a **single-file HTML page** plus supporting artifacts.

## Files
- `index.html` — the portfolio page (host this)
- `PRD.md` — sanitized product requirements doc
- `ORCHESTRATION.md` — orchestration explanation + skill file
- `persona.core.yaml` — the skill file used to drive intake/orchestration
- `ARCHITECTURE.md` — architecture explanation
- `map.json` — machine-readable schematic map
- `schematic_viewer.html` — standalone diagram viewer
- `QUALITY.md` — degradation guardrails (first pass)

## Fastest hosting options
### Option A — GitHub Pages (no build)
1. Create a new repo
2. Upload these files to the repo root
3. Settings → Pages → Deploy from branch → `main` / root
4. Your page will be at: `https://<user>.github.io/<repo>/`

### Option B — Cloudflare Pages
1. Create a Pages project from the repo
2. Framework preset: “None”
3. Build command: (leave blank)
4. Output directory: `/`

### Option C — Drag-and-drop
Netlify / Vercel static: upload the folder, deploy.

## Notes
- The diagram in `index.html` uses an iframe `srcdoc` so it stays single-file.
- If a platform strips `srcdoc`, host `schematic_viewer.html` and point the iframe to it.
