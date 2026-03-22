---
name: memory
version: 0.1.0
description: >
  Store and retrieve approved messaging, killed positioning options, live
  campaign contexts, and past content decisions. Prevents contradictions
  across campaigns. Run at the start of any content sprint and update after
  any positioning or campaign decision.
  Trigger on: "what did we decide about", "approved messaging", "what's our
  current positioning", "what campaigns are live", "memory", "what have we
  killed", "past decisions", "content history", "what did we agree on".
inputs:
  - Positioning decisions from /positioning-workshop
  - Campaign metadata from /launch-orchestrator
  - Approved one-liners, taglines, and value props
  - Killed messaging options and reason for killing
  - Client-specific approved language (if applicable)
outputs:
  - Memory Index (4 sections: live positioning, approved copy, killed options, live campaigns)
  - Conflict flags between current request and past decisions
  - Context brief for any content session
  - Feed for /context-setup
allowed-tools:
  - Bash
  - Read
  - Write
  - Glob
  - AskUserQuestion
---

# Memory — Brand Decision Log
*Adapted from gstack's context persistence layer + the YC principle: "Decisions made twice are decisions made wrong."*

> *"The most expensive thing in a small team isn't headcount. It's relitigating decisions you already made."*

Memory is the difference between a content operation and a content factory. A factory produces pieces. An operation makes decisions once, stores them, and references them forever. Without memory, every new campaign starts from scratch — contradicting the last one, retesting what's already been killed, and forcing founders to re-explain positioning to their own team weekly.

This skill is the persistent layer. It doesn't generate content. It prevents contradiction.

---

## The Structure

Memory has four sections. All four run simultaneously. Update any section whenever a relevant decision is made.

---

### Section 1 — Live Positioning

The one positioning that's currently active. Only one is ever live.

```
LIVE POSITIONING
Last updated: [date]
Approved by: [name]

ONE-LINER: [exact text — no paraphrasing]
TARGET: [specific person, company type, situation]
PRIMARY JOB-TO-BE-DONE: [functional job — what they're hiring us to do]
SWITCH TRIGGER: [what event makes them start looking for a solution]
KEY DIFFERENTIATOR: [what makes us the answer to their specific problem]

POSITIONING HISTORY:
- [Date]: [Option killed] — Reason: [why it was killed]
- [Date]: [Option killed] — Reason: [why it was killed]
- [Date]: Current option adopted — Reason: [why it won]

DO NOT REVISIT:
The following options were tested and killed. Do not raise them again without new user evidence:
- [Option] — killed [date] — because: [reason]
- [Option] — killed [date] — because: [reason]
```

---

### Section 2 — Approved Copy Bank

Exact phrases, lines, and structures that have been approved and should be re-used, not rewritten.

```
APPROVED COPY BANK
Last updated: [date]

TAGLINES (approved for use in any context):
- "[Exact tagline]" — approved [date] — use for: [context]
- "[Exact tagline]" — approved [date] — use for: [context]

VALUE PROP STATEMENTS (approved for proposals and decks):
- "[Exact statement]" — approved [date] — context: [where it was first used]

EMAIL SUBJECT LINES (approved, proven open rate):
- "[Subject line]" — [open rate if known] — approved [date]

CTAs (approved for each platform):
- LinkedIn: "[Exact CTA text]"
- Email: "[Exact CTA text]"
- Paid social: "[Exact CTA text]"

PROOF POINTS (approved for use with client permission):
- "[Client name or anonymous] achieved [specific result]" — approved [date] — [approval contact]

CAMPAIGN HOOKS (approved, used successfully):
- "[Hook]" — campaign: [name] — result: [metric]
```

---

### Section 3 — Killed Messaging Log

Messaging options tested, reviewed, and rejected. This section prevents the team from spending time on ideas that have already been decided.

```
KILLED MESSAGING LOG
Last updated: [date]

[Date] — KILLED: [exact option or direction]
Reason: [Why it failed — specific, not vague]
Evidence: [What told us it wasn't working — user feedback, conversion data, or founder judgment]
Do not revisit until: [new evidence type that would reopen the question]

[Date] — KILLED: [exact option or direction]
Reason: [specific]
Evidence: [specific]
Do not revisit until: [specific trigger]
```

---

### Section 4 — Live Campaign Index

All currently running campaigns, in a single view. Prevents contradictions between simultaneous campaign messages.

```
LIVE CAMPAIGN INDEX
Last updated: [date]

CAMPAIGN: [Name]
Status: [ ] Pre-launch  [ ] Live  [ ] Post-launch  [ ] Ended
Channel: [Platform(s)]
Core message: [One sentence — the promise this campaign is making]
Target: [Exact segment]
CTA: [Exact action]
Launch date: [date]
End date: [date or "ongoing"]
Owner: [name]
Do not contradict with: [list any live campaigns that could conflict]

---

CAMPAIGN: [Name]
[same structure]
```

---

## Using Memory in a Content Session

At the start of any content production session, pull the relevant memory sections and check for conflicts before briefing anything:

```
MEMORY CHECK — [Session date]

ACTIVE POSITIONING: [paste one-liner from Section 1]
RELEVANT APPROVED COPY: [paste any bank entries relevant to this piece]
LIVE CAMPAIGNS: [paste any campaigns that could be contradicted by this piece]
CONFLICTS FOUND: [list any contradiction between what's being asked and what's been decided]

IF CONFLICT EXISTS:
→ Flag before producing. Do not produce content that contradicts live campaigns or approved messaging.
→ Escalate to [content lead] if conflict can't be resolved in context.
```

---

## Memory Update Protocol

Memory is only useful if it's maintained. Update it after every decision, not in batches.

```
UPDATE TRIGGERS (update memory immediately after any of these):

→ /positioning-workshop produces a decision → update Section 1
→ /launch-orchestrator goes live → add to Section 4
→ A campaign ends → update status in Section 4, move successful hooks to Section 2
→ A hook or CTA is killed → add to Section 3
→ A client approves a proof point → add to Section 2
→ A quarterly /retro produces messaging decisions → update Sections 1 and 3

OWNER: [name responsible for maintaining the Memory Index]
STORAGE: [location — Notion page / Google Doc / Markdown file in repo]
```

---

## Kill Criteria

Kill the Memory update and flag for review if:
- A new content request contradicts Section 1 (live positioning) without new evidence to justify the shift — block the request, escalate to founder
- Section 3 (killed log) has no entries — the brand has never made a hard decision, or decisions aren't being recorded. Both are problems.
- Section 4 (live campaigns) hasn't been updated in 30+ days — it's not tracking reality anymore
- Two live campaigns in Section 4 are making contradictory promises to the same segment → immediate escalation

---

## Best Client Test
If your best client was briefing a freelancer using only the Memory Index, would the freelancer produce on-brand, non-contradictory content without asking a single clarifying question?
- YES → Memory is operational.
- NO → A section is incomplete or stale. Find it and fix it.

## Revenue Gate
- **A:** A complete Memory Index reduces proposal creation time by reusing approved copy — direct impact on new client speed.
- **B:** Prevents contradictions in retained client content — reduces revision cycles and protects account margins.
- **C:** Eliminates repeated founder involvement in messaging decisions that were already made.
- **D:** Memory built but never referenced → the overhead is not worth it. Maintenance and usage must happen together.

## Maintainability Check
- Is every section owned by a named person, not "the team"?
- Can the Memory Index be updated in under 5 minutes after any decision?
- Is it stored somewhere the whole team can access without asking?
- If no → fix the storage and ownership before adding more content to the index.

---

## Chains to
→ `/identity` — approved voice examples belong in the Voice Card, not Memory
→ `/rules` — approved copy bank informs what's permissible, not what's mandatory
→ `/context-setup` — Memory Index loads as Layer 3 of the brand context stack
→ `/brand-check` — Dimension 4 (message-positioning alignment) checks against Section 1
→ `/content-governance` — killed log informs the escalation audit trail
