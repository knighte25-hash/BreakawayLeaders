# Breakaway 2026 — Leader Info Packet (Web App)

A mobile web app version of the Breakaway 2026 Leader Info Packet (July 17–20, Cottages Christian Retreat, Panama City Beach, FL). Built as a single self-contained page: a home screen with a card for each section of the packet, leader notes in red, tap-to-call phone numbers, and the camp map embedded. Works offline once loaded, so it keeps working at the beach with spotty service.

## What's in this folder

| File | Purpose |
|---|---|
| `index.html` | The entire app (all content, styles, and images inlined) |
| `manifest.webmanifest` | Lets phones install it like an app (name, icon, colors) |
| `sw.js` | Service worker — caches the app so it opens offline |
| `apple-touch-icon.png` | Home-screen icon for iPhone |
| `icon-192.png`, `icon-512.png` | App icons for Android / manifest |

## How to publish on GitHub Pages (free)

1. Sign in at [github.com](https://github.com) and click **+** (top right) → **New repository**.
2. Name it something like `breakaway-2026`, leave it **Public**, and click **Create repository**.
3. On the new repo page, click **uploading an existing file**, drag in ALL the files from this folder (`index.html`, `manifest.webmanifest`, `sw.js`, and the three `.png` icons), and click **Commit changes**.
4. Go to **Settings** → **Pages** (left sidebar).
5. Under **Build and deployment**, set **Source** to "Deploy from a branch," choose branch **main** and folder **/ (root)**, then click **Save**.
6. Wait a minute or two, then refresh the Pages screen. Your link will appear at the top:
   `https://YOUR-USERNAME.github.io/breakaway-2026/`

That link is what you text or Remind out to your leaders.

## How leaders add it to their iPhone home screen

1. Open the link in **Safari** (must be Safari for this to work).
2. Tap the **Share** button (square with the up arrow).
3. Scroll down and tap **Add to Home Screen**, then **Add**.

It now opens full-screen like a regular app — no browser bars — with the Breakaway logo as its icon, and it works even with no signal once it's been opened once.

## Updating the packet later

Edit or replace `index.html` in the repo (GitHub → open the file → pencil icon → paste new content → Commit). Also bump the version string at the top of `sw.js` (e.g. `breakaway-2026-v1` → `-v2`) so phones that saved the old version pick up the new one. GitHub Pages republishes automatically within a couple of minutes.
