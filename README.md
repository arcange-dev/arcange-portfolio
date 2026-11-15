# arcange-portfolio

Source for **https://arcange-portfolio.vercel.app** — the Arcange Dev portfolio site.

## What is in here

| Path | Purpose |
| :-- | :-- |
| `index.html` | The site entry document (Vite React single-page app shell) |
| `assets/index-*.js`, `assets/index-*.css` | The compiled application bundle and stylesheet |
| `favicon.ico` | Browser tab icon (16, 32 and 48 px) |
| `favicon.svg` | Vector tab icon for modern browsers |
| `favicon-16x16.png`, `favicon-32x32.png` | Raster tab icons |
| `apple-touch-icon.png` | iOS home screen icon (180 px) |
| `android-chrome-192x192.png`, `android-chrome-512x512.png` | Android / PWA icons |
| `site.webmanifest` | Web app manifest, theme `#080B12` |
| `assets/monogram.svg`, `assets/monogram-transparent.png`, `assets/logo-preview.png` | Brand assets, not loaded by the site |

## Deployment

The project is deployed on Vercel. Connect this repository to the Vercel project and
keep the framework preset on **Other / static**: there is no build step, so Vercel
serves the repository root as-is.

Every icon path is absolute (`/favicon.ico`, `/site.webmanifest`, ...), so the files
must stay at the repository root.

## Icons

The icon tags in `index.html` follow `INTEGRATION.md`. Theme colour is `#080B12`.
Verify after deploying:

- `/favicon.ico`
- `/favicon.svg`
- `/favicon-32x32.png`
- `/favicon-16x16.png`
- `/apple-touch-icon.png`
- `/site.webmanifest`
