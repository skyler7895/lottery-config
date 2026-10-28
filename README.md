# Thai lottery draw overrides

Public endpoint: https://dev-skywalker.github.io/lottery-config/draw-overrides.json

This repository is the authoritative **complete** list of exceptional dates.
Normal draws (1st and 16th) and recurring shifts (January 1 → January 2,
January 16 → January 17, May 1 → May 2) are calculated in the app.

## Updating dates

1. Verify the date against a GLO announcement or published result. Add the
   supporting link to [sources.md](sources.md).
2. Edit `draw-overrides.json`, keeping `schemaVersion` equal to `1`.
3. Use Gregorian `YYYY-MM-DD` dates. Keys are the **original nominal draw**
   (the 1st or 16th), not the recurring replacement date. Values are the
   actual date, which may be in another year.
4. Commit to `main`. GitHub Pages deploys from `main` / `(root)` with
   `.nojekyll`. Check the Pages deployment and the public JSON URL afterward.

An entry can cancel a recurring shift by mapping a date to itself.
Deleting an entry restores the recurring/default calculation; an empty
`overrides` object intentionally removes **all** exceptional dates. Keep old
entries for historical calendars unless deliberately correcting them.

The app checks on launch, foreground resume, and network reconnection,
coalescing checks within 60 seconds. It keeps the last valid document offline
and uses bundled defaults only when no valid cache exists. Invalid JSON,
unsupported schemas, invalid dates, and HTTP failures leave the active
schedule intact. GitHub Pages deployment/CDN propagation is not instantaneous.
Devices must open/resume the app to receive changes and update local reminders.

## Initial publishing

Create public repository `dev-skywalker/lottery-config` and push these files
to `main`, including `.nojekyll`. In Settings → Pages, choose **Deploy from a
branch**, **main**, **/(root)**. No build tools, server, or API key are needed.

These are the initial publishing files supplied with the app. After publishing,
maintain the live data in this configuration repository.
