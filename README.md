# fstack

**A founder's operating system — built on Garry Tan's gstack principles and EOS/Traction, adapted for content ops founders running lean with small teams and real runway pressure.**

*fstack = founder stack. Or Fleire's stack. Depends who's asking.*

Inspired by [Garry Tan's gstack](https://github.com/garrytan/gstack) and Y Combinator's core operating philosophy. Adapted for founders who are:
- Running a content ops, marketing services, or SaaS business
- Working with a small team (1-5 people)
- Trying to reach default alive before runway runs out
- The sole decision-maker across product, sales, and operations

MIT License. Fork it. Make it yours. Don't player hate, appreciate.

---

## Why This Exists

Garry Tan runs YC. He's worked with thousands of companies — Coinbase, Instacart, Rippling — from one or two founders in a garage to companies worth tens of billions. He built gstack to turn Claude Code into a virtual engineering team of twenty.

This is gstack's spiritual cousin — for the founder who doesn't have an engineering team yet. Or a sales team. Or a marketing team. Just themselves, a small crew, and a clock ticking on runway.

The insight is the same: **AI makes the marginal cost of rigor near-zero.** You might as well run every decision through a senior advisor, a paranoid reviewer, and a skeptical investor before you spend a week on the wrong thing.

---

## The YC DNA Underneath

Every skill in fstack is grounded in Y Combinator's core operating principles. These aren't motivational quotes — they're forcing functions built into each review:

### "Make something people want"
The most common founder failure: building something technically impressive that nobody actually needs. Every `/office-hours` review starts here — not with the feature, but with the pain. What specific moment made a real user ask for this?

### "Talk to users"
You can't run `/ceo-review` without evidence from a real user conversation. Opinions don't qualify. "I think people want this" doesn't qualify. A specific sentence from a real client does.

### "Do things that don't scale"
The sprint system starts with the smallest test that proves the thesis — not the polished version, not the platform play. Ship the thing you can do manually first. `/office-hours` always asks: "What's the version we could test in one week with no code?"

### "Default alive"
Paul Graham's framework: are you on a path to profitability before you run out of money, or not? The Revenue Gate in every skill operationalizes this. Every task gets bucketed: does it close a client, retain a client, reduce burn, or none of the above? Tasks in the "none" bucket don't get worked on until you're default alive.

### "Ramen profitable"
The goal isn't hypergrowth. It's surviving long enough to find product-market fit. The `/retro` skill tracks this weekly: MRR change, burn change, client health. Navigation instrument, not performance review.

### "Boil the Lake" (Garry Tan)
Garry's principle: *when AI makes the marginal cost of completeness near-zero, do the complete thing.* A lake is boilable — full test coverage for a module, full feature implementation, all edge cases. An ocean is not — rewriting the entire system. Boil lakes. Flag oceans as out of scope. See: [garryslist.org/posts/boil-the-ocean](https://garryslist.org/posts/boil-the-ocean)

For content ops founders, the lake is: standardize delivery for your best client. The ocean is: build a platform that replaces all content agencies globally. Boil the lake first.

### "The best client IS the product"
Your highest-margin, lowest-friction, happiest client is not a success story. They are your product specification. Everything you build should be an attempt to replicate what's working for them at scale.

---

## The Virtual Team

fstack turns your AI assistant into a virtual operating team you actually manage:

| Role | Skill | What it catches |
|------|-------|-----------------|
| YC Advisor | `/office-hours` | Wrong problem, wrong framing |
| CEO/Founder | `/ceo-review` | Wrong scope, wrong product decision |
| CTO | `/eng-review` | Wrong architecture, hidden technical debt |
| UX Lead | `/ux-review` | Client friction, AI slop, confusing flows |
| Release Manager | `/ship` | Deployment risks, client-breaking changes |
| COO | `/retro` | What slipped this week and why |
| GTM Lead | `/gtm-review` | Wrong campaign, wrong message, wrong target |
| EOS Integrator | `/l10` | Monday clarity — rocks, scorecard, issues resolved |
| Content Director | `/brief-review` | Brief quality gate + AI output review before publish |
| **Growth Team** | | |
| Growth Strategist | `/positioning-workshop` | Wrong positioning, wrong message |
| Experiment Lead | `/experiment-designer` | Vibe-based shipping, no kill criteria |
| Growth Analyst | `/cohort-review` | Vanity metrics, leaky buckets |
| Launch Coordinator | `/launch-orchestrator` | Uncoordinated launches |
| User Research Lead | `/customer-interview-synthesizer` | Building for imaginary users |
| Growth Engineer | `/virality-loop-designer` | No referral loops |
| Content Strategist | `/seo-content-system` | One-off posts, no compounding |
| Growth Loop | `/growth-sprint` | Running growth phases in isolation |

---

## The Three Core Principles

These are fstack's versions of Garry's "Boil the Lake" — calibrated for founders with limited runway and small teams.

### 1. The Best Client Test
*(adapted from YC's "make something people want")*

Before any feature, offer, or campaign:
> **"Would your best client pay for this outcome in their first 7 days?"**

Your best client is not who you wish your clients were. It's your highest-margin, lowest-friction, most successful account right now. They are your product-market fit signal. Build toward them, not away from them.

### 2. The Maintainability Check
*(adapted from "do things that don't scale" + bus factor reality)*

Before any code ships:
> **"Can your smallest team member maintain this alone in 6 months without documentation?"**

On a small team, bus factor = 1. Design for that reality. Something only the founder understands is a liability, not an asset.

### 3. The Revenue Gate
*(adapted from YC's "default alive" framework)*

Every task, feature, or campaign gets bucketed:
- **A: Closes a client within 30 days**
- **B: Retains an existing client**
- **C: Reduces burn**
- **D: Everything else**

D doesn't get worked on until you're default alive. This isn't pessimism — it's the discipline that keeps the lights on long enough to find PMF.

---

## The Skills

### `/office-hours`
Challenge the idea before you build it. Reframes the problem, challenges 3 premises, generates 3 approaches (smallest test, best client path, scalable path). Recommends the narrowest wedge to prove the thesis.

*YC equivalent: "Talk to users first. Build second."*

### `/ceo-review`
Pressure-test any feature or product decision before your team spends time on it. Applies Best Client Test, Maintainability Check, and Revenue Gate.

*YC equivalent: "Is this the right thing to build right now?"*

### `/eng-review`
Architecture and safety review before code ships. Simulates the missing senior engineer. Catches technical debt, security gaps, and maintainability issues.

*Garry equivalent: gstack's `/plan-eng-review` — ASCII diagrams, failure modes, security concerns.*

### `/ux-review`
UX review from the perspective of a first-time, mildly-stressed client. Catches friction, confusion, and AI slop before real clients see it.

*Garry equivalent: gstack's `/design-review` — catching the gap between "it works" and "a real user would use this."*

### `/ship`
Release ritual. Makes every deployment documented, reversible, and client-safe.

*Garry equivalent: gstack's `/ship` — tests, PR, changelog, post-ship monitoring.*

### `/retro`
Weekly visibility on team output, client delivery health, and founder decisions. Navigation instrument, not performance review.

*Garry equivalent: gstack's `/retro` — lines added, commits, coverage trend.*

### `/gtm-review`
Pressure-test any GTM initiative. Applies Best Client Test and Revenue Gate to campaigns and outreach. Flags wrong message, wrong target, wrong channel.

*No gstack equivalent — GTM is the founder's job.*

### `/brief-review`
Two-mode content quality gate. **Before production:** reviews the brief for audience clarity, outcome clarity, voice, constraints, and success criteria. **After production:** reviews AI output for generic language, brand voice, specificity, CTA, and the "would your best client publish this?" test. Includes a red-flag phrase list and rewrite capability.

*The skill that makes you unfireable. If it could have been written by anyone, rewrite it.*

### `/sprint-plan`
Plan a sprint for your team against one clear goal. Every task gets filtered through the three principles before it gets assigned.

*YC equivalent: "What's the one thing you're shipping this week?"*

### `/l10`
Monday clarity check — a founder-adapted Level 10 meeting based on EOS/Traction by Gino Wickman. Covers scorecard, Rock review, headlines, last week's To-Dos, and IDS (Identify, Discuss, Solve). Same agenda every Monday. Produces a To-Do list with owners and due dates before you open Slack.

*EOS principle: "Rocks, not sand. Put the big stones in first."*
*Garry Tan equivalent: making invisible work visible — `/review` resolves issues with finality.*

### `/positioning-workshop`
Fast structured positioning session using April Dunford's JTBD framework. Produces 3 ranked positioning options, a competitor 2x2 matrix, and a Revenue Gate recommendation. Kills positions that fail the Best Client Test and suggests pivots.

*"If you can't explain why someone would switch to you in one sentence, you don't have positioning — you have a wishlist."*

### `/experiment-designer`
Designs rigorous low-risk growth experiments. Forces a written hypothesis, primary and guardrail metrics, and a kill criterion before anything launches. Outputs a Notion/Airtable experiment template.

*"Every campaign without a kill criterion is a hobby."*

### `/cohort-review`
Analyzes cohort and segment data to find growth truth. Runs the default alive check first. Identifies profitable cohorts (LTV:CAC > 3x), leaky buckets, and the highest-leverage segment or channel right now.

*"Vanity metrics are comfort food. Cohort data is the blood test."*

### `/launch-orchestrator`
Builds and sequences a realistic launch campaign (-7 days to +3 days). Includes copy variants for Product Hunt, X, and LinkedIn, a 50-account seeding list template, and a "Would Garry RT this?" hook filter.

*"A launch without coordination is just noise with a countdown."*

### `/customer-interview-synthesizer`
Distills raw user call notes and transcripts into Jobs-to-be-Done, objection patterns, and updated best client persona. Flags if you're talking to the wrong segment before you build anything.

*"Talking to users without synthesizing is just expensive small talk."*

### `/virality-loop-designer`
Diagnoses current viral coefficient and designs 3 concrete referral/viral loop options. Each loop includes incentive copy, success metric, implementation effort, and a Best Client Test filter.

*"If your users aren't bringing you more users, you have a product — not a growth engine."*

### `/seo-content-system`
Turns any topic into a full SEO content cluster — pillar page + 2–3 cluster articles + internal linking plan. Includes an EEAT check and a "would your best client share this?" filter before publishing.

*"One blog post is a lottery ticket. A content system is a compounding asset."*

### `/growth-sprint`
Orchestrates the full growth loop across all fstack growth skills. Run at the start of any new growth push or quarterly reset. Chains: `/customer-interview-synthesizer` → `/positioning-workshop` → `/experiment-designer` → `/launch-orchestrator` → `/cohort-review` → `/retro`.

*"Growth isn't a department. It's a loop."*

---

## Skill Chaining

### Core operating loop (weekly)
```
/sprint-plan → /ceo-review → /eng-review → /ux-review → /ship → /retro → /l10
```

### Growth loop (4-week cycle)
```
/customer-interview-synthesizer
        ↓
/positioning-workshop
        ↓
/experiment-designer
        ↓
/launch-orchestrator
        ↓
/cohort-review
        ↓
/retro ──────→ back to /customer-interview-synthesizer
```

Run `/growth-sprint` to orchestrate the entire cycle automatically.

### Content loop (per piece)
```
/office-hours → /brief-review (MODE 1) → [produce] → /brief-review (MODE 2) → /gtm-review → publish
```

---

## Installation (Claude Code)

```bash
# Clone fstack into your Claude Code skills directory
git clone https://github.com/likke/fstack.git ~/.claude/skills/fstack

# Or add to a specific project so teammates get it
cp -Rf ~/.claude/skills/fstack .claude/skills/fstack && rm -rf .claude/skills/fstack/.git
```

Then add to your project's `CLAUDE.md`:
```
## fstack skills
Available skills: /office-hours, /ceo-review, /eng-review, /ux-review, /ship, /retro, 
/gtm-review, /brief-review, /sprint-plan, /l10, /positioning-workshop, /experiment-designer, 
/cohort-review, /launch-orchestrator, /customer-interview-synthesizer, /virality-loop-designer, 
/seo-content-system, /growth-sprint
```

---

## The Sprint Rhythm

*(Inspired by EOS Traction + YC's weekly check-in culture)*

| When | What |
|------|------|
| Monday morning | Weekly CEO brief — priorities, health, one thing |
| Monday (L10 / team sync) | Scorecard, issues, rocks — max 90 min |
| Monday post-sync | Team gets sprint tasks |
| Friday | Quick async retro — did we ship? any blockers? |

---

## How to Adapt This to Your Business

1. **Identify your best client.** The one with the highest margin, lowest friction, and happiest relationship. That's your ICP template and your product specification.

2. **Set your revenue target.** The number that makes you default alive. Every D-bucket task gets killed until you hit it.

3. **Define your one offer.** The outcome you sell, not the feature. Strip all feature language from external-facing materials.

4. **Install the sprint rhythm.** Fixed weekly meeting. One goal per sprint. Explicit deferrals. If you don't have this, nothing will catch the drift until it's a crisis.

---

## Quick Start

```
You: I want to add an AI content suggestion feature.
You: /office-hours

Agent: What specific client conversation made you think of this?
You: Nobody asked for it — I just thought it would be cool.

Agent: Stop. That's the signal. YC's #1 lesson: build what people want,
       not what you think is cool. No evidence of demand = no sprint task.
       Let's find what your best client IS asking for.
       [reframes the problem, generates 3 narrower approaches]
       RECOMMENDATION: Talk to your top 3 clients this week.
       Ask: "What's the most annoying part of our current delivery process?"
       Build only what they say with their own words.
```

---

## Credits

### Garry Tan ([@garrytan](https://x.com/garrytan))
President & CEO of Y Combinator. Creator of [gstack](https://github.com/garrytan/gstack) — the open source software factory that directly inspired this project. Garry's "Boil the Lake" principle, his virtual engineering team concept, and his public experiment in agentic development are the foundation everything here is built on. Read his work: [garryslist.org](https://garryslist.org)

### Y Combinator
The source of the core operating principles that run through every skill here — make something people want, talk to users, default alive, do things that don't scale. Thousands of companies built on these principles. [ycombinator.com/library](https://www.ycombinator.com/library)

### Also built on:
- [Garry's "Boil the Lake" essay](https://garryslist.org/posts/boil-the-ocean) — completeness principle
- EOS / Traction by Gino Wickman — sprint rhythm and L10 structure
- Paul Graham's essays — default alive, ramen profitable, do things that don't scale

---

*Built by a solo founder running a content ops company. Every failure baked into these skills was expensive. Fork it. Make it yours.*
