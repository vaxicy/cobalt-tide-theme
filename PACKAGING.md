# Packaging

Run `scripts/package.ps1 -Force` (or without `-Force` when no archive exists yet).

The archives are written to `D:\迅雷下载\vibe coding\cobalt-tide-theme-<version>.zip`; `-Force` overwrites an existing one. Manifest is at the ZIP root. Contents: `manifest.json`, `logo/`, `README.md`, `LICENSE`, `PACKAGING.md`, `scripts/`, `store-assets/`, `.gitignore` (local data such as `.codebuddy/` is never packed).
