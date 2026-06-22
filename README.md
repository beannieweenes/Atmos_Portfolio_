# ATMOS — Cosmic Portfolio

An immersive, scroll-driven WebGL portfolio. Static site, no build step.

- `index.html` — the experience (loads Three.js r0.137 + bloom from a CDN)
- `cases/` — the four case-study pages, shown in-place when you enter a planet

## Deploy to Vercel

This is a pure static site, so there is **no build command and no framework** — Vercel just serves the files.

### Option A — GitHub → Vercel (recommended)
1. Create a new repo on GitHub (e.g. `atmos-portfolio`).
2. From this folder, push it:
   ```
   git remote add origin https://github.com/<you>/atmos-portfolio.git
   git branch -M main
   git push -u origin main
   ```
3. Go to https://vercel.com/new, import the repo.
4. When asked for settings: **Framework Preset = Other**, **Build Command = (leave empty)**, **Output Directory = (leave empty / `.`)**. Click **Deploy**.

### Option B — Vercel CLI (needs Node.js)
```
npm i -g vercel
vercel          # follow the prompts
vercel --prod   # promote to production
```

That's it — `index.html` is served at the root, and `cases/*.html` load over HTTPS.
