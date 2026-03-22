---
name: brand-check
version: 0.1.0
description: >
  7-dimension brand compliance audit for any piece of content before it ships.
  Scores voice, forbidden phrases, specificity, message-positioning alignment,
  CTA, platform rules, and revenue gate fit. Produces a verdict — ship, fix,
  or kill — with specific required changes.
  Trigger on: "brand check", "is this on brand", "review this for brand
  compliance", "brand audit", "score this content", "does this pass",
  "check against brand guidelines", "brand score".
inputs:
  - Content to audit (paste in full — no summarizing)
  - Content type (LinkedIn post / email / blog / deck slide / ad copy / other)
  - Target platform
  - Voice Card from /identity (required)
  - Rules Card from /rules (required)
  - Memory Index from /memory (recommended — to catch contradictions)
outputs:
  - Brand Compliance Score (7 dimensions, each pass/fail with evidence)
  - Verdict: Ship / Fix / Kill
  - Specific required changes (not general feedback)
  - Rewritten version if verdict is Fix
  - Escalation flag if verdict is Kill
allowed-tools:
  - Bash
  - Read
  - Write
  - Glob
  - AskUserQuestion
---

# Brand Check — 7-Dimension Compliance Audit
*Adapted from gstack's `/review` principle: "Every issue resolved with finality — AUTO-FIXED or ASK. Never maybe."*

> *"A brand audit with no verdict is just a critique. Critique doesn't ship product."*

Most content reviews are vague. They say "this needs work" or "I don't love the tone." That's not useful. This skill produces a score, a verdict, and specific changes — or it passes the piece clean. No maybes. No "it depends." Every dimension is binary.

Run this before anything reaches a client, goes live on a platform, or gets handed to a paid distribution channel.

---

## Pre-Audit Checklist

Before scoring, confirm these inputs are loaded:

```
[ ] Voice Card from /identity — if missing, run /identity first
[ ] Rules Card from /rules — if missing, run /rules first
[ ] Memory Index from /memory — recommended, not required
[ ] Content type confirmed: [LinkedIn / email / blog / deck / ad / other]
[ ] Target platform confirmed: [where this will be published]
[ ] Target audience confirmed: [who is reading this]
```

Missing Voice Card or Rules Card → do not proceed. The audit is meaningless without them.

---

## The 7-Dimension Audit

Run every dimension. None are optional. Score each as PASS or FAIL with a quote from the content as evidence.

---

### Dimension 1 — Voice Alignment

Does this sound like the brand, or does it sound like a language model writing what it thinks the brand sounds like?

Check against Voice Card dimensions 1–5 (pace, formality, confidence, emotional range, authority signal).

```
D1 — VOICE ALIGNMENT: PASS / FAIL

Evidence (quote from content):
"[exact line from piece]"

Violation (if FAIL):
[ ] Wrong pace — [too formal/too casual vs. Voice Card standard]
[ ] Hedging language — [specific phrase that signals low confidence]
[ ] Wrong emotional register — [performed emotion the brand doesn't show]
[ ] Generic authority — [claimed expertise without evidence]

Required fix (if FAIL):
[Specific rewrite, not general direction]
```

---

### Dimension 2 — Forbidden Phrase Scan

Zero tolerance. One forbidden phrase = automatic FAIL.

```
D2 — FORBIDDEN PHRASE SCAN: PASS / FAIL

Core scan (check each):
[ ] "Leverage" — [found / not found]
[ ] "Unlock" — [found / not found]
[ ] "Empower" — [found / not found]
[ ] "Game-changer" or "Revolutionary" — [found / not found]
[ ] "In today's fast-paced world" or any variation — [found / not found]
[ ] "It's no secret that..." — [found / not found]
[ ] "Take your X to the next level" — [found / not found]
[ ] "We're excited to announce..." — [found / not found]
[ ] [Brand-specific forbidden terms from Rules Card Layer 1] — [found / not found]

Violations found:
- "[Exact phrase]" — appears on line [X] — replace with: "[specific alternative]"

Required fix (if FAIL):
Replace every violation. Recheck before passing.
```

---

### Dimension 3 — Specificity

Does the content contain real numbers, real names, or real examples? Or is it describing concepts in the abstract?

```
D3 — SPECIFICITY: PASS / FAIL

Test: Does every major claim have a real number, real name, or real example attached?

Vague claims found (FAIL):
- "[Exact vague statement]" — needs: [what would make this specific?]
- "[Exact vague statement]" — needs: [what would make this specific?]

Strong specific claims (PASS signals):
- "[Exact specific line]" — this is correct.

If no real data exists:
→ Flag for addition. Do not fabricate numbers. Use "in our experience" or "we've seen" if no data available.
→ But fewer than 2 specific anchors in a piece = FAIL.

Required fix (if FAIL):
[Specific additions — what data or examples need to be sourced?]
```

---

### Dimension 4 — Message-Positioning Alignment

Does this piece reinforce the live positioning (from Memory Section 1), or does it accidentally contradict it?

```
D4 — MESSAGE-POSITIONING ALIGNMENT: PASS / FAIL

Live positioning one-liner: "[paste from /memory Section 1]"
Live campaign messages (if any): "[paste from /memory Section 4]"

Content promise (what this piece is saying): "[extract the core claim]"

Alignment check:
[ ] Content promise reinforces or is neutral to live positioning → PASS
[ ] Content promise contradicts live positioning → FAIL — escalate
[ ] Content promise makes a claim Memory has killed → FAIL — immediate hold

Violations found (if any):
"[Exact contradicting line]" — contradicts: [what in memory]

Required fix (if FAIL):
[Specific adjustment or escalation instruction]
```

---

### Dimension 5 — CTA Quality

One CTA, clearly stated, appropriate to the platform. Not buried. Not begging.

```
D5 — CTA QUALITY: PASS / FAIL

CTA found: "[exact text]"
CTA count: [number — must be 1]
CTA position: [where in the piece]
CTA register: [matches platform modifier from Voice Card? Yes / No]

Checks:
[ ] Exactly one CTA → PASS / FAIL (if multiple, FAIL)
[ ] CTA is direct, not apologetic → PASS / FAIL
[ ] CTA is appropriate to where the reader is in the funnel → PASS / FAIL
[ ] CTA matches platform rules from Rules Card Layer 5 → PASS / FAIL

Violations (if FAIL):
- [Specific issue with the CTA]

Required fix (if FAIL):
[Exact rewrite of CTA]
```

---

### Dimension 6 — Platform Rules Compliance

Does this piece follow the hard limits for its target platform from Rules Card Layer 5?

```
D6 — PLATFORM RULES COMPLIANCE: PASS / FAIL

Platform: [LinkedIn / Email / X / Paid social / Client deliverable]

Platform rules from Rules Card Layer 5:
[ ] [Relevant rule] — [compliant / violation]
[ ] [Relevant rule] — [compliant / violation]
[ ] [Relevant rule] — [compliant / violation]

Violations found (if any):
- "[Exact violation]" — Rule: [which rule from Layer 5]

Required fix (if FAIL):
[Specific compliance change]
```

---

### Dimension 7 — Revenue Gate Fit

Is this piece serving a Revenue Gate A, B, or C purpose — and is it designed to actually do that job?

```
D7 — REVENUE GATE FIT: PASS / FAIL

Stated purpose: [what this piece is supposed to do]
Revenue Gate category: A / B / C / D

If A (closes in 30 days):
→ Does it create urgency without fake scarcity? [Y/N]
→ Does it make the next step frictionless? [Y/N]
→ Is it reaching someone who can say yes? [Y/N]

If B (retains / nurtures — 60-90 days):
→ Does it build trust without asking for anything? [Y/N]
→ Does it advance the relationship, not just fill a calendar? [Y/N]

If C (brand / awareness):
→ Is there a reason to publish this beyond "we should post something"? [Y/N]
→ Does it reflect the brand at its best? [Y/N]

If D:
→ This piece has no clear revenue function. Kill or reclassify before publishing.

Required fix (if FAIL):
[Reframe the piece for its actual revenue function, or kill it]
```

---

## Scoring and Verdict

```
BRAND CHECK REPORT

Content: [type and brief description]
Platform: [where this goes]
Date: [today]

DIMENSION SCORES:
D1 — Voice Alignment:          PASS / FAIL
D2 — Forbidden Phrase Scan:    PASS / FAIL
D3 — Specificity:              PASS / FAIL
D4 — Message Alignment:        PASS / FAIL
D5 — CTA Quality:              PASS / FAIL
D6 — Platform Compliance:      PASS / FAIL
D7 — Revenue Gate Fit:         PASS / FAIL

SCORE: [X/7]

VERDICT:
7/7 PASS → SHIP. No changes required.
5–6/7 → FIX. Required changes listed below. Recheck after edits.
3–4/7 → REWRITE. The piece needs structural work, not edits.
< 3/7 → KILL. This brief was wrong. Run /brief-review (MODE 1) before re-starting.

REQUIRED CHANGES:
[List each specific fix — no "improve the tone," only "replace 'leverage' on line 2 with 'use'"]

REWRITTEN VERSION (if Fix or Rewrite verdict):
[Provide a rewritten draft if the verdict is Fix. For Rewrite, outline what the new brief needs to say.]

ESCALATION:
[ ] D4 positioning contradiction found → flag to [content lead] before proceeding
[ ] D2 compliance violation found → hold until [owner] reviews
[ ] D7 = D verdict → kill and debrief with [founder]
```

---

## Kill Criteria

Kill the audit (not the content — the audit itself) and restart if:
- Voice Card is missing → the audit is guessing. Run /identity first.
- Rules Card is missing → Dimensions 2 and 6 are invalid. Run /rules first.
- The content is a summary or paraphrase — audit requires the final exact text, not a version of it.

---

## Best Client Test
Would your best client, reading the audit output, trust that the piece either cleared a real bar or needs real fixes?
- YES → the audit is producing signal.
- NO → the audit is producing comfort. If every piece gets 6/7 with vague fixes, the scoring rubric is wrong.

## Revenue Gate
- **A:** A piece of content that passes brand-check can go to paid distribution immediately — no revision delay.
- **B:** Retained clients receive consistent, compliant content — fewer escalations and revision rounds.
- **C:** Every passed piece is brand-safe for organic publication — reduces compliance risk.
- **D:** Brand-check run on internal documents or drafts no one will see → skip.

## Maintainability Check
- Can a writer run this audit on their own piece without asking for feedback?
- Is the verdict always binary — ship, fix, or kill — with no "it depends"?
- Is the audit fast enough that writers will actually run it? (Target: 10 minutes per piece.)
- If no → the audit is too long or too vague. Cut any dimension that produces a non-binary result.

---

## Chains to
→ `/identity` — Voice Card is the rubric for Dimension 1
→ `/rules` — Rules Card is the rubric for Dimensions 2 and 6
→ `/memory` — Memory Index feeds Dimension 4
→ `/brief-review` — Brand Check is the structured version of Output Review (MODE 2)
→ `/content-governance` — Kill verdict triggers escalation protocol
→ `/repurpose` — run Brand Check on every output variant before distribution
