# App Icons

Place the following files here before deploying an installable icon:

- `icon-192.png` — 192x192px, used by manifest.json and apple-touch-icon
- `icon-512.png` — 512x512px, used by manifest.json
- `icon-512-maskable.png` — 512x512px with safe padding for maskable icons (Android)

Until these exist, the app still works as a PWA, but the home screen icon
on iPhone will fall back to a screenshot of the page instead of a custom icon.
