# CLAUDE.md

Behavioral guidelines for Claude Code in this repo. Merge with task-specific context as needed.

---

## 1. Think Before Coding
**State assumptions. Surface confusion. Don't silently pick an interpretation.**

- List your assumptions before writing code. If uncertain, ask.
- If multiple approaches exist, present them — don't pick one silently.
- If something is unclear, stop. Name what's unclear and ask.
- Push back if a simpler path exists.

---

## 2. Simplest Fix First
**Default to the least complex solution that solves the problem. No speculation.**

- Fix the bug with the smallest change possible before proposing a refactor.
- Deterministic before dynamic. Hard-coded edge case before abstraction.
- No features beyond what was asked.
- No abstractions for single-use code.
- No "flexibility" or "configurability" that wasn't requested.
- No error handling for impossible scenarios.
- If 200 lines could be 50, rewrite it — but only when asked.
- Test: would a senior engineer call this overcomplicated? If yes, simplify.

---

## 3. Surgical Changes
**Touch only what you must. Clean up only your own mess.**

- Don't improve adjacent code, comments, or formatting unless the task is a refactor.
- Don't change style or rename things unless asked.
- Match existing patterns, even if you'd do it differently.
- If you notice unrelated dead code, mention it — don't delete it.
- Every changed line should trace directly to the request.

---

## 4. Goal-Driven Execution
**Define success criteria. Loop until verified.**

- Transform imperative tasks into verifiable goals.
  - "Add validation" → "Write a test for invalid inputs, then make it pass"
  - "Fix the bug" → "Reproduce it in a test, then fix"
- State a brief plan before implementing multi-step tasks.
- Confirm success before closing the task.

---

## Stack & Conventions

- **Runtime:** Node.js / JavaScript. Markdown-first for skills and templates.
- **Skills:** `.claude/skills/` or `skills/` — each skill is a `SKILL.md` file.
- **Templates:** `templates/` — marketer-facing, copy-paste prompts.
- **Examples:** `examples/` — filled skill outputs for reference.
- **Build commands:** none (pure markdown project). Lint: `markdownlint`.

---

## fstack Skills Available

Run these in sequence or standalone:

**Brand Identity Layer** (run once per brand, in order):
`/identity` → `/rules` → `/memory` → `/files` → `/context-setup`

**Brand Operations** (per session or per piece):
`/brand-check` · `/repurpose` · `/content-governance`

**Core Operating Loop:**
`/office-hours` · `/ceo-review` · `/eng-review` · `/ux-review` · `/ship` · `/retro` · `/gtm-review` · `/brief-review` · `/sprint-plan` · `/l10`

**Growth Team:**
`/positioning-workshop` · `/experiment-designer` · `/cohort-review` · `/launch-orchestrator` · `/customer-interview-synthesizer` · `/virality-loop-designer` · `/seo-content-system` · `/growth-sprint`

**Default triggers:**
- Every content session → `/context-setup` first
- Every new idea → `/office-hours` first
- Every growth push → `/growth-sprint` first
- Anything client-facing → `/brand-check` before it ships

---

## Safety Rules

- Never hardcode API keys, tokens, or credentials.
- Never modify files in `examples/` directly — they are reference outputs.
- Never delete or overwrite a template without an explicit request.
- When in doubt about scope, ask — don't assume and expand.
