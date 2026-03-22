# Content Governance — Build the Approval System That Runs Without You
*Copy this entire prompt into ChatGPT or Claude. Then follow the instructions.*

---

You are a content operations lead helping me build the approval system for all content leaving my brand. This system maps who approves what, sets time limits per content type, defines what counts as a revision round, and produces an audit trail for every piece that ships.

The goal is simple: the founder should not be in every approval loop. But nothing off-brand, inaccurate, or legally risky should ship without a check. This skill builds the system once. Then it runs without me.

I'm going to give you context about my team and content types. Your job is to help me fill out the full Governance Charter.

---

## What I need to give you first

**Brand name:** [YOUR BRAND NAME]

**Team roles involved in content (list everyone who touches content, with their role):**
[e.g., "Fleire — Founder / Content Lead. Maria — Writer. James — Social Manager. AI tools — first draft production."]

**Content types currently in production:**
[e.g., "LinkedIn posts (brand account), email newsletters, client deliverable reports, paid social ads, blog posts"]

**What's breaking in your current process:**
[e.g., "Writers don't know when something needs founder approval. Revisions happen in email threads. We sometimes publish without a second pair of eyes."]

**Current revision pain:** How many rounds does a typical piece go through?
[e.g., "2–3 rounds for social posts, 4+ for client deliverables"]

**Escalation question:** When do you personally need to see something before it ships?
[e.g., "Any paid content, any client deliverable, anything that names a competitor"]

**SLA expectations:** How fast does content need to move from brief to published?
[e.g., "LinkedIn posts in 48 hours, client deliverables in 5 business days"]

---

## STEP 1 — Approval Matrix

Every content type has one producer, one reviewer, and one approver. No piece moves to the next stage without the prior stage complete.

```
APPROVAL MATRIX — [Brand Name]
Last updated: [date]

CONTENT TYPE: [e.g., LinkedIn post — brand account]
Producer: [name or role]
Reviewer: [name or role — runs brand-check]
Approver: [name or role — final sign-off before publish]
SLA (producer → approver): [e.g., 48 hours]
Revision limit: [e.g., 2 rounds max before escalation]
Distribution channel: [scheduler / direct publish / client handoff]

---

CONTENT TYPE: [e.g., client deliverable — content report]
Producer: [name or role]
Reviewer: [name or role]
Approver: [name or role — client sign-off required before publish]
SLA: [e.g., 5 business days from brief]
Revision limit: [2 rounds included in scope — 3rd round = out-of-scope conversation]
Distribution channel: [email to client / shared Drive / client portal]

---

CONTENT TYPE: [e.g., paid social ad]
Producer: [name or role]
Reviewer: [name or role — brand-check + claim verification]
Approver: [name or role — founder sign-off for all paid content]
SLA: [72 hours before scheduled launch]
Revision limit: [1 round — paid creative must lock 24 hours before launch]
Distribution channel: [ads manager]

---

[Repeat for each content type]
```

Rule: Any role left blank means that approval stage doesn't exist yet. Name it or accept that it's unprotected.

---

## STEP 2 — SLA Table

All time commitments in one view. Used for client expectations and internal accountability.

```
SLA TABLE — [Brand Name]

Content Type               | Production → Review | Review → Approval | Total SLA
---------------------------|--------------------|--------------------|----------
LinkedIn post (brand)      | [X hrs]            | [X hrs]            | [total]
Email (outbound)           | [X hrs]            | [X hrs]            | [total]
Client deliverable (report)| [X days]           | [X days]           | [total]
Paid social ad             | [X hrs]            | [X hrs]            | [total]
Blog post / SEO article    | [X days]           | [X days]           | [total]
[Add your types]           |                    |                    |

SLA BREACH PROTOCOL:
→ SLA missed by < 24 hours: producer flags in standup. No escalation.
→ SLA missed by 24–48 hours: reviewer escalates to content lead.
→ SLA missed by > 48 hours: content lead escalates to founder.
```

---

## STEP 3 — Revision Policy

Unlimited revisions are a scope problem, not a quality problem.

```
REVISION POLICY

Standard included revisions:
- Internal content (social, email, blog): 2 rounds max
- Client deliverables: [define in client contract — typically 2 rounds]
- Paid creative: 1 round (must lock 24 hours before launch)

What counts as one revision round:
A round is one complete set of consolidated feedback from one person or one stakeholder group.
Multiple people giving feedback at different times = multiple rounds.

Round 3+ triggers:
→ Internal content: Was the brief wrong? Run /brief-review (MODE 1) before restarting.
→ Client deliverable: Out-of-scope conversation with client before continuing.
→ Paid creative: Founder involved. Do not miss launch date for revision overflow.

Root cause rule:
Every third-round revision gets logged in the Defect Log. If the same content type hits 3 rounds more than twice in a month → the brief or template is broken. Fix upstream, not the next piece.
```

---

## STEP 4 — Escalation Protocol

When something needs to escalate, these are the four levels. No guessing, no Slack threads.

```
ESCALATION PROTOCOL

LEVEL 1 — Style violation (wrong phrase, off-register):
→ Writer fixes before next checkpoint. No escalation needed.

LEVEL 2 — Claim or compliance violation (unverified stat, missing approval):
→ Hold the piece. Do not ship until resolved.
→ Flag to: [CONTENT LEAD NAME]
→ Resolve within 24 hours.

LEVEL 3 — Legal or brand reputation risk:
→ Hold immediately.
→ Flag to: [FOUNDER/OWNER NAME]
→ Founder reviews within 4 hours. No exception.
Triggers: Client or competitor named without authorization. Content contradicts live positioning in a market-facing way. Platform compliance issue with legal implication.

LEVEL 4 — Published content with error or legal exposure:
→ Remove or retract immediately. Do not wait for consensus.
→ Document: what was published, when, what it said, who published it.
→ Brief: [FOUNDER/OWNER NAME] before any public correction.
→ Do not post a correction without founder review.
→ Post-incident review within 48 hours: what broke in the governance system?
```

---

## STEP 5 — Audit Trail Format

Every shipped piece gets logged. The audit trail is not for compliance. It's for learning — patterns in the trail tell you where the system is breaking.

```
AUDIT TRAIL FORMAT

For every piece that ships, log:

PIECE: [title or description]
Content type: [type]
Producer: [name]
Reviewer: [name]
Approver: [name]
Brief date: [date]
First draft date: [date]
Review date: [date]
Approval date: [date]
Publish date: [date]

Revision rounds: [number]
Brand-check score: [X/7]
Brand-check verdict: [Ship / Fix / Kill → resubmitted]
Escalation triggered: [Level 1–4 / None]
SLA met: [Yes / No — if no, reason]

Post-publish notes (add within 7 days):
- Engagement or conversion result: [if measurable]
- Client feedback: [if applicable]
- Quality issues noted after publish: [flag for defect log]

STORAGE LOCATION: [Notion / Google Sheet / Airtable — wherever team can find it in under 60 seconds]
```

---

## STEP 6 — Defect Log

A defect is any piece that required 3+ revision rounds, failed brand-check more than once, or triggered Level 2+ escalation. Defects aren't failures — they're signals.

```
DEFECT LOG — [Brand Name]

[Date] — DEFECT
Content type: [type]
What happened: [brief description]
Root cause: [brief / template / briefer / reviewer / tool / unclear]
Fix applied: [what was done to this piece]
Systemic fix: [what was changed upstream to prevent recurrence]
Owner of systemic fix: [name]
Due date: [date]

DEFECT PATTERN RULE:
If the same root cause appears 3+ times in 30 days → it's a system failure, not a person failure.
Fix the upstream source (brief template, Voice Card, training) before the next cycle.
```

---

## OUTPUT FORMAT

```
GOVERNANCE CHARTER: [Brand Name]
Created: [date]
Owner: [name]
Status: LIVE

APPROVAL MATRIX:
[complete — one block per content type]

SLA TABLE:
[complete]

REVISION POLICY:
[complete]

ESCALATION PROTOCOL:
[4 levels with names]

AUDIT TRAIL FORMAT:
[complete — with storage location]

DEFECT LOG:
[format + pattern rule]
```

---

## AFTER THIS RUNS

Share this Governance Charter with every person who touches content. Make it accessible without a Slack message or a founder call. The audit trail and defect log should be updated after every shipped piece — not in batches. Run `/brand-check` next on any piece in the pipeline to get its brand compliance score and move it through the approval matrix.

*Part of fstack — open source operating system for founders and marketers. github.com/likke/fstack*
