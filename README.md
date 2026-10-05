<p align="center">
  <img src="https://raw.githubusercontent.com/vaxicy/cobalt-tide-theme/main/logo/logo128.png" width="128" alt="Cobalt Tide Theme icon">
</p>

<h1 align="center">Cobalt Tide Theme</h1>

<p align="center">A fresh tide for your browser: deep cobalt, sky blue and icy aqua.</p>

<p align="center">
  <img src="https://img.shields.io/badge/Chrome%20Web%20Store-theme-blue?logo=googlechrome" alt="Chrome Web Store">
  <img src="https://img.shields.io/badge/version-1.0.0-blue" alt="version">
  <img src="https://img.shields.io/badge/license-Non--Commercial-lightgrey" alt="license">
</p>

## About

Cobalt Tide opens the browser onto cool, coastal water. A deep cobalt window frame wraps the top of the window, the toolbar and active tab wash it in sky blue, and the new tab page fills with soft icy aqua, so the page you are reading stays the brightest thing on screen. Deep navy text carries every label, icon, bookmark and heading, keeping contrast comfortable across all of those light surfaces. The design is flat colour throughout — no wallpaper, no textures, no gradients — and the icon distills it into a single royal-blue tide curling around a small circle.

## Color Palette

| Color | Hex | Usage |
|-------|-----|-------|
| Deep Cobalt | `#293681` | Window frame and toolbar buttons |
| Royal Blue | `#4274D9` | Links and brand accents on the new tab page |
| Sky Blue | `#95CCDD` | Toolbar and active tab |
| Icy Aqua | `#D0E7E6` | New tab page background |
| Frost | `#F7FBFC` | Omnibox (address bar) field and inactive tab text |
| Deep Navy | `#233052` | Tab, bookmark, toolbar and new-tab text |

## Features

- Deep cobalt frame with a sky-blue toolbar and active tab for crisp, readable browser chrome.
- Flat, solid colour design with no wallpaper, textures or gradients.
- Deep navy text tuned for contrast on every light surface.
- Calm icy aqua new-tab page whose logo is drawn in a single tone instead of the full-colour mark.
- One continuous frame colour whether the window is focused or not.
- Pure theme: no scripts, no permissions, nothing collected.

## Install

### From source (unpacked)

1. Download or clone this repository.
2. Open Chrome and navigate to `chrome://extensions`.
3. Enable **Developer mode** in the top-right corner.
4. Click **Load unpacked** and select this folder.

### From the Chrome Web Store

The store listing is in preparation. Until it is live, load the unpacked copy with the steps above.

## Preview

![Cobalt Tide Theme browser preview](https://raw.githubusercontent.com/vaxicy/cobalt-tide-theme/main/store-assets/screenshots/en/screenshot-1-browser.png)

![Cobalt Tide Theme palette](https://raw.githubusercontent.com/vaxicy/cobalt-tide-theme/main/store-assets/screenshots/en/screenshot-2-introduction.png)

### Store promo tiles

![Cobalt Tide Theme marquee](https://raw.githubusercontent.com/vaxicy/cobalt-tide-theme/main/store-assets/promo/1400x560.png)

<p align="center">
  <img src="https://raw.githubusercontent.com/vaxicy/cobalt-tide-theme/main/store-assets/promo/440x280.png" width="440" alt="Cobalt Tide Theme promo tile">
</p>

## Files

| File | Description |
|------|-------------|
| `manifest.json` | Chrome theme manifest (MV3) with inline `theme` config — single source of truth for every colour |
| `logo/logo128.png` | Chrome Web Store icon (128x128) |
| `store-assets/screenshots/en/` | Store listing screenshots (1280x800) |
| `store-assets/promo/` | Promo tiles (440x280 and 1400x560) |
| `store-assets/references/` | The browser and promo mock-up HTML plus their PNG renders |
| `store-assets/store-description.txt` | Store listing detailed description (English) |
| `scripts/` | Generators: layout references, store assets, upload zip |
| `PACKAGING.md` | How the upload ZIP is built |
| `LICENSE` | Non-Commercial License |

## Regenerating the assets

```
pip install -r scripts/requirements.txt
python3 scripts/generate-store-assets.py
```

The script renders the reference layouts with headless Chromium, writes the screenshots and promo tiles into `store-assets/`, and asserts that the logo is exactly 128x128.

## Packaging

```
powershell -ExecutionPolicy Bypass -File scripts/package.ps1 -Force
```

Writes a complete ZIP named `cobalt-tide-theme-<version>.zip` to the default upload folder outside the repository, with `manifest.json` at the archive root. `-Force` overwrites any existing archive.

## License

Non-Commercial License — personal use permitted, commercial use requires permission. See [LICENSE](LICENSE).
