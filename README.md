# FitTrack 3+1 · GitHub Pages PWA

## Deployment
1. Create a GitHub repository (e.g. `fittrack`).
2. Upload **all** files from this folder to the repository root, keeping the `icons/` folder and names.
3. Go to **Settings → Pages → Build and deployment → Deploy from a branch**, choose `main` and `/ (root)`, Save.
4. Wait for deployment, then open `https://YOUR-USERNAME.github.io/fittrack/` in Chrome on your phone.
5. Chrome menu → **Add to Home screen / Install app**. Open once online to cache app for offline use.

**Avoid `127.0.0.1`**. It points to your own phone, not the hosted app. Opening the standalone file through `file://` can work for preview but will not enable PWA install/service worker and storage behavior may differ.

## Features
- A/B/C and optional workouts **not tied to weekdays**.
- Default order: A (squat/chest/back/hamstrings/delts), B (hinge/back/shoulder/quads/core), C (chest/quads/back/hamstrings/chest fly), D (arms/delts).
- Swap each exercise with comparable movement-pattern alternatives. Swapped exercise gets a separate progress history.
- Add any exercise to an active workout; create custom exercises and custom packages.
- Record kg / reps / RIR **per set**, workout date, notes; save drafts automatically.
- Progress by exercise: top-set kg and estimated 1RM trend. This estimate is not a tested one-rep maximum.
- Bodyweight/waist and manual nutrition logging.
- CSV exports for workouts/body/food (Excel opens CSV); JSON full backup and restore.
- Local-only storage via browser `localStorage` (per origin+browser+device), no cloud sync. **Export JSON backups routinely**.

## Safety / tracking conventions
- Dumbbells: enter weight **per dumbbell** consistently. Bodyweight movements can use 0 kg external load; strength e1RM is not useful for these.
- Machine numbers differ; compare progress on the **same machine**.
- Weeks 1–2: 2 working sets, ~RIR 3–4; then gradually expand to program volume as tolerated.
- Do not train through pain. Cardio may be adjusted to bike if foot discomfort occurs.
- All nutrition values and targets are entered by user, not clinical guidance or food database values.

## Data migration
`file://`, localhost, and GitHub Pages have **different local storage**. If you have previous data, first export JSON from the old app and use **Data → Restore backup**. Older formats may not import automatically (the new app validates required arrays). Browser clearing site data also removes stored records.

## Security / privacy
No third-party JavaScript, analytics, accounts, network APIs or trackers are used. Hosting files publicly does not publish personal workout data (which remain in your device browser). Backups exported to other platforms are under your control. Do not share JSON backups publicly.
