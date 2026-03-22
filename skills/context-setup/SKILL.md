---
name: context-setup
version: 0.1.0
description: >
  Load all brand context layers into a single session brief before any content
  production begins. Chains /identity, /rules, /memory, and /files into one
  orchestrated setup command. Run at the start of every content session.
  Trigger on: "set up context", "load brand context", "start a content session",
  "context setup", "prepare for content", "load brand layers", "set up for
  content production", "initialize brand context".
inputs:
  - Brand name (required)
  - Voice Card from /identity (required — run /identity first if missing)
  - Rules Card from /rules (required — run /rules first if missing)
  - Memory Index from /memory (required — run /memory first if missing)
  - Brand doc index from /files (recommended)
  - Session goal: what content will be produced this session
outputs:
  - Loaded Context Brief (all layers stacked and conflict-checked)
  - Conflict report (any contradictions between layers)
  - Session charter (goal, constraints, approved starting points)
  - Green / Yellow / Red status for each layer
  - Handoff-ready brief for any content skill that follows
allowed-tools:
  - Bash
  - Read
  - Write
  - Glob
  - AskUserQuestion
---

# Context Setup — Brand Session Orchestrator
*Adapted from gstack's context initialization principle + YC's "do things that don't scale" reframed: front-load the work so production scales.*

> *"Every hour of planning prevents three hours of revision."*

The most expensive moment in content production is when a writer or AI tool starts without knowing what they're not allowed to say. Context Setup eliminates that moment. It loads everything the session needs — voice, rules, decisions, documents — before a single word of content is written.

This is the first skill you run. Every other brand skill runs after.

---

## The 5 Layers

Context Setup loads 5 layers in sequence. Each layer must clear before the next loads.

```
LAYER 1: Voice Card (/identity)
LAYER 2: Rules Card (/rules)
LAYER 3: Memory Index (/memory)
LAYER 4: Brand Doc Index (/files)
LAYER 5: Session Charter (built fresh each session)
```

Missing Layer 1 or Layer 2 → stop. Do not proceed. Run /identity and /rules before returning.
Missing Layer 3 → proceed with warning. Note that memory isn't loaded and flag any positioning references for manual check.
Missing Layer 4 → proceed. Not all sessions require reference documents.

---

## The Process

### Step 1 — Session declaration

Before loading anything, declare the session goal:

```
SESSION DECLARATION
Brand: [name]
Date: [today]
Session goal: [One sentence — what content will be produced this session?]
  e.g., "Write 3 LinkedIn posts for the week of March 24"
  e.g., "Draft the nurture email sequence for the Catipult.ai launch"
  e.g., "Review and approve 4 client deliverable pieces for OceanJet"

Content type(s) this session: [LinkedIn / email / blog / deck / ad / other]
Target platform(s): [list]
Target audience: [specific person — not a demographic]
Revenue Gate for this session: A / B / C
Owner: [who is running this session]
```

### Step 2 — Layer 1: Voice Card

Load the Voice Card from /identity. Confirm it's current.

```
LAYER 1 STATUS: GREEN / YELLOW / RED

GREEN: Voice Card exists, was updated within 90 days, matches current positioning.
YELLOW: Voice Card exists but is older than 90 days or was created before last repositioning.
  → Proceed, but flag that voice may be stale. Update /identity within the week.
RED: Voice Card doesn't exist.
  → STOP. Run /identity before returning to this session.

VOICE CARD SUMMARY (pull these for active use this session):
- Pace: [setting from Voice Card]
- Formality: [setting + session platform modifier]
- Confidence: [setting]
- Forbidden register: [top 5 phrases from Dimension 8]
- Voice tests: [5 test names as a quick checklist]
```

### Step 3 — Layer 2: Rules Card

Load the Rules Card from /rules. Confirm it's current and applies to this session's content types and platforms.

```
LAYER 2 STATUS: GREEN / YELLOW / RED

GREEN: Rules Card exists, covers the platforms in scope for this session, updated within 90 days.
YELLOW: Rules Card exists but doesn't cover one or more platforms in today's session scope.
  → Proceed for covered platforms. Document gap and flag for /rules update.
RED: Rules Card doesn't exist.
  → STOP. Run /rules before returning.

RULES ACTIVE THIS SESSION (pull the relevant layers):
- Forbidden phrases: [top 10 from Layer 1]
- Claim constraints active: [any relevant Layer 2 constraints for this content type]
- Platform hard limits for [today's platform]: [relevant Layer 5 rules]
- Quality floor: [Layer 6 checklist — summarize as 5 binary checks]
- Escalation level for any violation: [Level 1–4 from Step 2 of /rules]
```

### Step 4 — Layer 3: Memory Index

Load the Memory Index from /memory. Check for any live campaign conflicts with this session's content.

```
LAYER 3 STATUS: GREEN / YELLOW / RED

GREEN: Memory Index exists, Section 4 (live campaigns) updated within 7 days.
YELLOW: Memory Index exists but hasn't been updated in 7–30 days. Sections may be stale.
  → Proceed with caution. Manually confirm live campaigns before any positioning reference.
RED: Memory Index doesn't exist OR hasn't been updated in 30+ days.
  → Proceed without Memory, but flag every positioning claim for manual review.

MEMORY ACTIVE THIS SESSION:
- Live positioning one-liner: "[exact text from Section 1]"
- Approved copy to reference: [relevant entries from Section 2]
- Live campaigns that cannot be contradicted: [list from Section 4]
- Killed options — do not reopen: [relevant Section 3 entries]

CONFLICT PRE-CHECK:
Does the session goal require any messaging that might contradict live campaigns or killed options?
[ ] No conflict detected → proceed
[ ] Potential conflict: "[specific overlap]" → flag before producing
```

### Step 5 — Layer 4: Brand Doc Index

Load the Brand Doc Index from /files if any reference documents are needed for this session.

```
LAYER 4 STATUS: GREEN / YELLOW / NOT LOADED

GREEN: Relevant docs identified, freshness confirmed, priority stack loaded.
YELLOW: Docs exist but one or more flagged as stale (>90 days since review).
NOT LOADED: No reference docs needed for this session. Proceed.

DOCUMENTS ACTIVE THIS SESSION:
- [Doc name] — Type: [brief / guideline / reference] — Last verified: [date]
- [Doc name] — Type: [brief / guideline / reference] — Last verified: [date]

PRIORITY STACK (if docs conflict):
1. SKILL.md / fstack rules (highest authority)
2. Client brief or signed scope
3. Campaign brief
4. Style guide
5. Template or reference doc (lowest authority)
```

### Step 6 — Session Charter (Layer 5)

Built fresh every session. The single document that any writer or AI tool reads before producing content.

```
SESSION CHARTER
Brand: [name]
Date: [today]
Owner: [name]
Revenue Gate: A / B / C

SESSION GOAL:
[One sentence — what gets produced today]

WHAT THIS SESSION IS PRODUCING:
- [Content piece 1] — [platform] — [audience] — [CTA]
- [Content piece 2] — [platform] — [audience] — [CTA]

VOICE ACTIVE:
Pace: [setting]. Formality: [setting]. Confidence: [declarative/calibrated].
Forbidden: [top 5 phrases to avoid].

RULES ACTIVE:
Platform limits: [relevant Layer 5 rules in plain language].
Quality floor: [5 binary checks every piece must pass before leaving this session].
Escalation: [which level applies if something's flagged].

MEMORY ACTIVE:
Live positioning: "[one-liner]"
Do not contradict: [campaign name(s) and core messages].
Approved copy to use: [any reusable lines relevant to this session].

APPROVED STARTING POINTS:
These hooks, angles, or lines are pre-approved and can be used as-is:
- [approved line from memory or brief]
- [approved angle from previous campaign]

THIS SESSION IS DONE WHEN:
[Definition of done — specific, not vague]
e.g., "3 LinkedIn posts pass brand-check at 7/7, are ready to schedule."

HANDOFF:
After this session, content moves to: [/brand-check / client review / scheduler]
```

---

## Conflict Detection

If any two layers contradict each other, surface the conflict before producing:

```
CONFLICT REPORT (run at the end of Step 5):

Conflicts found: [ ] None  [ ] Yes — list below

CONFLICT: [Description]
Layer A: [what Layer X says]
Layer B: [what Layer Y says]
Resolution: [ ] Layer A wins (higher priority) / [ ] Layer B wins / [ ] Escalate

Resolution owner: [name]
Resolution deadline: [time — same session if possible]
```

Do not produce content against an unresolved conflict. Resolve first, then produce.

---

## Kill Criteria

Kill the context setup and fix the upstream layer if:
- Layer 1 (Voice Card) is RED → no identity, no production
- Layer 2 (Rules Card) is RED → no rules, no production
- Layer 5 (Session Charter) has no definition of done → no goal, no production
- A conflict is found between Layer 1 and Layer 3 (voice contradicts positioning) → fix one before proceeding

---

## Best Client Test
If your best client watched you run this session setup, would they be confident that everything produced would represent their brand correctly?
- YES → the layers are loaded and the session charter is clear.
- NO → something is missing, stale, or conflicting. Find it before producing.

## Revenue Gate
- **A:** A complete session setup means content can be produced and approved in a single session — no back-and-forth on brand alignment.
- **B:** Retained clients experience consistent output across every session — trust compounds.
- **C:** Eliminates repeated re-briefing of writers and AI tools. Measurable reduction in rework time.
- **D:** Running context-setup for a one-off piece with no brand guidelines → overhead exceeds value. Skip and run /brief-review directly instead.

## Maintainability Check
- Can any team member run context-setup and produce a valid Session Charter without asking the founder?
- Can the setup be completed in under 15 minutes?
- Is every layer stored somewhere the team can access in under 60 seconds?
- If no → the storage system is broken. Fix /files before fixing context-setup.

---

## Chains to (runs before)
→ `/brief-review` (MODE 1) — brief any content task with the Session Charter active
→ `/brand-check` — run after production with Session Charter as the scoring context
→ `/repurpose` — start every repurposing session with context-setup loaded
→ `/content-governance` — session charter feeds the approval workflow

## Depends on (runs after)
→ `/identity` — provides Layer 1
→ `/rules` — provides Layer 2
→ `/memory` — provides Layer 3
→ `/files` — provides Layer 4
