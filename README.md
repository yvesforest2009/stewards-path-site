
# Steward’s Path Tax & Accounting – Static Deploy on Vercel

This project is a **static website** (plain HTML/CSS/JS). No build step is required.

## Quick Deploy (Vercel Web UI)

1. Go to **vercel.com** → **New Project** → **Import** → **Drag & drop** your project folder **(as a ZIP or folder)**.
2. **Framework Preset:** `Other`
3. **Root Directory:** `/` (unless your `index.html` is inside a subfolder like `/site`—then choose that).
4. **Build & Output Settings:**
   - **Build Command:** *(leave blank)*
   - **Output Directory:** *(leave blank)* (for plain static sites)
5. Click **Deploy**.

> If you're using client‑side routing (SPA), you can enable the `rewrites` in `vercel.json` so every route serves `index.html`.

## Files to include

Your project should include at minimum:
- `index.html` (home page)
- `favicon.ico` (optional)
- `/assets/` (your CSS, JS, images, etc.)
- `vercel.json` (this file configures caching and clean URLs)

## Common Issues & Fixes

### 1) Blank page or 404 after deploy
- Ensure `index.html` is at the **root** (or set the correct **Root Directory** during import).
- If assets return 404, convert absolute paths like `/assets/style.css` → `./assets/style.css`.

### 2) "Build failed" messages
- For static sites, **leave Build Command and Output Directory empty**.
- If you previously chose a framework (Next.js, React, etc.) by mistake, edit the project → set **Framework Preset: Other**.

### 3) Navigation to subpages returns 404
- If you have multiple **real HTML pages** (e.g., `about.html`), link them like `href="about.html"` (not SPA routes).
- If you're using an SPA router (e.g., React Router), uncomment the `rewrites` in `vercel.json` to send all paths to `index.html`.

### 4) Caching
Static assets are cached aggressively via `vercel.json`. If you update them, consider versioning filenames (e.g., `style.v2.css`).

## Local test (optional)
Open `index.html` directly in your browser or use a simple server:

```bash
# Python 3
python -m http.server 5500
# then visit http://localhost:5500
```

---

**Contact:** stewardspath.tax@gmail.com · +1 647‑219‑1611
