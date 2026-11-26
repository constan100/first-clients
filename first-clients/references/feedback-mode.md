# Feedback mode: turn what users said into decisions

Use when the founder shares feedback (interview notes, DMs, emails, support tickets, reviews, GitHub issues, survey answers, call transcripts) or asks what users want. Goal: a short, ranked list of what to change, plus the words customers actually use, so marketing and product both get better.

## 1. Collect
Ask for the raw material (paste, files, or folders) and, if useful, where it came from and when. Read all of it. Note how many distinct people it covers: 3 people saying something is not the same as 1 person saying it 3 times.

## 2. Sort
For each piece of feedback, tag:
- **Type:** bug, missing feature, confusing step, pricing/value, praise, wrong customer (they're not the ICP).
- **Funnel stage:** discover → try → get value → pay → stay/recommend.
- **Who:** ICP or not. Feedback from non-ICP users matters less; say so.

## 3. Find the themes
Group into themes. For each: how many people, a short quote or two (word for word, anonymized unless they agreed to be named), and the stage it hurts.

## 4. Decide
Rank themes by (people affected × how close to payment/value) ÷ effort. For each top theme, one decision: **fix now**, **test**, **later**, or **no** (with why). Remember the founder's hours; 1–3 fixes per week is plenty.

## 5. Feed marketing
- **Customer language:** list phrases users use for the problem and the benefit; suggest updates to the front-door headline and outreach messages.
- **Proof:** praise that could become a testimonial. Never publish it without the person's explicit permission; draft the permission request message.
- **ICP update:** if the users who love it differ from the planned ICP, say so and suggest updating `icp.md`.

## 6. Save and reply
Write `marketing/feedback.md` (date range, sources, themes table, decisions, customer language, testimonial candidates with consent status). Add the "fix now" items to `PLAN.md`'s week and `plan-data.json`. Reply with the top 3 themes, the decisions, and one sentence on what it means for the plan. Offer to apply fixes (Fix mode) or export the themes table to Excel.
