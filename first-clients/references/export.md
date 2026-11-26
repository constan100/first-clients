# Export mode: the plan as Excel, PowerPoint, Word, PDF, Markdown or CSV

Use when the founder asks for the plan in a file format, or says yes to the export offer. The source of truth is always `marketing/plan-data.json`; every format is generated from it, so they all say the same thing.

## 1. Ask which formats (one line, if they didn't say)
"Which formats do you want? Excel (task tracker + weekly numbers), PowerPoint (to present the plan), Word (to print or share), PDF, Markdown, CSV." Suggest based on use:
- **Excel (`xlsx`)**: to work from: tick tasks (status drop-down, done rows turn green), hours planned vs. done per week, a weekly numbers tracker for 13 weeks, blockers, channels, if/then rules.
- **PowerPoint (`pptx`)**: ~10 clean slides: title, bet & goal, this week, blockers, channels, one slide per week, if/then, metrics.
- **Word (`docx`)**: the full plan as a document with checkboxes and tables.
- **PDF**: same as Word (converted with LibreOffice if installed; otherwise a print-ready HTML to "Save as PDF").
- **Markdown (`md`)**, **HTML**, **CSV** (tasks only, opens in any spreadsheet or task tool).

## 2. Make sure `plan-data.json` is current
If it's missing or older than `PLAN.md`, write it from `PLAN.md` and `strategy.md` using the schema below (start from `references/plan-data.example.json`). Then validate:
`node <skill-dir>/scripts/export.cjs --check marketing/plan-data.json`
Fix every `error`; read the `warning`s (e.g. a week planned over the founder's hours) and fix the plan if they're real.

## 3. Run the exporter (preferred: same look every time)
Requires Node.js 18+. Markdown, HTML and CSV need nothing else. For Excel, PowerPoint and Word, install the three libraries once into a temporary folder (not the founder's project):

```bash
npm install --no-save --no-audit --no-fund --prefix "<tmp>/fc-export" docx@9.15.3 pptxgenjs@4.0.1 exceljs@4.4.0
FC_EXPORT_MODULES="<tmp>/fc-export/node_modules" node <skill-dir>/scripts/export.cjs marketing/plan-data.json --formats xlsx,pptx,docx --out marketing/exports
```
(PowerShell: `$env:FC_EXPORT_MODULES="<tmp>\fc-export\node_modules"; node <skill-dir>\scripts\export.cjs ...`.) `<tmp>` is the session's temporary or scratch folder; `<skill-dir>` is the folder this skill is installed in. Use `--formats all` for everything. Files land in `marketing/exports/` as `<product>-plan.<ext>`.

**If Node or npm isn't available** (or installing isn't allowed): use the platform's own document skills or tools for Word, PowerPoint, Excel or PDF if it has them, building the file from `plan-data.json` with the same sections and order as the exporter (summary, this week, blockers, weeks, if/then, channels, metrics). As a last resort, give Markdown, CSV and HTML, which need no libraries (run the script for those formats only, or write them by hand), and say which formats couldn't be made and why.

## 4. Check and hand over
- Confirm each file was written (the script prints `wrote …`) and is not empty. If the platform can render or preview files, glance at the PowerPoint and Excel output.
- Tell the founder where the files are, in one line each with what it's for. Re-run the export after every weekly review so the files stay current (Review mode offers this).
- Exports may contain the plan's numbers; `targets.md` is never exported (personal data).

## `plan-data.json` schema (`first-clients/plan@1`)
Only `product`, `bet` and `weeks` (with `action` text) are required; include everything you have. `capacity` on a week (optional) is the hours the founder agreed to for that week, e.g. a launch week; otherwise `hours_per_week` applies. `results` (optional, appended by each weekly review) are the numbers logged per check-in; `values` keys must match `metrics[].name`. `hours_done` (optional) records real time spent on an action. `checklists` (optional) hold lists that aren't weekly actions: a launch readiness list, a launch-day run sheet (use `when` for the time and `value` for numbers like "+3h: 24 points"), a validation scorecard. `language` (`en` or `fr`) sets the labels; other languages: pass translated `labels` (same keys as `LABELS.en` in the script) or use `en`.

```json
{
  "schema": "first-clients/plan@1",
  "product": "Name",
  "created": "YYYY-MM-DD",
  "language": "en",
  "founder": { "hours_per_week": 4, "budget": "€0" },
  "bet": "One sentence: who, where, why it should work.",
  "one_liner": "[Product] helps [ICP] [outcome] without [pain].",
  "goal": { "day30": "…", "floor90": "…", "target90": "…", "north_star": "…", "threshold": "…" },
  "blockers": [ { "blocker": "…", "fix": "…", "hours": 0.5, "status": "todo" } ],
  "channels": [ { "name": "…", "role": "primary | experiment | supporting | one-off | dropped", "score": 20, "why": "…" } ],
  "weeks": [
    { "week": 1, "start": "YYYY-MM-DD", "end": "YYYY-MM-DD", "theme": "…", "capacity": 4,
      "actions": [ { "id": "1.1", "action": "…", "channel": "…", "hours": 1, "output": "…", "done_when": "…",
                     "asset": "assets/outreach.md", "top3": true,
                     "status": "todo | doing | partial | done | moved | skipped", "hours_done": 0.5, "note": "…" } ] }
  ],
  "results": [ { "date": "YYYY-MM-DD", "values": { "<metric name>": 6 }, "note": "…" } ],
  "checklists": [ { "title": "Launch readiness", "items": [ { "when": "Mon 14 Dec", "item": "…", "status": "todo", "value": "" } ] } ],
  "if_then": [ { "if": "…", "then": "…" } ],
  "metrics": [ { "name": "…", "type": "north_star | supporting", "source": "where to read it", "baseline": 0 } ],
  "review": { "day": "Sunday", "minutes": 15 },
  "sources": [ { "title": "…", "url": "https://…" } ]
}
```
A complete example of the format ships with the skill: `references/plan-data.example.json` (a fictional café-rota app: copy the structure, never the content). A real run is in the repository's `examples/` folder. `goal.threshold` (optional) holds a launch or experiment threshold, e.g. "+40 stars and 5 feedback runs in launch week".
