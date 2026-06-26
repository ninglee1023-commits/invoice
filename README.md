# Invoice Generator — Deploy to GitHub Pages

This folder is a complete, installable web app. Put it online once and you get a
permanent link you can share. To update the app later, just replace the files and
the same link refreshes automatically.

## Files in this folder
- `index.html` ............ the app itself (self-contained)
- `manifest.webmanifest` .. makes it installable ("Add to Home Screen")
- `sw.js` ................. offline support + instant loading
- `icon-192.png` / `icon-512.png` / `apple-touch-icon.png` .. app icons

Keep all of these together in the same folder.

---

## One-time setup: publish with GitHub Pages (free, permanent URL)

1. Go to https://github.com and sign in (create a free account if you don't have one).
2. Click the **+** at the top-right → **New repository**.
   - Name it something like `invoices`.
   - Set it to **Public**.
   - Click **Create repository**.
3. On the new repo page, click **uploading an existing file** (the link in the
   "Quick setup" box). Drag in EVERY file from this `deploy` folder, then click
   **Commit changes**.
4. Go to the repo's **Settings** tab → **Pages** (left sidebar).
5. Under "Build and deployment", set **Source** to **Deploy from a branch**,
   pick branch **main** and folder **/ (root)**, then **Save**.
6. Wait ~1 minute, refresh the Pages settings page. Your live link appears at the
   top, like:  `https://YOUR-USERNAME.github.io/invoices/`

Send that link to your friend. They open it in a browser; on a phone they can tap
**Share → Add to Home Screen** to get an app icon that opens full-screen.

---

## Updating the app later

When there's a new version of `index.html` (or any file):

1. In your repo, open the file → click the pencil/upload, or use
   **Add file → Upload files** and drop in the new version (overwrite).
2. Commit. The live link updates within a minute.
3. (If you changed the app and visitors don't see the update, bump
   `CACHE_VERSION` at the top of `sw.js` — e.g. `v1` → `v2` — and re-upload it.
   That forces installed copies to refresh.)

That's it — the URL never changes, only the contents behind it.
