<div align="center">

# 🚀 First Clients

### A Claude skill that turns your product into a client-acquisition plan

**Built for solo developers and indie makers who can build great products, but don't know how to find the people who'll pay for them.**

![Claude Skill](https://img.shields.io/badge/Claude-Skill-D97757?style=for-the-badge)
![For Solo Devs](https://img.shields.io/badge/For-Solo%20Devs-4F46E5?style=for-the-badge)
![Digital + Physical](https://img.shields.io/badge/Products-Digital%20%2B%20Physical-10B981?style=for-the-badge)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

**[See a real run](examples/first-clients-on-itself/PLAN.md)** · **[Install in 1 minute](#️-installation)** · **[Tell me how it went](https://github.com/constan100/first-clients/issues/new?template=i-ran-it.yml)**

</div>

---

## 🤔 The problem

You shipped the product. It works. And then... silence.

Most marketing advice is written for companies with a team, a budget and months to spare. You have **one person, a few hours a week, and very little money**.

**First Clients** is a marketing strategist built for that situation. It studies your actual product, asks you the right questions, researches your market, and gives you a **realistic 30-day plan with ready-to-use content**.

---

## ✨ What makes it different

| Generic marketing advice | First Clients |
|---|---|
| "Describe your product..." | **Reads your code**, visits your live site, looks at your photos |
| 50 generic questions | Only asks what it **couldn't figure out alone** |
| "Use social media" | Names the **exact subreddits, groups, shops and creators** |
| Plans for a 10-person team | Plans sized to **your hours and your budget** |
| Theory and frameworks | **Ready-to-send** emails, posts, landing copy, listings |
| Starts from zero every time | Saves a `marketing/` folder and **builds on it next session** |

---

## 🗺️ How it works

```mermaid
flowchart LR
    A[🔍 Discover<br/>code · site · photos] --> B[💬 Interview<br/>only what's missing]
    B --> C[🌍 Research<br/>competitors · communities]
    C --> D[✅ Readiness<br/>score + fixes]
    D --> E[🎯 Position<br/>ICP · one-liner · pricing]
    E --> F[📡 Channels<br/>pick 2 + 1 test]
    F --> G[📅 30-day plan<br/>+ ready assets]
    G --> H[📈 Track<br/>& iterate]
    H -.next session.-> B

    style A fill:#EEF2FF,stroke:#4F46E5
    style E fill:#FEF3C7,stroke:#D97706
    style G fill:#D1FAE5,stroke:#10B981
```

| Step | What happens | You get |
|---|---|---|
| **1. Discover** | Scans your repo (README, routes, models, pricing, SEO, analytics), audits your live site like a first-time visitor, and reviews your photos | A draft product profile |
| **2. Interview** | Asks 3–4 questions at a time: your customer, goals, **hours per week, budget**, and what you're comfortable doing | A plan that fits *you* |
| **3. Research** | Finds real competitors, mines their reviews for complaints, and finds where your customers hang out | Sourced market insights |
| **4. Readiness** | Rates how ready you are to market (0–10) and lists quick fixes with dev-hour estimates | A pre-launch fix list |
| **5. Position** | Defines your ideal customer, turns features into benefits, writes your one-liner, suggests pricing | Clear messaging |
| **6. Channels** | Scores channels on speed, cost, time, fit and your strengths, then commits to the best 2 | Focus instead of noise |
| **7. Plan + assets** | A week-by-week plan, plus copy you can use right away | Things you can send today |
| **8. Track** | Metrics, analytics setup, and a weekly review | A loop that improves |

---

## 📦 What you get at the end

**One page you can follow:** `marketing/PLAN.md`. The bet, your goal, the 3 things to do this week, a checklist for weeks 2–4, and what to do if things don't work. You can read it in 2 minutes.

```markdown
## Do this week (26 Nov – 2 Dec)
- [ ] 1. Fix the install line and test a fresh install (1h15)
- [ ] 2. Publish a sample run and link it at the top of the README (1h30)
- [ ] 3. Send the 5 drafted messages in assets/outreach.md (1h)
```

**In the format you want:** ask for it as an **Excel tracker** (tick tasks, log weekly numbers, hours per week), a **PowerPoint** (to show a partner), a **Word** document or **PDF**, **Markdown** or **CSV**. See a real example in [`examples/`](examples/).

Behind that page, everything it's based on:

```mermaid
mindmap
  root((First Clients))
    Strategy
      Positioning & one-liner
      Ideal customer profile
      Pricing & break-even
      Channel scorecard
    Action plan
      30-day week-by-week plan
      Top 3 actions this week
      Days 31–90 roadmap
    Ready-to-use assets
      Landing page copy
      Cold outreach + follow-ups
      Product Hunt / HN / Reddit posts
      Content calendar
      Directory list
    Tracking
      North-star metric
      Analytics events
      Weekly review ritual
```

Everything is saved in your repo, so the next session starts where you left off:

```
marketing/
├── product-profile.md   # what it is, features → benefits, readiness score
├── icp.md               # ideal customer, where they hang out, amplifiers
├── targets.md           # first people to contact, with links (keep private)
├── competitors.md       # competitor table, complaint themes, sources
├── strategy.md          # goal check, positioning, pricing, channel scores
├── PLAN.md              # the one-page plan you follow each week
├── plan-data.json       # the same plan as data (feeds the exports)
├── exports/             # Excel, PowerPoint, Word, PDF versions
├── unit-economics.md    # physical products: cost per unit, margin, max CAC
├── results.md           # your numbers and learnings, session after session
└── assets/              # only what your plan uses: front-door copy, outreach,
                         # launch posts, listings, emails…
```

Want to share the full reasoning with a partner or cofounder? Ask for the **strategy document** too.

---

## 🧰 More than a plan: 9 modes

Just say what you need. The skill picks the right mode.

| You say… | Mode | What you get |
|---|---|---|
| "Help me find my first clients" | 🗺️ **Plan** | The one-page 30-day plan (Quick or Full) |
| "Here are my numbers this week" | 📈 **Weekly review** | What worked, what to drop, this week's 3 actions, updated tracker |
| "Find me more people to contact" | 🎯 **Targets** | 10 real people who fit, with links and a drafted message each |
| "I only have an idea" | 🧪 **Validate** | Interview script, smoke test, and a go / change / stop decision |
| "I'm launching on Product Hunt / HN" | 🚀 **Launch kit** | Rules check, date, checklist, all the posts, launch-day run sheet |
| "Fix the blockers" | 🔧 **Fix** | The week-1 fixes applied in your code (diff shown, nothing pushed) |
| "Here's what users told me" | 💬 **Feedback** | Themes, decisions, customer language, testimonial candidates |
| "Write my onboarding emails" | ✉️ **Emails** | A welcome → activation → review → win-back sequence |
| "Export it to Excel / PowerPoint / Word" | 📤 **Export** | The plan in the formats you choose |

---

## 📡 Example: how it picks channels

The skill doesn't tell you to be everywhere. It scores each channel and picks the ones with the **fastest path to a first client for the least effort**:

```mermaid
quadrantChart
    title Example channel scoring (solo dev, 5h/week, €0 budget)
    x-axis Low effort --> High effort
    y-axis Slow results --> Fast results
    quadrant-1 Worth it if you have time
    quadrant-2 Do these first
    quadrant-3 Later
    quadrant-4 Avoid for now
    Direct outreach: [0.35, 0.85]
    Niche communities: [0.3, 0.7]
    Product Hunt launch: [0.55, 0.65]
    Directories: [0.15, 0.4]
    SEO articles: [0.7, 0.2]
    Paid ads: [0.6, 0.55]
    Build in public: [0.5, 0.35]
```

*This is an illustration. Your chart depends on your product, time, budget and strengths.*

---

## 🧩 Works with many kinds of products

| Product type | Fit | What it focuses on |
|---|:---:|---|
| 💼 **B2B SaaS** | ⭐⭐⭐ | Precise ideal customer, LinkedIn + email outreach, demos, case studies |
| 📱 **B2C apps** | ⭐⭐⭐ | Communities, short-form content, app store optimization, referrals, local partners |
| 🛠️ **Developer tools** | ⭐⭐⭐ | Docs as marketing, GitHub, Show HN, dev communities, free tier |
| 🌱 **Open source / free tools** | ⭐⭐⭐ | Installs, real usage and feedback (not just stars), README as landing page, sample output, awesome lists |
| 🔄 **Marketplaces** | ⭐⭐⭐ | Win one side first, go hyper-local or niche |
| 🧑‍💻 **Freelance services** | ⭐⭐⭐ | Niche, portfolio, referrals, Malt/Upwork, productized offers |
| 🔌 **Hardware / electronics** | ⭐⭐ | Video demos, tech reviewers, crowdfunding, compliance |
| 👕 **Consumer goods** | ⭐⭐ | Photos, Instagram/TikTok, influencer seeding, Etsy, local shops |
| 🎨 **Handmade / artisan** | ⭐⭐ | Etsy, markets, founder story, limited editions |
| 🎮 **Indie games** | ⭐⭐ | Steam wishlists, demos, store festivals, streamers, short clips |

### Physical products get their own track

When there's no code to read, the skill switches to a physical-product mode:

- 📸 **Photo audit**: online, your photos *are* your product
- 💶 **Unit economics**: cost per order, margin, the most you can spend to win a customer, break-even
- 🏪 **Physical channels**: your own store vs. Amazon/Etsy, pre-orders, crowdfunding, influencer seeding, local shops, fairs, wholesale
- 📋 **Compliance flags**: CE marking, product safety, labeling, return rights (to verify with an official source)
- 🛡️ **No big batches before demand is proven**: pre-orders and small runs come first

---

## ⚙️ Installation

### Claude Code
macOS / Linux:
```bash
git clone https://github.com/constan100/first-clients.git
mkdir -p ~/.claude/skills
cp -r first-clients/first-clients ~/.claude/skills/
```
Windows (PowerShell):
```powershell
git clone https://github.com/constan100/first-clients.git
New-Item -ItemType Directory -Force "$HOME\.claude\skills" | Out-Null
Copy-Item -Recurse first-clients\first-clients "$HOME\.claude\skills\"
```
Check it worked: start a new Claude Code session and type `/first-clients`. To use it in one project only, copy the folder into that project's `.claude/skills/` instead.

### Claude.ai / Claude desktop app
1. Skills need code execution turned on (in Settings, under Capabilities; on Team/Enterprise plans an admin enables it).
2. Make a zip with the `first-clients/` folder at its top level (the zip must contain `first-clients/SKILL.md`, not a loose `SKILL.md`). GitHub's "Download ZIP" adds an extra parent folder, so don't upload that directly. After cloning (see above):
   - macOS / Linux: `cd first-clients && zip -r ../first-clients.zip first-clients -x "*/node_modules/*"`
   - Windows 10/11: `cd first-clients; tar -a -c -f ..\first-clients.zip first-clients` (the built-in `tar` writes the standard paths a zip needs)
3. Upload the zip in Claude's **Skills** settings (Customize > Skills in recent versions, Settings > Capabilities in older ones).
4. Make sure the skill is turned on, then ask: *"Help me find my first users for this product."*

### Exports (optional)
Markdown, CSV and printable HTML work everywhere. Excel, PowerPoint and Word need **Node.js 18+**; the skill installs three small libraries (`docx`, `pptxgenjs`, `exceljs`) into a temporary folder the first time you ask. Direct PDF uses LibreOffice if you have it; otherwise you get a print-ready page to "Save as PDF".

---

## 💬 How to use it

Just ask Claude in plain words:

> *"Help me find my first clients for this app."*
> *"Build a marketing strategy for my product. Here's the repo and the live URL."*
> *"I make handmade leather wallets. How do I start selling them?"*
> *"Weekly check-in: 6 new stars, 2 replies, I had 3 hours. What now?"*
> *"Give me the plan as an Excel tracker and a PowerPoint."*

Or call it directly:

```
/first-clients
```

**Tips for the best results**
- 📁 Give Claude access to your **project folder** so it can read the code
- 🌐 Share your **live URL**
- 🖼️ Attach **screenshots or product photos**
- ⏱️ Be honest about your **hours per week and budget**. The plan depends on it.

### Two depths for the plan

| ⚡ Quick | 🧠 Full |
|---|---|
| Product scan + blockers | Everything in Quick, plus: |
| Positioning one-liner | Competitor, community & benchmark research |
| 2 channels | Real first people to contact, with drafted messages |
| 5 actions for this week | Goal reality check, pricing / unit economics |
| | Dated 30-day plan + assets + tracking |

---

## 🛡️ Built-in guardrails

- ✅ **Honest:** if your product isn't ready or the market looks weak, it says so
- ✅ **No invented data:** no fake stats, reviews or testimonials; it uses placeholders instead
- ✅ **Ethical tactics only:** no spam, no fake accounts, no undisclosed self-promotion, GDPR-friendly
- ✅ **Respects community rules,** so you don't get banned from the places where your users are
- ✅ **Never acts without you:** it drafts, and you decide what gets posted, sent or paid for

---

## ❓ FAQ

<details>
<summary><b>Do I need to be a marketer to use it?</b></summary>

No. It's made for developers. It explains things simply and gives you ready-made content instead of theory.
</details>

<details>
<summary><b>Does it work without code access?</b></summary>

Yes. It falls back on your live site, photos, specs and answers. Code access just makes it sharper for software.
</details>

<details>
<summary><b>Will it post or send things for me?</b></summary>

No. It drafts everything and you stay in control. Nothing is posted, sent or bought without your approval.
</details>

<details>
<summary><b>Does it work in other languages?</b></summary>

Yes. Customer-facing content is written in your target market's language, and the strategy in the language you use with Claude.
</details>

<details>
<summary><b>Can I use it more than once?</b></summary>

Yes, and you should. Come back with your numbers each week. It reads the `marketing/` folder and adjusts the plan.
</details>

<details>
<summary><b>Can I get the plan in Excel, PowerPoint or Word?</b></summary>

Yes. Ask for any of them (or PDF, Markdown, CSV). The Excel file is a working tracker: tick tasks, log your weekly numbers, see hours planned vs. done. Re-export after each weekly review so it stays up to date.
</details>

---

## 🛣️ Roadmap

- [x] Dedicated playbook for indie games (wishlists, streamers, festivals)
- [x] Weekly review mode with automatic plan adjustments
- [x] Email sequence templates for onboarding and retention
- [x] Export to Excel, PowerPoint, Word, PDF, Markdown, CSV
- [x] A first real example ([`examples/`](examples/))
- [ ] More examples for SaaS, physical products and games
- [ ] More languages for exports (English and French today)

## 🧪 Contributing

Changed the skill? Test it first with [`evals/`](evals/): founder profiles for different products, a runner prompt and a 12-point scoring rubric. Ideas and PRs are welcome. Open an issue!

---

## 📄 License

MIT. Use it, fork it, improve it.

<div align="center">

**Built by a solo developer, for solo developers.** ⭐ Star the repo if it helped you land your first clients!

</div>
