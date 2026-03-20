# CarbCalc

A mobile-friendly Progressive Web App for calculating carbohydrates in home-cooked meals. Designed for people with diabetes tracking carbs across recipes.

Vibe coded with Claude Code / Sonnet 4.6

## Features

- **Barcode scanner** — live camera scans barcodes and looks up carbs from Open Food Facts (3M+ products)
- **OCR label reader** — photograph the nutrition label, app reads carbs automatically
- **Recipe builder** — add multiple ingredients, track running carb total
- **Portion calculator** — enter final dish weight and portion size to get carbs per plate
- **Works offline** — app shell cached by service worker after first load
- **Installable** — add to home screen on iOS and Android

---

## Publishing to GitHub Pages (step by step)

### 1. Create a GitHub account
Go to https://github.com and sign up if you don't have an account.

### 2. Create a new repository
- Click the **+** icon → **New repository**
- Name it `carbcalc` (or anything you like)
- Set it to **Public**
- Leave everything else as default
- Click **Create repository**

### 3. Upload the files
- On the repository page click **uploading an existing file**
- Drag and drop ALL files from this folder:
  - `index.html`
  - `manifest.json`
  - `sw.js`
  - `icon-192.png`
  - `icon-512.png`
- Click **Commit changes**

### 4. Enable GitHub Pages
- Go to **Settings** → **Pages** (left sidebar)
- Under **Source**, select **Deploy from a branch**
- Branch: **main**, folder: **/ (root)**
- Click **Save**

### 5. Wait ~60 seconds, then open your app
Your app will be live at:
```
https://YOUR-USERNAME.github.io/carbcalc/
```

### 6. Add to home screen

**iPhone (Safari):**
1. Open the URL in Safari
2. Tap the Share button (box with arrow)
3. Scroll down and tap **Add to Home Screen**
4. Tap **Add**

**Android (Chrome):**
1. Open the URL in Chrome
2. Tap the three-dot menu
3. Tap **Add to Home screen**
4. Tap **Add**

The app will open fullscreen like a native app with its own icon.

---

## File structure

```
carbcalc/
├── index.html      ← the whole app
├── manifest.json   ← PWA metadata (name, icon, colours)
├── sw.js           ← service worker (offline caching)
├── icon-192.png    ← app icon (Android, PWA)
└── icon-512.png    ← app icon (large / splash screen)
```

## Updating the app

Edit `index.html`, re-upload it to GitHub, and bump the cache version in `sw.js` from `carbcalc-v1` to `carbcalc-v2` so phones pick up the new version.
