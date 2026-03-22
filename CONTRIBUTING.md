# Contributing to fstack

fstack is an open system. Fork it. Adapt it. Add skills for your context.

---

## How to Add a Skill

### 1. Create the directory

```bash
mkdir -p skills/<skill-name>
```

Use lowercase, hyphens, no spaces. Match the name you'll use as the slash command.

### 2. Create SKILL.md

Every skill lives in `skills/<skill-name>/SKILL.md`. Use this template:

```markdown
---
name: skill-name
version: 0.2.0
description: >
  One paragraph. What it does, when to use it, what triggers it.
  Include example trigger phrases.
inputs:
  - Input 1
  - Input 2
outputs:
  - Output 1
  - Output 2
allowed-tools:
  - Bash
  - Read
  - Write
  - Glob
  - AskUserQuestion
---

# Skill Name
*Credit line — who inspired this or what framework it draws from*

> *"One-line philosophy that defines the skill's purpose."*

One paragraph explaining the core insight. Why does this skill exist? What mistake does it prevent?

---

## Process

[Step-by-step instructions for the AI to follow]

---

## Kill Criteria

Kill if: [list of conditions that mean this skill should return a kill recommendation]

---

## Best Client Test
[How to evaluate if the output serves the best client]

## Revenue Gate
- **A:** [Condition that maps to A]
- **B:** [Condition that maps to B]
- **C:** [Condition that maps to C]
- **D:** [Kill condition]

## Maintainability Check
[Can the smallest team member own this without help?]

---

## Chains to
→ `/next-skill` — [why and when to chain]
```

### 3. Required elements (non-negotiable)

Every skill MUST have:
- [ ] YAML frontmatter with `name`, `version`, `description`, `inputs`, `outputs`, `allowed-tools`
- [ ] One-line philosophy quote at the top
- [ ] Kill criteria section
- [ ] Best Client Test section
- [ ] Revenue Gate section (A/B/C/D)
- [ ] Maintainability Check section
- [ ] Chains to section (even if it only chains to one other skill)

These are the fstack standards. They're not suggestions.

**If your skill belongs to the Brand Identity Layer** (it depends on or produces identity, voice, rules, or memory context), it must also:
- [ ] Reference which brand layer it reads from (`/identity`, `/rules`, `/memory`, `/files`)
- [ ] Reference which brand layer it writes to (or state "no write" explicitly)
- [ ] Document whether it requires `/context-setup` to be loaded before running
- [ ] Include a conflict protocol — what happens if the brand context contradicts the input

### 4. Quality bar

Before submitting, run the skill against these checks:

- **Opinionated.** Don't hedge. Tell the user what to do and what to kill.
- **Short sentences.** If a sentence needs a semicolon, split it.
- **Checklists over prose.** Actionable > comprehensive.
- **Kill logic.** Every skill must have clear "stop and kill" criteria.
- **Best Client Test.** Every output must be filterable against the user's best client.
- **Garry-level rigor.** Would Garry Tan use this? Would he ship it at YC?
- **Brand context aware.** If the skill produces content, it should either depend on `/context-setup` or explicitly state why it doesn't need it. Skills that produce content without brand context are incomplete.

---

## PR Process

1. Fork the repo
2. Create a branch: `feat/skill-name`
3. Add your skill in `skills/<skill-name>/SKILL.md`
4. Update the README — add the skill to the Virtual Team table and Skills section
5. Open a PR with:
   - Title: `feat: add /skill-name — [one-line description]`
   - Description: Philosophy, what problem it solves, what it chains to

### PR checklist
- [ ] SKILL.md passes all required elements above
- [ ] README updated with new skill
- [ ] Skill chains documented in SKILL.md
- [ ] No private or company-specific data in the skill

---

## What Makes a Good fstack Skill

Good:
- Solves a specific, recurring founder problem
- Has clear kill criteria
- Chains naturally to other skills
- Works for a one-person team AND a 10-person team
- Is opinionated (recommends, doesn't just list options)
- Knows where it sits in the stack (brand layer / operating loop / growth team)

Not good:
- Generic "prompt templates" with no decision logic
- Skills that only work for specific tools or platforms
- Skills that never kill anything
- Skills with vague output formats
- Content-producing skills that don't reference brand context at all

## Skill Layers

fstack has three layers. Know which one your skill belongs to before you write it:

**Brand Identity Layer** — Foundation. Runs once per brand before anything else.
Skills: `/identity`, `/rules`, `/memory`, `/files`, `/context-setup`, `/brand-check`, `/repurpose`, `/content-governance`
Rule: Brand layer skills don't chase Revenue Gate A directly. Their job is to protect quality and prevent drift. Their Revenue Gate impact is always downstream — fewer revision rounds (B), faster onboarding (C).

**Core Operating Loop** — Weekly rhythm. Runs every sprint.
Skills: `/office-hours`, `/ceo-review`, `/eng-review`, `/ux-review`, `/ship`, `/retro`, `/gtm-review`, `/brief-review`, `/sprint-plan`, `/l10`
Rule: Operating loop skills always apply the three principles: Best Client Test, Maintainability Check, Revenue Gate.

**Growth Team** — Periodic. Runs at the start of growth pushes and quarterly resets.
Skills: `/positioning-workshop`, `/experiment-designer`, `/cohort-review`, `/launch-orchestrator`, `/customer-interview-synthesizer`, `/virality-loop-designer`, `/seo-content-system`, `/growth-sprint`
Rule: Growth skills always include a kill criterion and a default alive check.

---

## Credits

When your skill draws from an existing framework (April Dunford, YC, EOS, Garry Tan's gstack), cite it in the skill header. fstack stands on shoulders — acknowledge them.

---

## Questions

Open an issue. No DMs required.
