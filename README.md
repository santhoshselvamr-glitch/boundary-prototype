# Boundary — Ad-free Cricket (prototype)

This is a phone-friendly, installable-web-app prototype with simulated cricket scores. It is **not connected to a live score provider** and does not send real push notifications yet.

## What's included
- `index.html` — interactive mock UI: Live / Upcoming / Results, match details, commentary, sample scorecard, favourites and notification preference toggles.
- `manifest.webmanifest` — installable app metadata.
- `sw.js` — basic offline cache for the prototype.
- `icon.svg` — app icon.

## Try it on an Android phone

### Fastest preview
Open `index.html` in a browser that allows local HTML files. Some browsers restrict scripts or local-file behavior; if so, use the hosting steps below.

### Installable home-screen version
A PWA needs to be served from HTTPS (or localhost) for service workers and installation to work reliably. Phone-only path:
1. Sign in to GitHub in your browser and create a new public repository named `boundary-prototype`.
2. Upload the four files (`index.html`, `manifest.webmanifest`, `sw.js`, `icon.svg`) to the repository root.
3. In repository Settings → Pages, publish from the `main` branch and `/ (root)`.
4. Open the published HTTPS URL on Android in Chrome, open the browser menu, and choose **Add to Home screen** / **Install app** if offered.

## Important prototype notes
- Scores, teams, commentary and schedules are sample data. Do not present them as real match information.
- Notification switches are UI preferences only; no push notification service is wired up.
- No advertising SDK or ad network is included.
- This is a PWA prototype, not an Android APK/AAB. For Play Store publishing we will next create a native Kotlin/Jetpack Compose app or wrap the web app with a suitable Android shell, then test Play Console requirements.

## Suggested next technical milestone
Keep the UI on mock data and define a small `Match` data model plus a repository interface, so mock data can later be replaced with a licensed cricket API without rewriting the screens.
