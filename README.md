# Kings Puzzle (n×n, k per row/col)

Interactive browser app to experiment with placing kings on an n×n chessboard such that exactly **k** kings appear in **every** row and column, and no two kings are adjacent (8-neighborhood).

## Files
- `index.html` – the whole app (HTML/CSS/JS in one file)
- `.nojekyll` – ensures GitHub Pages serves files as-is
- `.gitignore` – basic ignores for macOS/IDE clutter
- `LICENSE` – MIT License (feel free to edit the copyright holder)

## Run locally
1. Double-click `index.html` to open in your browser.
2. Or serve it (optional) to avoid any local file URL issues:
   ```bash
   python3 -m http.server 5500
   # then visit http://localhost:5500/index.html
   ```

## Publish on GitHub Pages (GUI)
1. Create a new repo on GitHub, e.g. `kings-puzzle`.
2. Upload the four files in this folder: `index.html`, `.nojekyll`, `.gitignore`, `LICENSE`.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
5. Set **Branch** to **main** and **/ (root)**, then **Save**.
6. Wait for the green check; your site will be at:
   ```
   https://<your-username>.github.io/kings-puzzle/
   ```

## Publish on GitHub Pages (CLI)
```bash
# 1) Create and init repo
mkdir kings-puzzle && cd kings-puzzle
# put these files into this folder
git init
git add .
git commit -m "init: kings puzzle"

# 2) Create repo on GitHub (or do this in the web UI)
# then add remote and push
git branch -M main
git remote add origin https://github.com/<your-username>/kings-puzzle.git
git push -u origin main

# 3) Enable GitHub Pages in Settings → Pages (branch: main, folder: / (root))
```

## One‑click hosting alternatives
- **Netlify**: drag `index.html` onto app.netlify.com → gets a public URL.
- **Vercel**: `vercel deploy` or drag-and-drop in the dashboard.
- **Replit / CodePen**: paste the HTML contents and click **Run**/**Share**.

## Notes
- Everything runs client-side. No backend needed.
- Tested in Chromium-based browsers and Firefox.
- If you file issues/PRs, include your **n**, **k**, and a screenshot if possible.
