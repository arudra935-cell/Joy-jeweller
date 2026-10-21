JOY Jewellery — Installable PWA starter

CONTENTS
- index.html: JOY jewellery shopping prototype
- manifest.webmanifest: app name, colors, display mode, icons
- sw.js: service worker for app-shell caching/offline loading
- icons/icon-192.png and icons/icon-512.png: install icons

IMPORTANT
PWA installation and service workers require HTTPS hosting (or localhost for development). Opening index.html directly from your phone's file manager will not enable install/offline features. Host these files at the root of a website, preserving the folder structure.

SIMPLE HOSTING OPTION: GITHUB PAGES
1. On a computer, sign in to GitHub and create a new repository, e.g. joy-jewellery.
2. Upload all files and the icons folder from this ZIP (upload the files inside the JOY_PWA folder, not the outer folder itself).
3. In the repository, open Settings → Pages.
4. Under Build and deployment, choose deploy from a branch; select main and /(root), then Save.
5. Wait for GitHub Pages to publish the site. Use the HTTPS URL it provides.
6. Open that HTTPS URL in Chrome on Android.
7. Tap Chrome's three-dot menu → Install app or Add to Home screen → Install (wording varies).
8. Open JOY from the new home-screen icon. Visit once while online so the service worker can cache the app shell; then basic app shell loading can work offline.

ANDROID NOTES
- Keep index.html, manifest.webmanifest, sw.js, and icons at the paths shown.
- If you edit files after deployment, refresh online. If caching causes an old version to persist, update CACHE_NAME in sw.js (e.g. joy-jewellery-v2) and redeploy.
- This starter caches the app shell. It does not guarantee all remote content or third-party image resources work offline.
- Product data is demo data; prices and emoji artwork are illustrative. The prototype does not process real orders/payments or store customer accounts. A production launch needs backend, secure auth, inventory, payment gateway, order management, privacy policy, and business/product verification.
