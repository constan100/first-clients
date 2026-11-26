# Evals: test the skill before you ship a change

The skill is a set of instructions, so the only real test is to run it and look at what it produces. This folder makes that repeatable.

## What's here
- `personas/`: founder profiles covering different products: the skill itself (open source), a B2B SaaS, handmade candles (physical), an indie game.
- `runner-prompt.md`: the prompt that makes a fresh Claude session follow the skill exactly, answer interview questions from a persona, and write honest run notes.
- `rubric.md`: 12 criteria scored 0–2 (max 24).

## Run one eval
In Claude Code, from the repo root, ask:

> Spawn a fresh agent with the prompt in `evals/runner-prompt.md`, using SKILL = `first-clients/SKILL.md`, PERSONA = `evals/personas/b2b-saas.md`, MODE = "Plan, Full", RUBRIC = `evals/rubric.md`, OUT = a new folder in your scratchpad.

A fresh agent matters: the session that edited the skill knows what it meant, a new one only knows what it says.

## Suggested routine after every change
1. Run 2 personas that the change touches (Full mode), plus 1 other mode (Review, Targets, Launch kit or Export).
2. Compare the rubric total with the last run, and read `run-notes.md` section 2 (where the instructions were unclear).
3. Fix the skill, then re-run the worst one.

## Checking exports quickly
```bash
node first-clients/scripts/export.cjs --check examples/first-clients-on-itself/plan-data.json
```

Keep run outputs out of git (they contain research about real people). Only cleaned-up examples belong in `examples/`.
