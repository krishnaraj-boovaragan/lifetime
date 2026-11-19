# Lifetime — web app version

A free, installable web app (PWA) version of the Lifetime iPhone app.
It works on iPhone, Android, Mac and Windows, and keeps working offline.

## Files

- `index.html` — the whole app (screens, styling and logic)
- `manifest.webmanifest` — app name, colours and icons used when installing
- `sw.js` — service worker that lets the app open offline
- `icons/` — app icons made from the original AppIcon.png

## Try it on your Mac

In Terminal:

    cd ~/"Claude projects/Lifetime/web"
    python3 -m http.server 8000

Then open http://localhost:8000 in your browser.

## Put it online for free (GitHub Pages)

1. Create a free account at github.com.
2. Create a new **public** repository, e.g. `lifetime`.
3. Click **Add file → Upload files**, and drag in everything inside this `web` folder
   (index.html, manifest.webmanifest, sw.js and the icons folder). Click **Commit changes**.
4. Go to **Settings → Pages**, set **Source** to "Deploy from a branch",
   choose branch `main` and folder `/ (root)`, then **Save**.
5. After a minute your app is live at `https://YOUR-USERNAME.github.io/lifetime/`.

Other free hosts work just as well: Netlify, Vercel, Cloudflare Pages.

## Install it

- **iPhone:** open the link in **Safari** → tap **Share** → **Add to Home Screen**.
- **Mac / Windows:** open the link in Chrome or Edge → click the **Install** icon in the address bar.
  (Safari on Mac: **File → Add to Dock**.)

## Good to know

- Data is saved on each device separately. Use **Back up** / **Restore** at the bottom of the list
  to copy your people from one device to another, or to keep a safe copy.
- On iPhone, use it from the Home Screen icon rather than a Safari tab — Safari can clear data
  for websites you haven't opened in a while, but not for Home Screen apps.
- Home Screen widgets are not possible for web apps; that part only exists in the native app.
- If you change a file later, also change `VERSION` at the top of `sw.js` so phones pick up the update.
