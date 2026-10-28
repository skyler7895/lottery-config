# Thai lottery draw overrides

Public endpoint: https://skyler7895.github.io/lottery-config/draw-overrides.json

This repository is the authoritative **complete** list of exceptional dates.
Normal draws (1st and 16th) and recurring shifts (January 1 → January 2,
January 16 → January 17, May 1 → May 2) are calculated in the app.

The researched snapshot contains 73 overrides covering the available
1990–2026 date archive, three cancelled 2020 issues, and one GLO result-date
lookup exception. [sources.md](sources.md) records the evidence for every entry,
distinguishing original GLO sheets from corroborated older archives. The 2026
December postponement is an announced future entry, outside observed history.

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

Optional schema-1 fields support the 2020 COVID suspension:

- `cancelled`: nominal dates for issues that were not issued. These must not
  overlap override keys. Cancelling nominal May 16 does not cancel the April 1
  issue that was actually drawn on May 16.
- `resultDateOverrides`: actual day → GLO API ticket date. For example,
  `2020-05-16` looks up `2020-04-01` in GLO. Each mapping must correspond to a
  nominal → actual override. Omitted optional fields mean empty collections.

App versions must support these optional fields for accurate COVID-period
calendars and result lookup. Keep all three fields when editing the full snapshot.

The app checks on launch, foreground resume, and network reconnection,
coalescing checks within 60 seconds. It keeps the last valid document offline
and uses bundled defaults only when no valid cache exists. Invalid JSON,
unsupported schemas, invalid dates, and HTTP failures leave the active
schedule intact. GitHub Pages deployment/CDN propagation is not instantaneous.
Devices must open/resume the app to receive changes and update local reminders.

## Initial publishing

Create public repository `skyler7895/lottery-config` and push these files
to `main`, including `.nojekyll`. In Settings → Pages, choose **Deploy from a
branch**, **main**, **/(root)**. No build tools, server, or API key are needed.

The app also includes a publishing copy of these files. Maintain ongoing live
data here and keep the app's reference files and evidence ledger in sync.
