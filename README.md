# Leafland App — Prototype

Phone app prototype for Leafland: promotions, tree catalogue with specs and grades, Tree Finder, favourites and a quote list.
**Ordering is disabled.** "Request quote", call, email and booking only show a "Prototype only" message. All stock, prices and promotions are sample data.

## Build the APK with GitHub (no Android Studio needed)

1. Create a new repository on GitHub (e.g. `leafland-app`).
2. Upload **everything in this folder**, including the hidden `.github` folder.
   - Easiest way: on the repo page click **Add file → Upload files** and drag the folder contents in.
   - If the `.github` folder doesn't upload by drag-and-drop, create the file by hand:
     **Add file → Create new file**, name it `.github/workflows/build-apk.yml`, and paste in the contents of that file.
3. Go to the **Actions** tab. The "Build Android APK" job starts automatically (or click **Run workflow**).
4. When it finishes (about 5 minutes), open the run and download **leafland-prototype-apk** under *Artifacts*.
5. Unzip it to get `app-debug.apk`, copy it to an Android phone and open it (allow "Install unknown apps" when asked).

## Editing the app

Everything is in `www/index.html`:
- Trees: the `TREES` list near the top of the `<script>` (names, specs, grades `[bag size, current height, price, stock]`).
- Promotions: the `PROMOS` list.
- Colours: the `:root` variables at the top of the `<style>`.

Push a change and GitHub builds a new APK.

## Files
- `www/index.html` — the whole app
- `capacitor.config.json` — app name and ID (`nz.co.leafland.prototype`)
- `assets/` — app icon and splash screen
- `.github/workflows/build-apk.yml` — the GitHub build
