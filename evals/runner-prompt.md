You are test-running the "first-clients" Claude skill so its author can improve it. Follow the skill exactly as written, as if a founder had just invoked it. Don't improve on it or skip steps it asks for; when it is vague, make the choice a typical model would and NOTE it.

SKILL FILE: {SKILL}   (its references/ and scripts/ folders are next to it)
PERSONA FILE: {PERSONA}
MODE TO TEST: {MODE}   (e.g. "Plan, Full", "Plan, Quick", "Review", "Targets", "Launch kit", "Export: xlsx,pptx,docx")
OUTPUT DIR: {OUT}

Rules:
- The persona file describes the product and the founder. If it points to a repository or URL, study it, but NEVER modify it. Otherwise treat the product description as everything discovery can find.
- Write the skill's `marketing/` folder to {OUT}/marketing/ (and any exports to {OUT}/marketing/exports/). Don't publish artifacts or docs.
- You cannot ask the real user. Whenever the skill tells you to ask or show the founder something, log it in {OUT}/interview-log.md and answer ONLY from the persona. If the persona doesn't cover it, write "founder doesn't know" and proceed with a flagged assumption.
- Do real web research. Cite sources. Do not invent facts.
- If the mode involves exports and the skill's exporter needs libraries, install them only into {OUT}/../fc-export (create it if missing; reuse it if it exists).

At the end write {OUT}/run-notes.md with:
1. Per phase/step: what you did, and roughly how much effort it took.
2. Every place the instructions were ambiguous, contradictory, missing something, didn't fit this product, or made you produce low-value filler.
3. What you had to guess.
4. Scores against evals/rubric.md (if provided at {RUBRIC}), and your honest overall rating 1–10 of how useful the result is to this founder, plus the 3 biggest weaknesses.

Final reply: under 200 words: paths written, the rating, and the top 3 skill problems.
