# QR Strobe

Offline file transfer between devices using animated QR codes (camera + strobing QR display). No server, no network required — pure static PWA.

## Local development

Just open `index.html` via any static file server (camera access requires HTTPS or `localhost`), e.g.:

```
npx serve .
```

## Deploy (Netlify)

```
npx netlify-cli login
npx netlify-cli init      # first time: link/create the site
npx netlify-cli deploy --prod
```

Netlify publishes only the contents of this repo (static files: `index.html`, `manifest.json`, `sw.js`, `icons/`) — no build step or secrets involved.

## Install on iPhone (PWA)

1. Open the deployed Netlify URL in Safari.
2. Tap Share → **Add to Home Screen**.
3. Launch from the home screen icon — runs full-screen, works offline after first load.

See [icons/README.md](icons/README.md) for the home screen icon files still needed.
