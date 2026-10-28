# Draw schedule sources

Reviewed on 2026-10-28. Dates in the app use Gregorian years; Thai Buddhist
years in the sources are 543 years ahead (2566 = 2023, 2567 = 2024,
2569 = 2026, 2570 = 2027).

This review corrects the existing 2024 and 2026/2027 entries and adds the
confirmed New Year 2024 exception. It is not a complete archive of every
historical postponement. Recurring rules remain defaults for dates without
a documented override; they do not confirm an unannounced future draw.

## Overrides retained in the app

| Base draw | Actual draw | Evidence |
| --- | --- | --- |
| 2024-01-01 | 2023-12-30 | GLO's December 16, 2023 result sheet announces the next draw on December 30. The December 30 result sheet confirms that draw and identifies January 17, 2024 as the following draw, with no January 2 draw between them. |
| 2026-12-16 | 2026-12-17 | Thailand's Public Relations Department publishes GLO's announcement postponing both L6 and N3 for the royal cremation. |

- [GLO December 16, 2023 result sheet, including the next draw announcement](https://api.glo.or.th/utility/file/download/4666308d-6e2e-4156-9d0e-180cd9395dff).
- [GLO December 30, 2023 result sheet (copy hosted by MyHora)](https://www.myhora.com/lottery/files/load.aspx?id=25661230).
- [Public Relations Department / NBT: December 16, 2026 postponed to December 17, 2026](https://thainews.prd.go.th/thainews/news/view/2414807/?bid=1).

## Removed incorrect entries

### May 16, 2024 must remain May 16

Removed `2024-05-16 -> 2024-05-22`. The
[GLO May 16, 2024 result sheet](https://api.glo.or.th/utility/file/download/6a3df85e-6751-43bd-9bd1-b48aef766202)
explicitly dates the draw May 16, 2567 and records first prize 205690.
A holiday date alone is not evidence that a lottery draw was rescheduled.

### No evidence for moving New Year 2027 to December 30, 2026

Removed `2027-01-01 -> 2026-12-30`. This review found no official support for
that December date. [JS100's October 13, 2026 report](https://www.js100.com/th/site/news/view/165128)
instead names January 2, 2570 for the New Year draw. A standalone GLO
New Year announcement could not be verified, so this report is not used to
add a new override. January 2, 2027 follows the existing January 1 -> January 2
default rule. Recheck it against any subsequent GLO announcement.

## Maintenance

Use the original nominal draw (the 1st or 16th) as the key, even when the
actual draw moves into the previous calendar year. An override replaces the
recurring rule; it must not add an extra draw on top of that rule.

Record a source when adding or changing an exception. Prefer GLO result
sheets or GLO announcements published by government channels. Test both the
actual draw date and the superseded date, including the latest-draw lookup
and repository pending/empty classification.
