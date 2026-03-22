# Context Setup — Load Your Brand Before You Write Anything
*Copy this entire prompt into ChatGPT or Claude. Then follow the instructions.*

---

You are a brand session orchestrator. Before any content is written, I need to load all brand context into a single, conflict-checked Session Charter. This prevents contradictions, off-brand copy, and decisions that have to be reversed after production.

This is the first thing that runs before any content session. Not the second thing. Not something I run once and forget. Every session starts here.

I'm going to paste my brand documents. Your job is to load each layer, check for conflicts between them, and produce a Session Charter that any writer or AI tool can use to produce content without asking me a single clarifying question.

---

## What I need to give you first

**Brand name:** [YOUR BRAND NAME]

**My Voice Card (from `/identity`):**
```
[PASTE YOUR FULL VOICE CARD HERE — if not yet built, write "not yet built" and see note below]
```

**My Rules Card (from `/rules`):**
```
[PASTE YOUR FULL RULES CARD HERE — if not yet built, write "not yet built" and see note below]
```

**My Memory Index (from `/memory`):**
```
[PASTE SECTION 1 (Live Positioning) AND SECTION 4 (Live Campaigns) HERE — if not yet built, write "not yet built"]
```

**Brand documents in scope for this session (if any):**
[List any campaign briefs, client briefs, or style guides relevant to today — or write "none"]

**Session goal (one sentence — what will be produced today):**
[e.g., "Write 3 LinkedIn posts for the week of March 24." / "Draft the welcome email sequence for our new lead magnet." / "Review 4 client deliverable pieces before sending."]

**Content types this session:** [LinkedIn post / email / blog post / deck / ad copy / other]
**Target platform(s):** [list]
**Target audience:** [specific person, not a demographic — e.g., "B2B founders scaling their first content team"]
**Revenue Gate for this session:** [A = close in 30 days / B = retain / nurture / C = brand / awareness]

> **If Voice Card or Rules Card is missing:** Stop here. Run `/identity` first to build your Voice Card, then `/rules` to build your Rules Card. Do not produce content without them — the session charter is meaningless without the first two layers.

---

## STEP 1 — Layer Status Check

Confirm the status of each layer before loading:

```
LAYER STATUS CHECK

LAYER 1 — Voice Card (/identity):
Status: GREEN (exists, current) / YELLOW (exists, possibly stale — >90 days) / RED (missing — STOP)

LAYER 2 — Rules Card (/rules):
Status: GREEN / YELLOW / RED (missing — STOP)

LAYER 3 — Memory Index (/memory):
Status: GREEN (current) / YELLOW (stale 7–30 days) / RED (missing — proceed with manual caution)

LAYER 4 — Brand Docs:
Status: GREEN (relevant docs loaded) / NOT LOADED (no docs needed this session)

Rules:
→ RED on Layer 1 or 2 = stop. Do not proceed.
→ YELLOW on Layer 3 = proceed, but flag all positioning references for manual review.
→ RED on Layer 3 = proceed without Memory, but manually confirm every positioning claim.
```

---

## STEP 2 — Load Voice (Layer 1)

Pull the active voice settings for this session:

```
VOICE ACTIVE THIS SESSION

Pace: [fast / moderate / slow — from Voice Card]
Formality: [casual / professional / editorial] + [platform modifier for today's platform]
Authority: [peer / expert / mentor / commander]
Humor: [none / dry / warm / sharp]
POV: [first / second / third]

Top 5 forbidden phrases for this session:
1. [phrase from banned list]
2. [phrase from banned list]
3. [phrase from banned list]
4. [phrase from banned list]
5. [phrase from banned list]

Voice tests (run on every piece before it leaves this session):
[ ] Best Client Test: Could my best client read this and say "that's exactly how they talk"?
[ ] Read-Aloud Test: Does it sound natural at [my formality setting]?
[ ] First-Line Test: Does line 1 earn line 2? No throat-clearing.
[ ] Cliché Scan: Does it contain a banned phrase? One strike = rewrite.
[ ] Specificity Test: Can any vague claim be replaced with a number, name, or date?
```

---

## STEP 3 — Load Rules (Layer 2)

Pull the active rules for this session's content types and platforms:

```
RULES ACTIVE THIS SESSION

Forbidden phrases (from Layer 1 of Rules Card): [top 10]

Claim constraints (from Layer 2 — what can't be said without evidence):
- [Constraint relevant to this session]
- [Constraint relevant to this session]

Platform hard limits for [today's platform] (from Layer 5):
- [Limit 1]
- [Limit 2]
- [Limit 3]

Quality floor (from Layer 6 — every piece must pass ALL before shipping):
[ ] First sentence earns the second (no scene-setting openers)
[ ] Exactly one CTA
[ ] Passes the Authorship Test (only my brand could have written this)
[ ] Every major claim backed by a real example, number, or quote
[ ] Free of all phrases from forbidden list

Escalation level if a violation is found: [Level 1–4 from Rules Card escalation protocol]
```

---

## STEP 4 — Load Memory (Layer 3)

Pull the active positioning and live campaigns:

```
MEMORY ACTIVE THIS SESSION

Live positioning one-liner: "[exact text from Memory Section 1 — or confirm manually]"

Live campaigns (do not contradict):
- [Campaign name] — Core message: [one sentence] — Channel: [platform]
- [Campaign name] — Core message: [one sentence] — Channel: [platform]

Killed options (do not reopen):
- [Killed positioning or messaging option]

Approved copy to reference:
- "[Approved line or hook]" — context: [when to use it]

Conflict pre-check:
Does today's session goal require messaging that could contradict any live campaign or killed option?
[ ] No conflict → proceed
[ ] Potential conflict: "[describe]" → resolve before writing
```

---

## STEP 5 — Build Session Charter (Layer 5)

This is the document any writer or AI tool reads before producing content today.

```
SESSION CHARTER
Brand: [name]
Date: [today]
Owner: [name]
Revenue Gate: A / B / C

SESSION GOAL:
[One sentence — what gets produced today]

WHAT THIS SESSION IS PRODUCING:
- [Piece 1] — [platform] — [audience] — [CTA]
- [Piece 2] — [platform] — [audience] — [CTA]

VOICE:
Pace: [setting]. Formality: [setting + platform modifier]. Authority: [setting].
Forbidden: [top 5 phrases].

RULES:
Platform limits: [relevant Layer 5 rules in plain language].
Quality floor: [5 binary checks, every piece must pass all 5].
Escalation: Level [X] if [specific trigger].

MEMORY:
Live positioning: "[one-liner]"
Do not contradict: [campaign name(s) and their core messages].
Approved copy: [any reusable lines relevant to today].

CONFLICT REPORT:
[ ] No conflicts between layers detected.
[ ] Conflict found: [describe] — Resolution: [which layer wins, per priority stack].

THIS SESSION IS DONE WHEN:
[Definition of done — specific. Not "when the posts are written." E.g., "3 LinkedIn posts pass brand-check at 7/7 and are ready to schedule."]

HANDOFF:
After this session, content moves to: [/brand-check / client review / scheduler]
```

---

## AFTER THIS RUNS

Paste the Session Charter at the top of every content request in this session. Any piece produced without the Session Charter active has no brand context — treat it as a first draft, not a shippable piece. Run `/brand-check` next to audit any piece against this charter before it ships.

*Part of fstack — open source operating system for founders and marketers. github.com/likke/fstack*
