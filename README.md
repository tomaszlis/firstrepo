# firstrepo — MEGA.dev S01E03 "what it shows"

Support ticket [#4471](https://github.com/tomaszlis/firstrepo/issues) ("dates parse
mm/dd in eu locales") was merged by matching subject lines and marked known, as one
bug covering 412 reports. Reading the bodies and running the kb's own cause logic
(`causes.ts`) against the reports shows it's actually three bugs:

| Problem | Reports | Issue |
|---|---|---|
| Shared parser reads dates month-first, flips them for day-first-locale tenants | 374 | [#1](https://github.com/tomaszlis/firstrepo/issues/1) |
| `booking-v3` form shows a `MM/DD/YYYY` hint to day-first-locale tenants | 33 | [#2](https://github.com/tomaszlis/firstrepo/issues/2) |
| A one-day date shift, not a month/day swap (already footnoted by the desk as `oneDayMove`, never split out) | 5 | [#3](https://github.com/tomaszlis/firstrepo/issues/3) |

374 + 33 + 5 = 412.

The kb page explaining the split: [`kb/incidents/4471-split/+page.svx`](kb/incidents/4471-split/+page.svx),
rendered as the desk will see it: [`kb/incidents/4471-split/rendered.html`](kb/incidents/4471-split/rendered.html)
(see [`NOTES.md`](kb/incidents/4471-split/NOTES.md) for how the render was produced).
