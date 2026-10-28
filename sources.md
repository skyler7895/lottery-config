# Draw schedule history and evidence

Reviewed on **2026-10-28**. All JSON dates use Gregorian years; subtract 543
from Thai Buddhist years. The remote JSON contains **73 overrides**, **3
cancelled nominal draws**, and **1 result-date lookup exception**.

## Coverage and verification

- Reviewed the available 1990–2026 archive: **880 observed draw records**, from
  **1990-01-16 through 2026-10-16**. This is the earliest available archive found,
  not a claim to cover GLO's entire institutional history.
- Independently matched **all 397 date records from 2010-03-01 onward** against
  GLO's public `getLotteryMasterDataList` API. The lists match exactly. Its
  2026-11-01 upcoming record was excluded from historical verification.
- Retrieved original GLO PDF sheets through `getLotteryAward` for each applicable
  exceptional date available in that API. Older dates before 2010-03-01 were
  checked against MyHora and an independent archive, and are explicitly labelled
  **corroborated historical archives**, not original GLO verification.
- The archive records the COVID draw under its original ticket date, 2020-04-01.
  The original GLO sheet explicitly says it was **held on 2020-05-16**. The test
  fixture uses the actual day, giving 880 observed actual dates without duplicates.
- The retained **2026-12-16 → 2026-12-17** entry is an announced future exception,
  not an already-held historical draw. No unannounced 2027 override was added.
- Coverage starts at January 16, 1990. The preceding New Year draw in December
  1989 was not independently verified and is **not invented** in the JSON.
  Recurring defaults outside the verified coverage are not historical evidence.

## Primary data and corroborating sources

- [GLO history interface](https://www.glo.or.th/mission/awarding/orderby-time).
  Read-only API: `POST https://www.glo.or.th/api/lottery/getLotteryMasterDataList`
  with `{}`; result details: `POST https://www.glo.or.th/api/lottery/getLotteryAward`
  with Gregorian string fields `date`, `month`, `year`.
- [GLO draw-policy FAQ](https://www.glo.or.th/service/faq/award) describes the
  historic New Year → December 30 policy. Dated results take precedence over
  generic wording: January 2 draws are confirmed for 2025 and 2026.
- [MyHora yearly archive](https://www.myhora.com/lottery/), years 2533–2569.
  Each older entry below links to the individual result, with separate corroboration.
- [Independent January archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk)
  confirms January 16 through 2015. The shift to January 17 begins in 2016.
- [Independent December archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9)
  corroborates older December 30 results. Ignore its blank December 30, 2024 row;
  GLO's published dates show no such draw. Calendar year 2024 has 23 actual draws.

## Complete override ledger

A self-mapping preserves the actual historical day by cancelling a modern
recurring shift. A January 1 key refers to the **following nominal New Year draw**,
so `1991-01-01 → 1990-12-30` is one draw, not an additional December draw.

| Nominal base | Actual day | Evidence level | Evidence / purpose |
| --- | --- | --- | --- |
| 1990-01-16 | 1990-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2533.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 1991-01-01 | 1990-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2533.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 1991-01-16 | 1991-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2534.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 1992-01-01 | 1991-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2534.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 1992-01-16 | 1992-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2535.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 1993-01-01 | 1992-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2535.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 1993-01-16 | 1993-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2536.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 1994-01-01 | 1993-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2536.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 1994-01-16 | 1994-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2537.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 1995-01-01 | 1994-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2537.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 1995-01-16 | 1995-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2538.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 1995-05-16 | 1995-05-17 | Corroborated historical archives | Actual-date exception. [MyHora result](https://www.myhora.com/lottery/result-17-05-2538.aspx), [independent archive](https://www.nationtv.tv/news/378872785) |
| 1996-01-01 | 1995-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2538.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 1996-01-16 | 1996-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2539.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 1996-05-16 | 1996-05-17 | Corroborated historical archives | Actual-date exception. [MyHora result](https://www.myhora.com/lottery/result-17-05-2539.aspx), [independent archive](https://www.nationtv.tv/news/378872785) |
| 1997-01-01 | 1996-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2539.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 1997-01-16 | 1997-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2540.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 1998-01-01 | 1997-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2540.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 1998-01-16 | 1998-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2541.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 1999-01-01 | 1998-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2541.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 1999-01-16 | 1999-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2542.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 1999-03-01 | 1999-03-02 | Corroborated historical archives | Actual-date exception. [MyHora result](https://www.myhora.com/lottery/result-02-03-2542.aspx), [independent archive](https://lotto.mthai.com/lottostat-bymonth/march) |
| 2000-01-01 | 1999-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2542.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 2000-01-16 | 2000-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2543.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 2001-01-01 | 2000-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2543.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 2001-01-16 | 2001-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2544.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 2002-01-01 | 2001-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2544.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 2002-01-16 | 2002-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2545.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 2003-01-01 | 2002-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2545.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 2003-01-16 | 2003-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2546.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 2003-02-16 | 2003-02-17 | Corroborated historical archives | Actual-date exception. [MyHora result](https://www.myhora.com/lottery/result-17-02-2546.aspx), [independent archive](https://www.tnnthailand.com/lotto/104865/) |
| 2004-01-01 | 2003-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2546.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 2004-01-16 | 2004-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2547.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 2004-08-01 | 2004-08-02 | Corroborated historical archives | Actual-date exception. [MyHora result](https://www.myhora.com/lottery/result-02-08-2547.aspx), [independent archive](https://horoscope.trueid.net/detail/jgOM9LNEbq7Q) |
| 2005-01-01 | 2004-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2547.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 2005-01-16 | 2005-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2548.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 2006-01-01 | 2005-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2548.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 2006-01-16 | 2006-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2549.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 2007-01-01 | 2006-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2549.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 2007-01-16 | 2007-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2550.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 2008-01-01 | 2007-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2550.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 2008-01-16 | 2008-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2551.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 2009-01-01 | 2008-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2551.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 2009-01-16 | 2009-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2552.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 2010-01-01 | 2009-12-30 | Corroborated historical archives | New Year draw in previous calendar year. [MyHora result](https://www.myhora.com/lottery/result-30-12-2552.aspx), [independent archive](https://horoscope.trueid.net/detail/YJPbNx24LDm9) |
| 2010-01-16 | 2010-01-16 | Corroborated historical archives | Cancel current Teachers’ Day default. [MyHora result](https://www.myhora.com/lottery/result-16-01-2553.aspx), [independent archive](https://horoscope.trueid.net/detail/RkwO0rA3YZgk) |
| 2011-01-01 | 2010-12-30 | GLO original result sheet | New Year draw in previous calendar year. [GLO PDF](https://api.glo.or.th/utility/file/download/dfeb0b9d-31b8-4590-9ebc-44a417a05b57) |
| 2011-01-16 | 2011-01-16 | GLO original result sheet | Cancel current Teachers’ Day default. [GLO PDF](https://api.glo.or.th/utility/file/download/f0f211a7-0a40-4b25-b7fa-d46ffb819ebc) |
| 2012-01-01 | 2011-12-30 | GLO original result sheet | New Year draw in previous calendar year. [GLO PDF](https://api.glo.or.th/utility/file/download/f4937c0a-2d28-46a1-bc65-29179b863d9d) |
| 2012-01-16 | 2012-01-16 | GLO original result sheet | Cancel current Teachers’ Day default. [GLO PDF](https://api.glo.or.th/utility/file/download/cf6bf416-36a7-4a90-bc6b-dc0a21eefc03) |
| 2013-01-01 | 2012-12-30 | GLO original result sheet | New Year draw in previous calendar year. [GLO PDF](https://api.glo.or.th/utility/file/download/d9f40378-6358-402e-9081-2e73df7f7b41) |
| 2013-01-16 | 2013-01-16 | GLO original result sheet | Cancel current Teachers’ Day default. [GLO PDF](https://api.glo.or.th/utility/file/download/60560915-3f22-4aab-8681-12f1b39db9f8) |
| 2014-01-01 | 2013-12-30 | GLO original result sheet | New Year draw in previous calendar year. [GLO PDF](https://api.glo.or.th/utility/file/download/41f0006e-87bb-477e-9d3e-bb8cf44ee564) |
| 2014-01-16 | 2014-01-16 | GLO original result sheet | Cancel current Teachers’ Day default. [GLO PDF](https://api.glo.or.th/utility/file/download/7af12575-0461-4fbb-ad24-6a500e41e1da) |
| 2015-01-01 | 2014-12-30 | GLO original result sheet | New Year draw in previous calendar year. [GLO PDF](https://api.glo.or.th/utility/file/download/52a65b4c-e01d-41fc-a909-ed926da5d7d0) |
| 2015-01-16 | 2015-01-16 | GLO original result sheet | Cancel current Teachers’ Day default. [GLO PDF](https://api.glo.or.th/utility/file/download/971d1266-2839-458a-8029-620db67eb63d) |
| 2015-06-01 | 2015-06-02 | GLO original result sheet | Actual-date exception. [GLO PDF](https://api.glo.or.th/utility/file/download/87adcafd-b26e-4dec-a713-c3f21885fcf4) |
| 2015-12-16 | 2015-12-17 | GLO original result sheet | Actual-date exception. [GLO PDF](https://api.glo.or.th/utility/file/download/7a1b4278-fa64-44f6-b9b9-74fa8354c8d5) |
| 2016-01-01 | 2015-12-30 | GLO original result sheet | New Year draw in previous calendar year. [GLO PDF](https://api.glo.or.th/utility/file/download/5443bc76-dd42-4535-841f-8ba01f135e95) |
| 2017-01-01 | 2016-12-30 | GLO original result sheet | New Year draw in previous calendar year. [GLO PDF](https://api.glo.or.th/utility/file/download/75e19be0-338a-45b4-bab5-ea403202bb3d) |
| 2018-01-01 | 2017-12-30 | GLO original result sheet | New Year draw in previous calendar year. [GLO PDF](https://api.glo.or.th/utility/file/download/c8ea2ea3-0a93-4528-831f-7a3c9c3c86c4) |
| 2018-03-01 | 2018-03-02 | GLO original result sheet | Actual-date exception. [GLO PDF](https://api.glo.or.th/utility/file/download/5d400459-6460-4097-8558-c559cd80d774) |
| 2019-01-01 | 2018-12-30 | GLO original result sheet | New Year draw in previous calendar year. [GLO PDF](https://api.glo.or.th/utility/file/download/86c71c7e-dfaf-488a-91c7-ed878a385be4) |
| 2019-07-16 | 2019-07-15 | GLO original result sheet | Actual-date exception. [GLO PDF](https://api.glo.or.th/utility/file/download/15d20b9c-c4e9-482e-b04f-aaea3d3fc53f) |
| 2020-01-01 | 2019-12-30 | GLO original result sheet | New Year draw in previous calendar year. [GLO PDF](https://api.glo.or.th/utility/file/download/e5bd324a-5708-4042-a234-29d4f1f8a815) |
| 2020-04-01 | 2020-05-16 | GLO original result sheet | Held May 16; GLO API retains April 1 ticket date. [GLO PDF](https://api.glo.or.th/utility/file/download/5a8b5b4a-da58-4e6b-a49d-2f23fb031cdc) |
| 2021-01-01 | 2020-12-30 | GLO original result sheet | New Year draw in previous calendar year. [GLO PDF](https://api.glo.or.th/utility/file/download/faee0144-a40e-4974-8ae2-621befe79707) |
| 2022-01-01 | 2021-12-30 | GLO original result sheet | New Year draw in previous calendar year. [GLO PDF](https://api.glo.or.th/utility/file/download/d416c36a-dffe-4b06-96ba-6fc970f3269c) |
| 2022-02-16 | 2022-02-17 | GLO original result sheet | Actual-date exception. [GLO PDF](https://api.glo.or.th/utility/file/download/901b5f93-7315-4df4-b757-edc8462cc336) |
| 2023-01-01 | 2022-12-30 | GLO original result sheet | New Year draw in previous calendar year. [GLO PDF](https://api.glo.or.th/utility/file/download/fa547998-9f2f-440e-af75-7fc8f8b72bdb) |
| 2023-08-01 | 2023-07-31 | GLO original result sheet | Actual-date exception. [GLO PDF](https://api.glo.or.th/utility/file/download/2ff84569-9b0e-4e5e-860f-6a23d4a080a2) |
| 2024-01-01 | 2023-12-30 | GLO original result sheet | New Year draw in previous calendar year. [GLO PDF](https://api.glo.or.th/utility/file/download/58ae095b-350e-4d93-aa48-3ea0d562eafd) |
| 2026-12-16 | 2026-12-17 | GLO announcement via PRD; future | Actual-date exception. [PRD / NBT](https://thainews.prd.go.th/thainews/news/view/2414807/?bid=1) |

## COVID cancellations and GLO lookup date

The April 1, 2020 ticket issue was postponed to **May 16, 2020**. The nominal
**April 16, May 1 (normally held May 2), and May 16** issues were not issued.
The May 16 actual draw belongs to the April 1 issue, so generating another May 16
nominal draw would duplicate it. The next published issue is June 1.

Evidence:

- [Original GLO April 1 sheet, explicitly held May 16](https://api.glo.or.th/utility/file/download/5a8b5b4a-da58-4e6b-a49d-2f23fb031cdc).
- GLO's master date list has April 1 and June 1 with no intermediate nominal issues.
- [Thai PBS, March 25 board decision suspending two issues](https://www.thaipbs.or.th/news/content/290218).
- [Thai PBS, April 15 board decision postponing again and suspending the May 16 issue](https://www.thaipbs.or.th/news/content/291174).

Optional schema-1 fields encode these separately:

```json
"cancelled": ["2020-04-16", "2020-05-01", "2020-05-16"],
"resultDateOverrides": {"2020-05-16": "2020-04-01"}
```

`cancelled` contains **nominal** dates and must not overlap override keys.
`resultDateOverrides` maps an actual calendar day to the GLO API ticket date;
it must match the corresponding nominal → actual override. Neither field changes
published winning numbers. Omitted optional fields mean empty lists/maps.
The app must include support for these fields to display the COVID period
correctly; older app versions ignore them. The GLO result API inspected here
starts in March 2010, so earlier calendar dates do not guarantee result retrieval.

## Rejected entries and maintenance

- Do not add `2024-05-16 → 2024-05-22`:
  [GLO's May 16 result sheet](https://api.glo.or.th/utility/file/download/6a3df85e-6751-43bd-9bd1-b48aef766202)
  confirms the actual May 16 draw. A holiday alone does not establish a postponement.
- Do not add `2027-01-01 → 2026-12-30` without an official dated announcement.
- Only change dates with dated results or announcements; retain historical entries.
  Record the evidence level explicitly. Do not fill gaps by applying today's holiday
  rules retroactively. Dates are facts; causes are not assigned where unverified.
- `test/fixtures/draw_schedule_history.json` in the app repository contains the
  date-only regression reference for all 880 observed actual days. Compare the
  generated calendars against it, including cancellations and cross-year moves.
- The bundled app fallback retains its minimal original exceptions. This researched
  full snapshot is distributed by GitHub Pages and retained in the offline cache.
