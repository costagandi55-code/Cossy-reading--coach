# Mt Ruunze English Reading Coach — Offline-capable website

## What is included
- `index.html` — the reading coach and lessons
- `manifest.webmanifest` — installable web app details
- `sw.js` — caches the app so it can reopen offline after first successful online load
- `icon.svg` — app icon

## Important
This is an installable Progressive Web App (PWA) package, not an Android APK.
For service-worker offline caching and installation, publish the folder to an HTTPS website first.
Opening `index.html` directly from Downloads may work for practice, but it does not activate the service worker reliably.

## Publish it free (one-time setup)
One option is GitHub Pages:
1. Sign in or create an account at https://github.com
2. Create a new public repository, for example `mt-ruunze-reading-coach`.
3. Upload all four files from this folder to the repository's root.
4. In the repository, open Settings → Pages.
5. Choose deployment from the `main` branch and `/ (root)`, then Save.
6. Wait for the published HTTPS URL to appear. Open that URL on each learner's phone while online once.

Other static HTTPS hosts can also be used. Hosting provider steps may change.

## Install on Android
1. Open the published HTTPS link in Chrome.
2. Open Chrome's three-dot menu.
3. Choose `Install app` or `Add to Home screen` if offered.
4. Confirm, then open the new icon once while online.
5. Turn off mobile data and test that the app opens and lessons work offline.

## Progress and privacy
- The prototype saves lesson results in the browser's local storage on that phone.
- Results do not automatically sync to a teacher's device.
- Do not enter sensitive personal information. Use learner codes.
- Clearing browser/site data can erase saved results. Export progress records regularly.

## Limitations
- This package contains sample lessons, not the full official syllabus.
- The service worker caches the app shell, not remote resources; the current lessons are built into the HTML.
- This does not generate an APK. An APK would require an Android build/signing workflow or a trusted PWA-to-APK packaging service.
