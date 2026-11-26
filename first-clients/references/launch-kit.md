# Launch kit: one launch, done well

Use when the founder is preparing a specific launch (Show HN, Product Hunt, a subreddit, Indie Hackers, Kickstarter/Ulule, an app store release, a Steam page). Goal: a checklist and every piece of text ready, so launch day is just executing.

## 0. If there's no `marketing/` folder yet
Don't launch blind. Do a short version of SKILL.md first: Phase 1a (front door, path to first value, **public vs. local**), the Phase 4 blocker list, and the goal check using this platform's history as the benchmark (e.g. how comparable launches scored; search the platform's archive). Ask the founder only what's missing (goal for the launch, hours available on launch day, who already knows the product). Blockers go into the checklist as "fix before launch".

## 1. Check the platform (verify, don't recall)
Read the platform's current rules and guidelines page and note: eligibility (must be usable now? no betas? karma or account age?), what's forbidden (asking for upvotes, multiple accounts, link-only posts), format (title rules, first comment, gallery), and timing norms. Mark anything you couldn't read as unverified and tell the founder to check it.
- **Show HN:** something people can try now; plain title "Show HN: <name> – <what it does>"; the founder answers comments personally; never ask for upvotes.
- **Product Hunt:** tagline, description, gallery images, maker's first comment; launch is a full day of being present; you can't ask for upvotes, but you can tell people it's live.
- **Reddit:** each subreddit has its own rules and self-promotion limits; many require an account history; write a genuinely useful post (what you learned, how it works) with the link as a detail.
- **Crowdfunding:** needs an audience before day 1 (an email list); the first 48 hours decide momentum.

## 2. Pick the date
Avoid holidays and dead weeks for the target market, big platform events, and days the founder can't be online for the first 3–6 hours. A launch day usually needs more than a normal week's share of hours: ask the founder to block that time, set that week's `capacity` in `plan-data.json` to the agreed hours, and lighten the weeks around it. Name the date and the start time in the founder's timezone and the audience's. Timing advice that isn't from the platform itself is folklore: label it.

## 3. Readiness checklist (the week before)
- [ ] The path to first value works for a stranger (test it from a clean browser or machine).
- [ ] Front door says who it's for and what it does in 5 seconds; proof is visible (demo, example, screenshot).
- [ ] A way to capture interest if they're not ready (email list, star, wishlist, waitlist).
- [ ] Measurement is in place (analytics or platform stats; a "where did you hear about us?" question).
- [ ] Support ready: FAQ, a reply template for common questions, the founder's calendar cleared.
- [ ] Assets ready (step 4), proofread, and links tested.
- [ ] People who already know the product (users, email list, followers) told it's coming, with the rule for each platform respected: on Product Hunt you may say it's live; on Hacker News, don't send the link to friends or ask anyone to upvote or comment (HN penalizes it), just post it on your own channels after it's up.

## 4. Write the assets
Write each in the platform's style (see step 1): title options (3), the post/description, the founder's first comment (why they built it, what's next, a question for the audience), 3–5 replies for likely questions or criticism (honest, short), gallery captions if needed, a short announcement for the founder's own audience and email list, and a thank-you/follow-up post for after.

## 5. Launch-day run sheet
Hour by hour: post, share with own audience, reply to every comment within ~30 minutes for the first hours, log numbers at +3h/+24h, no vote-begging, no sockpuppets, stay polite under criticism.

## 6. After (48 hours later)
- Record results in `results.md` against the threshold set in the plan.
- Reply to every comment and email; turn questions into FAQ and product fixes.
- Contact everyone who signed up personally (warm targets now).
- Write a short "what I learned launching on X" post for a second wave.

## 7. Save
- Shared material (the date, the checklist, the run sheet, numbers to log) goes in `marketing/assets/launch-week.md`; each platform's own texts go in `marketing/assets/launch-<platform>.md`. Don't repeat the shared parts in the platform files.
- Write or update `PLAN.md` (launch week as "Do this week") and `plan-data.json`: the launch actions in `weeks`, the readiness checklist and the run sheet in `checklists` (see `references/export.md`), and the launch threshold in `if_then`.
- Offer exports: the Excel file then has a sheet per checklist (readiness, run sheet) with tick boxes and a column for the numbers at +3h/+24h/+48h.
