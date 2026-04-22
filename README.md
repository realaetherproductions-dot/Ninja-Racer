# NinjaCycle

`NinjaCycle` is a mobile-first browser game: dodge traffic, fight enemy riders, and chain sword combos on a neon highway.

## Publish-ready files

- `index.html`: main game
- `manifest.json`: PWA/app metadata
- `sw.js`: offline cache/service worker
- `icon.svg`: app icon
- `netlify.toml`: Netlify publish + security headers
- `vercel.json`: Vercel security headers

## Safe ways to share it

The safest option is to host it as a static HTTPS site and share the website link.

Recommended hosts:

1. Netlify
2. Vercel
3. GitHub Pages

Avoid sending random executable files or unsigned APKs to people unless you intentionally package a native app later.

## Local preview

Serve the folder with a local web server instead of opening `index.html` directly, so the manifest and service worker work correctly.

Simple options:

1. `python -m http.server 8080`
2. `npx serve .`

Then open:

`http://localhost:8080`

## Netlify publish

1. Create a new site from this folder or from a Git repository.
2. Set the publish directory to the project root.
3. Deploy.
4. Share the HTTPS URL.

The included `netlify.toml` already sets useful security headers and cache rules.

## Vercel publish

1. Import the folder or repository into Vercel.
2. Keep the output as a static site.
3. Deploy.
4. Share the HTTPS URL.

The included `vercel.json` already adds security headers and cache rules.

## Before sharing publicly

1. Test on your phone over HTTPS.
2. Confirm install-to-home-screen works.
3. Check that restart, touch controls, and orientation behavior feel correct.
4. If you update the service worker often, ask testers to refresh once after new deployments.
