# AVATAR: THE FOUR NATIONS

A self-contained, classroom-friendly student picker inspired by the four elemental nations. Built with HTML, CSS, vanilla JavaScript, inline symbols, generated particle effects, and optional Web Audio sounds. No frameworks, external images, audio files, or build steps.

## Files (repository root)

- `index.html` — application structure
- `style.css` — responsive visual design and animation
- `script.js` — roster, selection, history, audio, and UI logic
- `manifest.webmanifest` — installable PWA metadata
- `sw.js` — offline cache
- `icon-192.png`, `icon-512.png` — generated PWA icons

## Create and publish from an Android phone

1. Open **github.com** in Chrome and sign in.
2. Tap **+** (or the New repository option). Name the repository, for example `four-nations-picker`; choose Public if you want free GitHub Pages.
3. Create the repository. Open it and tap **Add file → Create new file**.
4. Create each file listed above with its exact filename. Paste the matching contents from this project. Keep all files at the repository root—do not create a project or assets folder.
5. For PNG icons, use the supplied icon files in the ZIP. On GitHub mobile web, use **Add file → Upload files** and upload both icons from your phone's Downloads.
6. Commit each addition using the **Commit changes** button.
7. In the repository, open **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, select `main` (or your default branch), and choose **/(root)**. Tap **Save**.
8. Wait for the Pages deployment to finish. The published URL is shown in Settings → Pages and normally looks like `https://YOUR-USERNAME.github.io/REPOSITORY/`. Open that URL in Chrome.

## Install on Android

1. Open the published HTTPS URL in Chrome.
2. Use the Chrome menu **⋮ → Install app** or **Add to Home screen** (the wording depends on Chrome version).
3. Confirm. Launch Four Nations from the home-screen icon. The first visit should be online so the service worker can cache the app.

## Use the classroom picker

- Tap a nation card to enter its arena.
- Choose **Teacher-selected nation**, **Random Avatar mode**, or **Fixed nation mode** from the selection-mode menu. Teacher-selected and fixed modes use the chosen nation; Random Avatar assigns a nation for each pick.
- Add students individually or paste a list with one name per line. Duplicate names are retained as separate entries.
- **Choose a Student** selects an unselected roster entry. Each entry is chosen once per round. Use **Begin New Round** to reset the cycle.
- History, round progress, and roster save in this browser's local storage. CSV export downloads the selection log.
- Audio starts only after the teacher enables it and interacts with the app. Audio is optional.

## Update the app

Edit the relevant root file on GitHub and commit. For reliable cache refreshes, change the cache version in `sw.js` (for example `four-nations-v2`) when shipping a major update. Reopen the published site and refresh. If Chrome keeps old files, open the site, use Chrome site settings to clear its stored data, then reload.

## Troubleshooting

- **Pages URL 404:** verify Settings → Pages is enabled, branch is correct, and files are in the root. Wait a few minutes after committing.
- **PWA install missing:** use Chrome on Android, visit the HTTPS Pages URL, and ensure `manifest.webmanifest`, icons, and `sw.js` are present at the root. Browser install prompts vary.
- **Offline doesn't load:** visit once while online, wait for the page to finish, then reload. Service-worker caching requires HTTPS (GitHub Pages supplies it). Check that filenames and relative paths are exact.
- **New version not visible:** increment the service worker cache name, commit, wait for Pages deployment, and reload.
- **Audio silent:** audio is disabled by default. Enable Sound in the top bar or Settings, then tap a button. Device silent mode/browser audio restrictions can still apply.
- **Roster seems missing:** local storage is per browser/device and can be cleared by Android Chrome site-data cleanup. Export history regularly; this app does not sync between devices.

## Privacy and compatibility

This project has no external runtime requests. Names and history stay in the local browser storage unless the teacher exports them. Use a current Android Chrome or desktop browser. GitHub Pages hosts the static files; no server or account backend is required.

## Credits and disclaimer

This is a fan-made classroom activity inspired by elemental fantasy themes. It is not affiliated with or endorsed by the rights holders of Avatar: The Last Airbender. Use of the app does not require copyrighted character art, logos, music, or show audio.
