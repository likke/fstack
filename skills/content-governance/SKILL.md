---
name: content-governance
version: 0.1.0
description: >
  Define and run the approval workflow for all content leaving the brand.
  Maps who approves what, sets SLA per content type, tracks revision rounds,
  and produces an audit trail for every piece that ships. Run once to set up
  the governance system; run weekly in /l10 to review escalations.
  Trigger on: "content approval", "who approves this", "content workflow",
  "approval process", "revision tracking", "content governance", "SLA for
  content", "who signs off", "escalation", "audit trail".
inputs:
  - Team structure and roles (who produces, who reviews, who approves)
  - Content types in production (list all)
  - Current revision pain points (what's breaking in the current process)
  - Escalation thresholds (when does the founder need to see something?)
  - SLA expectations from clients or leadership
outputs:
  - Governance Charter (approval map, SLA per content type, revision limits)
  - Escalation protocol (4 levels, mapped to specific triggers)
  - Audit trail format (what gets logged for every shipped piece)
  - L10 governance scorecard (weekly health check for /l10)
  - Defect log format (track recurring issues at source)
allowed-tools:
  - Bash
  - Read
  - Write
  - Glob
  - AskUserQuestion
---

# Content Governance — Approval Workflow and Audit System
*Adapted from gstack's delivery health principles + EOS Traction's accountability chart + YC's "build systems that fail safely."*

> *"If the founder is in every approval loop, the founder is the bottleneck — not the content."*

Content governance isn't bureaucracy. It's the system that lets the founder step out of the daily approval chain while knowing that nothing off-brand, inaccurate, or legally risky ships without a check. Without a governance system, every piece of content is as good — or as bad — as the person who last touched it.

This skill builds the system once. Then it runs without you.

---

## Part 1 — Governance Charter

### Step 1 — Map the approval matrix

Every content type has one producer, one reviewer, and one approver. No piece moves to the next stage without the stage before it being complete.

```
APPROVAL MATRIX — [Brand Name]
Last updated: [date]

CONTENT TYPE: [e.g., LinkedIn post — brand account]
Producer: [name or role]
Reviewer: [name or role — runs /brand-check]
Approver: [name or role — final sign-off]
SLA (Producer → Approver): [e.g., 48 hours]
Revision limit: [e.g., 2 rounds max before escalation]
Distribution channel: [scheduler / direct publish / client handoff]

---

CONTENT TYPE: [e.g., Client deliverable — content report]
Producer: [name or role]
Reviewer: [name or role]
Approver: [name or role — client sign-off required before publish]
SLA: [e.g., 5 business days from brief]
Revision limit: [e.g., 2 rounds included in scope; 3rd round = out-of-scope conversation]
Distribution channel: [email to client / shared Drive / client portal]

---

CONTENT TYPE: [e.g., Paid social ad]
Producer: [name or role]
Reviewer: [name or role — brand-check + claim verification]
Approver: [name or role — founder sign-off for all paid]
SLA: [e.g., 72 hours before scheduled launch]
Revision limit: [1 round — paid creative must be locked 24 hours before launch]
Distribution channel: [ads manager]

---

[Repeat for each content type in production]
```

Roles not named → that approval stage doesn't exist. Until it's assigned, it's not real.

### Step 2 — SLA table

All SLAs in one view. Used for client commitments and team accountability.

```
SLA TABLE — [Brand Name]

Content Type                  | Production → Review | Review → Approval | Total SLA
------------------------------|--------------------|--------------------|----------
LinkedIn post (brand)         | 24 hrs             | 24 hrs             | 48 hrs
Email (outbound)              | 24 hrs             | 24 hrs             | 48 hrs
Client deliverable (report)   | 3 days             | 2 days             | 5 days
Paid social ad                | 48 hrs             | 24 hrs             | 72 hrs
Blog post / SEO article       | 3 days             | 2 days             | 5 days
Short-form video brief        | 24 hrs             | 24 hrs             | 48 hrs
[Add your content types]

SLA BREACH PROTOCOL:
→ SLA missed by < 24 hours: producer flags in standup. No escalation.
→ SLA missed by 24–48 hours: reviewer escalates to content lead.
→ SLA missed by > 48 hours: content lead escalates to founder. Block added to /l10 IDS.
```

### Step 3 — Revision limits and out-of-scope triggers

Unlimited revisions are a scope problem, not a quality problem.

```
REVISION POLICY:

Standard included revisions per piece:
- Internal content (social, email, blog): 2 rounds max
- Client deliverables: [define in client contract — typically 2 rounds]
- Paid creative: 1 round (must lock 24 hours before launch)

What counts as a revision round:
A round is one complete set of consolidated feedback from one person or one stakeholder group. Multiple comments from multiple people sent at different times = multiple rounds.

Round 3+ triggers:
→ Internal content: brief review (did the brief fail?). Escalate to /brief-review (MODE 1) before restart.
→ Client deliverable: out-of-scope conversation with client before continuing. Document the scope expansion.
→ Paid creative: founder involved. Do not miss launch date for revision overflow.

Root cause protocol:
Every third-round revision gets logged in the Defect Log (see Part 3). If the same content type hits 3 rounds more than twice in a month → the brief or the template is broken. Fix upstream before fixing the next piece.
```

---

## Part 2 — Escalation Protocol

Four levels. The level determines who handles it and how fast.

```
ESCALATION LEVELS:

LEVEL 1 — Quality flag (style, voice, specificity)
Trigger: Brand-check fails on D1, D3, or D5 (voice, specificity, CTA)
Handler: Producer fixes before next checkpoint
Timeline: Same session
Founder involvement: None

LEVEL 2 — Claim or compliance flag
Trigger: Brand-check fails on D2 (forbidden phrase) or D4 (positioning contradiction)
   OR: Content makes an unverified statistical claim
   OR: Client approval is needed before publish
Handler: Reviewer holds the piece and flags to content lead
Timeline: Resolved within 24 hours
Founder involvement: Notified if unresolved in 24 hours

LEVEL 3 — Legal or brand reputation risk
Trigger: Brand-check fails on D6 (platform compliance) with legal implication
   OR: Content references a client, competitor, or incident without authorization
   OR: Content contradicts live positioning (Memory Section 1) in a way that could cause market confusion
Handler: Content lead holds piece and flags to founder immediately
Timeline: Founder reviews within 4 hours
Founder involvement: Required. No exception.

LEVEL 4 — Crisis or reputational emergency
Trigger: Published content contains factual error, legal exposure, or client data breach
Handler: Founder takes direct ownership
Timeline: Response within 1 hour of discovery
Protocol:
  1. Remove or retract the content immediately (don't wait for consensus)
  2. Document: what was published, when, what it said, who published it
  3. Assess exposure: who saw it, is a correction needed, is a client affected?
  4. Issue correction if needed: own the error, fix it, don't minimize
  5. Post-incident review within 48 hours: what broke in the governance system?

DO NOT:
- Post a correction without founder review
- Delete without documenting
- Go silent on a client-facing error
```

---

## Part 3 — Audit Trail

Every shipped piece gets a log entry. The audit trail is not for compliance. It's for learning. Patterns in the trail tell you where the system is breaking.

```
AUDIT TRAIL FORMAT

For every piece that ships, log:

PIECE: [title or description]
Content type: [type]
Producer: [name]
Reviewer: [name]
Approver: [name]
Brief date: [date brief was created or received]
Production date: [date first draft was completed]
Review date: [date review was completed]
Approval date: [date approved for distribution]
Publish date: [date it went live]

Revision rounds: [number]
Brand-check score: [X/7]
Brand-check verdict: [Ship / Fix / Kill → re-submitted]
Escalation level triggered: [1 / 2 / 3 / 4 / None]
SLA met: [Yes / No — if no, note delay reason]

Post-publish notes (add within 7 days):
- Engagement or conversion result: [if measurable]
- Client feedback: [if applicable]
- Any quality issues noted after publish: [flag for defect log]
```

Store the audit trail in: [Notion / Google Sheet / Airtable / repo file]
Audit trail is reviewed in: [monthly /retro / quarterly /l10 rocks]

---

## Part 4 — Defect Log

A defect is any piece that required 3+ revision rounds, failed brand-check more than once, or triggered Level 2+ escalation. Defects aren't failures — they're signals.

```
DEFECT LOG — [Brand Name]

[Date] — DEFECT
Content type: [type]
What happened: [brief description of the failure]
Root cause: [brief / template / briefer / reviewer / tool / unclear]
Fix applied: [what was done to this piece]
Systemic fix: [what was changed upstream to prevent recurrence]
Owner of systemic fix: [name]
Due date: [date by which the systemic fix is complete]

---

DEFECT PATTERNS (review monthly):
If the same root cause appears 3+ times in 30 days:
→ That is a system failure, not a person failure.
→ Add to /l10 IDS list as a rocks item.
→ Fix the upstream source (brief template, Voice Card, training) before the next cycle.
```

---

## Part 5 — L10 Governance Scorecard

Run this in every Monday /l10 meeting. Takes 5 minutes.

```
CONTENT GOVERNANCE SCORECARD — [Week of date]

PRODUCTION HEALTH:
Pieces in production: [number]
On-track to SLA: [number] / [number]
SLA breaches this week: [number] — [list]
Avg revision rounds this week: [number] — target: ≤ 2

BRAND COMPLIANCE:
Average brand-check score this week: [X/7]
Pieces that failed brand-check: [number]
Escalations triggered: [level and number]

DEFECT LOG:
New defects this week: [number]
Systemic fixes due: [list with owners and dates]

RED FLAGS (add to IDS):
- [Flag] — owner — due date
- [Flag] — owner — due date

GREEN:
- [What's working well in governance this week]
```

---

## Kill Criteria

Kill the governance review and escalate to founder if:
- A Level 3 or Level 4 escalation has been open for more than 4 hours without founder awareness
- The audit trail has not been updated in more than 7 days — governance is theater if nothing is being logged
- Average revision rounds across content types is above 3 for two consecutive weeks — the brief system is broken, not the writers
- The defect log has 5+ entries with the same root cause and no systemic fix has been applied → the system isn't learning

---

## Best Client Test
Would your best client, reading about your governance process in a proposal, feel more confident giving you their brand — not less?
- YES → the governance system signals professionalism and trust.
- NO → you've built bureaucracy. Governance that slows down every piece without preventing any errors is overhead, not protection. Cut the stages that don't catch real failures.

## Revenue Gate
- **A:** A documented approval process accelerates enterprise and agency client proposals — governance is a selling point at larger deal sizes.
- **B:** Governance reduces revision rounds with retained clients — direct margin improvement on accounts that get more-than-two rounds today.
- **C:** An audit trail and defect log compound into a training dataset for briefing AI tools — indirect burn reduction over time.
- **D:** Governance applied to internal content no client sees with SLAs no one tracks → overhead only. Remove or simplify until it's earning its maintenance cost.

## Maintainability Check
- Can the approval matrix run for two weeks without the founder checking in?
- Is the audit trail being updated by writers, not founders?
- Does the L10 scorecard produce at least one actionable IDS item per month?
- Can a new team member read the governance charter and follow it without asking a clarifying question?
- If no → the charter has a gap. Find the ambiguous step and make it unambiguous.

---

## Chains to
→ `/l10` — governance scorecard is a standing agenda item
→ `/retro` — audit trail feeds the weekly delivery health review
→ `/brand-check` — brand-check verdict feeds escalation level determination
→ `/rules` — escalation protocol in this skill extends the rules escalation in /rules Step 2
→ `/memory` — defect log systemic fixes sometimes require Memory Index updates
→ `/brief-review` — third-round revisions always chain back to MODE 1 (brief failure)
