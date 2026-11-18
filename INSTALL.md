# Building LUMOS

LUMOS is a single web page (`app/index.html`) wrapped in a small [Electron](https://www.electronjs.org) shell (`main.js`) so it can run as a desktop app.

## Running it without building anything

Open `app/index.html` in Chrome, Edge, Firefox or Safari. Everything works offline.

## Building the desktop app

1. Install [Node.js](https://nodejs.org) 20 or newer (the LTS version is fine). No account is needed.

2. Open a terminal (on Windows, PowerShell or Command Prompt) in this folder and install the build tools:

       npm install

3. Run LUMOS in a window to check it works:

       npm start

4. Build the single-file Windows executable:

       npm run dist:win

   The program is built as `dist/LUMOS-<version>.exe`. It is a portable executable: copy it anywhere and double-click it.

   On macOS, `npm run dist` builds `dist/LUMOS-<version>.dmg`; on Linux it builds `dist/LUMOS-<version>.AppImage`. Building the Windows `.exe` is easiest on Windows (or through GitHub Actions); building it on Linux or macOS needs Wine.

## Building on GitHub instead

You do not need to build anything on your own computer. The workflow in `.github/workflows/release.yml` builds all three versions on GitHub's servers:

- **To make a release:** push a tag whose name starts with `v`, for example:

      git tag v1.0.0
      git push origin v1.0.0

  When the run finishes (about 5–10 minutes), the `.exe`, `.dmg` and `.AppImage` appear on the repository's Releases page.

- **To test a build without releasing:** open the **Actions** tab, choose **Build and release**, and click **Run workflow**. The files appear under **Artifacts** at the bottom of that run.

## Publishing the web version

The workflow in `.github/workflows/pages.yml` publishes `app/` to GitHub Pages every time you push to `main`. Switch it on once in **Settings → Pages → Build and deployment → Source: GitHub Actions**.

## Changing the version

Edit `"version"` in `package.json`, add a section to `CHANGES.md`, commit, then tag the same version.
