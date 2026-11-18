# firstrepo — MEGA.dev S01E03 "what it shows"

Support ticket [#4471](https://github.com/tomaszlis/firstrepo/issues) ("dates parse
mm/dd in eu locales") was merged by matching subject lines and marked known, as one
bug covering 412 reports. Running the kb's own cause logic (`causes.ts`) against the
reports shows it's actually two bugs:

| Problem | Reports | Issue |
|---|---|---|
| Shared parser reads dates month-first, flips them for day-first-locale tenants | 379 | [#1](https://github.com/tomaszlis/firstrepo/issues/1) |
| `booking-v3` form shows a `MM/DD/YYYY` hint to day-first-locale tenants | 33 | [#2](https://github.com/tomaszlis/firstrepo/issues/2) |

379 + 33 = 412.

(An earlier pass split a 5-report `oneDayMove` footnote out as a third ticket; the kb's
own `causes.ts` files those 5 under the same `parser` cause as #1, so that's one ticket,
not two — closed as a duplicate: [#3](https://github.com/tomaszlis/firstrepo/issues/3).)

The kb page explaining the split: [`kb/incidents/4471-split/+page.svx`](kb/incidents/4471-split/+page.svx),
rendered as the desk will see it: [`kb/incidents/4471-split/rendered.html`](kb/incidents/4471-split/rendered.html)
(see [`NOTES.md`](kb/incidents/4471-split/NOTES.md) for how the render was produced).
