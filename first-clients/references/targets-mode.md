# Targets mode: find people to contact

Use when the founder needs (more) people to reach out to, or when the Plan or Review modes find fewer than 5 good targets. Goal: 10 qualified people with a way to reach them, and a first message for each, saved in `marketing/targets.md`.

## 1. Know who you're looking for
Read `icp.md` (or ask 2 questions: who exactly, and what must be true for them to use it). Write down:
- **Hard prerequisites** (must use platform X, be in country Y, have a team, sell online…).
- **Trigger signals** that show the problem right now: asking for a recommendation, complaining about a competitor, "just launched and no users", hiring for the job the product does, a new store or repo, a funding or launch announcement.

## 2. Search: build queries from triggers
For each trigger, write 2–3 queries and run them where the ICP actually posts. Recipes that usually work:
Start with sources that have open APIs or public search (they work for an agent), then add the founder-browser list for the rest:
- **DEV.to:** `https://dev.to/api/articles?tag=<tag>&per_page=50` (newest posts by tag; also `&top=7`), then read the post for the author's links.
- **GitHub:** `https://api.github.com/search/repositories?q=topic:<topic>+created:>YYYY-MM-DD&sort=updated` and issues/discussions search; a new repo with 0–5 stars in the right topic is often a builder stuck at zero.
- **Bluesky:** `https://public.api.bsky.app/xrpc/app.bsky.feed.searchPosts?q=<words>&sort=latest`.
- **Stack Overflow / Stack Exchange:** `https://api.stackexchange.com/2.3/search/advanced?q=<words>&site=stackoverflow&sort=creation` for technical products.
- **Hacker News:** `https://hn.algolia.com/?q=<words>&dateRange=pastMonth&type=story` (and `type=comment`). API: `https://hn.algolia.com/api/v1/search_by_date?query=<words>&tags=story`.
- **GitHub:** search repos/issues/discussions, e.g. `<topic> created:>YYYY-MM-DD` or `"looking for" <problem> in:title,body`, sorted by newest.
- **Web search with site filters:** `site:reddit.com/r/<sub> <words>`, `site:indiehackers.com <words>`, `site:x.com <words>`, `site:linkedin.com/posts <words>`, plus the niche's forums.
- **Marketplaces and directories** where the ICP lists themselves (Product Hunt new launches, app stores, Etsy shops, Google Maps for local businesses, association member lists).
- **Competitor complaints:** reviews and threads where people complain about the alternative.

Sites that block you (Reddit, Indie Hackers, LinkedIn, Facebook groups) still work in the founder's own browser: give them a ready list of search links to open, and a 1-line instruction for what to copy back.

## 3. Qualify each person
Keep only people who meet all of these:
- **ICP fit:** meets the hard prerequisites (verified, or marked "likely" with why).
- **Recent:** active in the last ~30 days.
- **Reachable:** a route the founder can use (DM, email or site on their profile, an open thread where they asked, an on-topic GitHub issue). Never someone else's launch thread (a post announcing their own product). A post where the author asks readers for advice or tools counts as asking: one helpful reply there is fine.
- **Tier:** warm (asked for help) or cold (has the problem, didn't ask). Prefer warm; cold only by private message and only if the founder is OK with cold DMs.

## 4. Save to `marketing/targets.md`
One table, newest first. Keep only what's needed (GDPR):

| # | Who (handle) | Link | What they said / signal | Route | Tier | Status | Next step date |
|---|---|---|---|---|---|---|---|

Statuses: `to contact` → `contacted <date>` → `replied` → `trying it` → `client/user` (or `no`, `no reply`). Before adding new people, update the existing rows (ask the founder which were contacted and when, if you don't know). Delete rows when outreach is over or if someone asks. This is the one table format for `targets.md`, in every mode.

## 5. Write the first messages
One per target, referencing what they said, 60–120 words, disclosure that the founder built it, one clear low-effort ask, no link-dumping. Follow-ups only through private routes, at most 2, 5–7 days apart. Only claim what the founder actually told you about themselves.

## 6. Update the plan
If `PLAN.md` exists: add the outreach to this week (or next, if this week is full) **within the founder's hours**: replace or move another action rather than adding on top. Mirror it in `plan-data.json` (run `export.cjs --check`) and add a line to `results.md` (date, people found, contacted so far).

## 7. Reply
"Found N people (W warm, C cold). Start with these 3:" + names, routes and where the drafted messages are. If you found fewer than 10, say so and give the search links for the founder's browser.
