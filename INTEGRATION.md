# Arcange Dev favicon: integration

I did not have your website project, so I could not edit it. Everything below is ready to drop in.

## Files to copy into the site's static folder
Vite or React: `public/`. Next.js: `public/` (or `app/` for favicon.ico). Plain HTML: the site root.

- favicon.ico (16, 32, 48), favicon.svg
- favicon-16x16.png, favicon-32x32.png
- apple-touch-icon.png (180), android-chrome-192x192.png, android-chrome-512x512.png
- integration/site.webmanifest (copy next to the icons)

monogram-transparent.png, monogram.svg and logo-preview.png are brand assets; keep them outside `public/` if you do not need them served.

## HTML
Replace all old icon tags in `index.html` (Next.js: `app/layout.tsx` metadata) with `integration/head-snippet.html`.

## Remove old references
Run from the project root and delete or update every hit:

    grep -rniE "favicon|apple-touch-icon|rel=.icon|manifest" --include=*.html --include=*.json --include=*.ts --include=*.tsx --include=*.js --include=*.jsx . --exclude-dir=node_modules --exclude-dir=dist
    find . -name "favicon*" -o -name "logo192*" -o -name "logo512*" -o -name "manifest.json" | grep -v node_modules

Delete old `favicon.ico`, `logo192.png`, `logo512.png` and any old `manifest.json` (Create React App) so only `site.webmanifest` remains.

## Test
1. Run the site, open `/favicon.ico`, `/favicon.svg` and `/site.webmanifest` directly: each must load.
2. Hard refresh (Ctrl+Shift+R). Browsers cache favicons hard; if the old one lingers, open the `/favicon.ico` URL and refresh it.
3. Chrome DevTools, Application, Manifest: icons should show with no warnings.
4. After deploying to Vercel, redeploy and check the tab on desktop and phone.
