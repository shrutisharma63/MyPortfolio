# Vercel deploy (static portfolio)

This repo is a plain static site (no build step). To avoid 404s on Vercel:

## 1) Vercel Project Settings
- Framework preset: **Other** / **Static** (any static preset)
- Build Command: **leave empty**
- Output Directory: **leave empty**

## 2) Entrypoint
Make sure `index.html` is present at the repo root (it is).

## 3) Routes
`vercel.json` rewrites all routes to `/index.html`.

### Assets
References in `index.html` are relative to the root:
- `style.css`
- `script.js`

So `style.css` and `script.js` must remain in the root (they are).

## 4) Re-deploy
After changing settings/redeploying, clear browser cache and retry.

