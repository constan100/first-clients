# Fix mode: apply the blockers in the code

Use when the founder asks to fix the blockers found in the plan, apply the front-door copy, or set up tracking. Goal: the week-1 blockers fixed in their codebase, in small reviewable changes, with nothing committed or deployed without their say-so.

## 1. Pick what to fix
Read the blocker list in `product-profile.md`. If there's no `marketing/` folder yet, run a quick Phase 1 (front door, path to first value, public vs. local) and write the blockers to `marketing/product-profile.md` first.

Some blockers can't be fixed by editing files; list them as **founder to-dos** with the exact command or link:
- **Public behind local** (unpushed commits, uncommitted work, undeployed site): give the commands to commit and push or deploy everything that belongs together (e.g. a README that links to folders that aren't pushed yet). Never commit, push or deploy yourself unless asked.
- Repo settings (description, topics, Discussions): a ready `gh repo edit …` command or the settings link.
- Accounts, payments, domains, store listings. Confirm the list with the founder in one message: what you'll change, file by file, and anything you won't touch. Fix in order of impact on the first client.

## 2. Work safely
- Check `git status` first. If there are uncommitted changes, ask before touching those files. Suggest a branch (`marketing-fixes`) for the changes.
- One blocker = one small change. Show the diff after each, or all at the end in one summary.
- Match the project's existing style, framework and language. Don't add dependencies without asking (prefer what's already installed).
- Never commit, push, deploy, publish, or change production settings unless the founder asks. Never put real keys or secrets in code; use environment variables and say which to set.
- Test what you can: run the build, the tests, or open the page locally. Say plainly what you couldn't test.
- **Install instructions** (CLIs, packages, plugins, skills): test them literally in a temporary folder (fresh clone, empty target directory, the exact commands from the README, on the founder's OS and shell). Missing parent folders, placeholders and OS-specific commands are the usual failures; give Windows (PowerShell) and macOS/Linux versions when they differ.
- **Platform facts change** (settings menu names, upload limits, store rules): check the platform's current docs before writing them, cite them, and when a UI was recently renamed, name both ("Settings > Skills, or Customize > Skills in newer versions").

## 3. Common fixes and how to do them
- **Front door copy:** replace the headline, subheadline, benefits and primary action with the approved copy from `assets/`; keep the design.
- **SEO and sharing basics:** a page `<title>` and meta description per page, Open Graph and Twitter card tags, an OG image (note if the founder must make one), `sitemap.xml`, `robots.txt`.
- **Analytics:** add the tool the founder chose (privacy-friendly ones like Plausible or Umami avoid cookie banners in many cases; check), plus events for the funnel steps in `strategy.md` (signup, activation, payment). Don't add a cookie banner the tool doesn't need, but flag EU consent rules.
- **Feedback and contact path:** a feedback link or form, a contact email, or for repos a GitHub issue template and Discussions.
- **"Where did you hear about us?"** in signup or onboarding.
- **Repos, packages and skills:** fix the install command and placeholders, add repo description and topics (give the founder the `gh repo edit` command or settings link; you can't change them by editing files), add an `examples/` folder link near the top of the README, add a license if missing.
- **Payments:** if there's no way to pay, suggest the simplest option for their stack (a payment link) and wire the button; the founder creates the account.
- **Legal pages:** flag what's missing (privacy policy, terms, legal notice for EU businesses); you can draft placeholders clearly marked for review, not legal advice.

## 4. Wrap up
List what changed (file: what), what the founder must do (create an account, set an env var, upload an image, merge and deploy), and update the blocker list in `product-profile.md` and the checkboxes in `PLAN.md`/`plan-data.json`.
