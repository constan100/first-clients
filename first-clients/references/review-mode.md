# Review mode: the weekly check-in

Use when `marketing/` exists and the founder brings numbers, asks "what now?", or asks for a weekly review. Goal: in about 10 minutes of their time, they know what worked, what to drop, and exactly what to do this week. No new research unless a rule below calls for it.

## 1. Read (don't ask what's written down)
`PLAN.md`, the last 2–3 rows of `results.md`, the if/then rules, `targets.md` statuses, and `plan-data.json`. Work out which week of the plan they're in from today's date.

## 2. Ask: one short batch
Only what you can't read yourself:
- This week's numbers for the north-star and supporting metrics (offer the exact list from the plan, so they just fill in values).
- Which of last week's checkboxes got done (list them; they answer "1, 3 done, 2 not").
- Anything that happened: replies, a post that worked, a blocker, a change in hours or budget.
If they already gave this in their message, skip straight to step 3.

## 3. Diagnose
- **Done vs. planned:** hours used vs. available. If they did less than half, the plan is too big, not the founder too lazy: cut, don't pile on.
- **Funnel:** find the first step with the biggest drop (e.g. many visits, no installs → front door or install problem; installs, no feedback → ask is weak). Fix the narrowest point, not the top.
- **Rules:** check every if/then rule and the day-30 milestone against the numbers. Say which fired.
- **Channels:** for each channel, results per hour spent. A channel with zero signal after its fair test (usually 2–3 weeks of the planned effort) gets dropped or changed; say which.
- **Small numbers are noisy:** with fewer than ~20 events, talk about direction, not percentages.

## 4. Update the files
- Append a row to `results.md`: date | done | numbers | what we learned | decision.
- Rewrite the **"Do this week"** section of `PLAN.md` (3 actions max, sized to the hours they actually had last week if that was less than planned) and adjust weeks ahead if a rule fired. Tick finished boxes.
- Update `plan-data.json` the same way:
  - Statuses: `done`, `partial` (with `"hours_done"`), `moved` (carried to a later week: copy it there as a new `todo` action), `skipped`. Add `"hours_done"` whenever it differs from the plan, so the Excel "hours done" is right.
  - Move the `"top3": true` flags to this week's 3 actions (remove them from last week's).
  - Append this week's numbers to `results`: `{ "date": "YYYY-MM-DD", "values": { "<metric name>": value }, "note": "…" }`, using the exact metric names from `metrics`.
  - If the founder checks in on a different day than `review.day`, update it.
  - Run `export.cjs --check` and fix what it reports.
- Assets refer to actions by file and description, not by action number, so renumbering never breaks them.
- Update `targets.md` statuses. Count only **good** targets not yet contacted (recent, reachable, fits the ideal customer); if fewer than 5 remain, run Targets mode's search step for 5 more, or make it this week's action.
- **Files from older versions of this skill** (e.g. `plan-30d.md`, `strategy-doc.md` duplicating the plan): move anything unique into `plan-data.json` or `strategy.md`, then replace the old file's content with a one-line pointer to `PLAN.md`. Don't delete files without asking.

## 5. Reply (short)
1. One-line verdict: on track / behind / ahead, versus the day-30 milestone.
2. What worked, what didn't (one line each, with the number).
3. The decision (keep, change, drop) and why.
4. This week's 3 actions.
5. Exports: if they asked for a file (or used exports before), re-run the exporter so the files match; the Excel "Weekly numbers" sheet now shows every logged week. Otherwise offer it in one line.

## Day 30 (and every 30 days)
Do a bigger review: compare against the goal, keep the channel(s) that produced results, write the next 30-day `PLAN.md` (keep the old one as `plan-archive/PLAN-<date>.md`), and re-check the 90-day goal honestly.
