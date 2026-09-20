# Deploying the Personal Finance Ledger to GitHub Pages

You need all **three files** (`index.html`, `manifest.json`, `sw.js`) at the
root of the same repo — they work together.

## Steps

1. Go to https://github.com/new and create a new repository (public is fine,
   e.g. `finance-ledger`).
2. Upload `index.html`, `manifest.json`, and `sw.js` to the repo root
   (drag-and-drop on the "Add file → Upload files" page works, or use git).
3. Commit them to the `main` branch.
4. Go to the repo's **Settings → Pages**.
5. Under "Build and deployment", set **Source** to "Deploy from a branch",
   pick branch `main` and folder `/ (root)`, then **Save**.
6. Wait 1-2 minutes. GitHub will show your live URL, something like:
   `https://<your-username>.github.io/finance-ledger/`
7. Open that link on your phone or computer and use the **"Add to device"**
   button — since it's now served over real HTTPS with a working service
   worker, browsers that support the native install prompt (Chrome, Edge,
   Android) should offer a genuine one-tap install. iPhone/iPad Safari and
   Firefox still don't support automatic install prompts (no browser does,
   not a limitation of this page) — the button shows their manual steps
   instead (Share → Add to Home Screen, etc.).

## Notes

- All your data stays in the browser on your own device (`localStorage`) —
  nothing is sent to GitHub or anywhere else.
- If you ever update the app, just re-upload the changed file(s) and commit —
  Pages redeploys automatically in about a minute.
