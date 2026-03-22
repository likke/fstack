---
name: files
version: 0.1.0
description: >
  Index and manage all brand reference documents. Tracks authority level,
  freshness, and conflicts between docs so every content session starts with
  the right source — not the most recent or the most convenient one.
  Trigger on: "what docs do we have", "which brief should I use", "our brand
  docs", "file index", "which document is authoritative", "brand references",
  "document freshness", "which version is right".
inputs:
  - List of existing brand documents (with location or link)
  - Document types (brand guide, campaign brief, style guide, template, research)
  - Dates of creation and last review (or "unknown")
  - Any known conflicts between documents
outputs:
  - Brand Doc Index (all documents, typed, tiered, freshness-flagged)
  - Priority stack (which document wins when two conflict)
  - Stale document flags (anything > 90 days since review)
  - Conflict map (which docs contradict each other and why)
  - Recommendations for consolidation or deletion
allowed-tools:
  - Bash
  - Read
  - Write
  - Glob
  - AskUserQuestion
---

# Files — Brand Document Index
*Adapted from gstack's configuration management principles + YC's "build systems your team can run without you."*

> *"The most dangerous document on your team is the one everyone uses and no one owns."*

Every growing content operation accumulates documents: brand guides, campaign briefs, style guides, client templates, old decks, one-off decisions saved in Slack threads. Most teams have more documents than decisions. The result is writers using the wrong brief, AI tools trained on stale guides, and clients receiving inconsistent output because two briefs disagreed and no one noticed.

This skill builds the index that makes the right document obvious every time.

---

## The Process

### Step 1 — Document audit

List every document that currently exists. Quantity is the point here — don't pre-filter.

```
DOCUMENT AUDIT — [Brand Name]
Date: [today]

[Document name] — [location/link] — [type] — [created: date] — [last reviewed: date] — [owner: name]
[Document name] — [location/link] — [type] — [created: date] — [last reviewed: date] — [owner: name]
...

DOCUMENT TYPES:
- Brand guide — foundational identity and voice
- Campaign brief — specific campaign context
- Client brief — client-specific requirements and preferences
- Style guide — formatting, grammar, and platform rules
- Template — reusable structure for recurring content types
- Research — market, ICP, or competitive data
- Approved copy — pre-cleared lines, taglines, proof points
- One-off decision — a decision made in Slack, email, or a meeting that no one turned into a document
```

If "last reviewed" is unknown for more than 3 documents → the index doesn't exist yet. This session is the first one.

### Step 2 — Authority tiering

Assign every document an authority tier. When two documents conflict, the higher tier wins.

```
PRIORITY STACK (from highest to lowest authority):

TIER 1 — System rules
- fstack SKILL.md files (brand-check, rules, identity)
- Signed client contract scope

TIER 2 — Active briefs
- Current campaign brief (active campaigns only)
- Signed client brief or creative brief

TIER 3 — Standing guides
- Brand guide (voice, visual, tone)
- Style guide (formatting, platform rules)

TIER 4 — Reference material
- Templates (reusable but not authoritative)
- Research documents (informational, not directive)

TIER 5 — Informal decisions
- Slack screenshots
- Email decisions
- Meeting notes
Any Tier 5 item that's been referenced more than once → escalate to Tier 3 by writing it properly.
```

### Step 3 — Freshness assessment

Stale documents are worse than no documents. A writer following a stale brand guide is confidently wrong.

```
FRESHNESS ASSESSMENT:

FRESH (reviewed within 90 days): [list] → safe to use
STALE (90–180 days since review): [list] → use with caution, flag for review
CRITICAL (>180 days since review): [list] → do not use until reviewed
UNKNOWN (no review date): [list] → treat as critical

STALE DOC PROTOCOL:
For every stale or critical doc:
1. Owner reviews against current positioning (from /memory Section 1)
2. If doc is still accurate → update review date
3. If doc has gaps → update doc before it re-enters the index
4. If doc is obsolete → archive it (don't delete — record why it was retired)

REVIEW DEADLINES:
[Document] — owner: [name] — review due: [date]
[Document] — owner: [name] — review due: [date]
```

### Step 4 — Conflict map

Two documents saying different things about the same topic is a decision waiting to happen. Map conflicts before writers encounter them.

```
CONFLICT MAP:

CONFLICT 1:
Document A: "[name]" says — "[exact position]"
Document B: "[name]" says — "[exact position]"
On topic: [what they disagree about]
Resolution: Document [A/B] wins — because: [tier + reasoning]
Action: Update [the lower-tier doc] to match. Done by: [name] by [date].

CONFLICT 2:
[same structure]
```

Unresolved conflicts → add to /l10 IDS list. Don't leave them floating.

### Step 5 — Build the Index

Final output. This is what /context-setup loads as Layer 4.

```
BRAND DOC INDEX — [Brand Name]
Last updated: [date]
Owner: [name]

TIER 1 — SYSTEM RULES:
- /identity Voice Card — [location] — Reviewed: [date] — [GREEN/YELLOW/RED]
- /rules Rules Card — [location] — Reviewed: [date] — [GREEN/YELLOW/RED]

TIER 2 — ACTIVE BRIEFS:
- [Campaign brief name] — [location] — Active: [date range] — Owner: [name]
- [Client brief name] — [location] — Active: [date range] — Owner: [name]

TIER 3 — STANDING GUIDES:
- [Brand guide name] — [location] — Reviewed: [date] — [GREEN/YELLOW/RED]
- [Style guide name] — [location] — Reviewed: [date] — [GREEN/YELLOW/RED]

TIER 4 — REFERENCE:
- [Template name] — [location] — Type: [content type] — Reviewed: [date]
- [Research doc] — [location] — Topic: [what it covers] — Reviewed: [date]

STALE FLAGS:
[Any document marked YELLOW or RED — name + review owner + deadline]

ARCHIVED (retired documents):
- [Document name] — archived: [date] — reason: [why]

PRIORITY RESOLUTION:
When in doubt, the higher tier wins. If two Tier 2 documents conflict → escalate to founder. Do not guess.
```

---

## Maintenance Protocol

```
UPDATE TRIGGERS:

Add a document: new campaign brief → add to Tier 2 immediately
Remove a document: campaign ends → archive from Tier 2
Freshness review: quarterly /retro → flag stale documents as L10 issue
Conflict found: any time a writer or AI produces contradictory output → investigate and update conflict map

MAINTENANCE CADENCE:
Monthly: check all Tier 1 and Tier 2 freshness
Quarterly: full index audit (add to /l10 rocks)
Owner: [name]
```

---

## Kill Criteria

Kill the document and archive it (never use it again) if:
- It contradicts current live positioning and hasn't been updated in 60+ days
- It references a cancelled campaign, retired product, or former client
- It's been superseded by a Tier 1 document and the old version is still in active folders
- No one can name the person responsible for it

---

## Best Client Test
If your best client asked "what brief are you working from?" — could you answer in one sentence, point to the document, and confirm it was reviewed this month?
- YES → your document system is operational.
- NO → a document is either missing, stale, or unowned. This session's output is at risk.

## Revenue Gate
- **A:** A current client brief and campaign brief means proposals and deliverables go out faster. Directly affects close and retention speed.
- **B:** Consistent reference documents mean retained clients receive work that builds on itself, not work that forgets what was decided last month.
- **C:** A maintained index means writers and AI tools don't need founder time to find the right source. Measurable burn reduction.
- **D:** Indexing documents that have no active readers and no active use → skip until the index has >5 active documents.

## Maintainability Check
- Is every document in the index owned by a named person?
- Can any team member pull the right document for any content session in under 2 minutes?
- Is the index stored somewhere accessible without Slack, email, or a founder call?
- If no → fix the storage location before adding more documents to the index.

---

## Chains to
→ `/context-setup` — Brand Doc Index loads as Layer 4 of the session context
→ `/memory` — approved copy from Tier 2/3 docs can be promoted to the Memory Copy Bank
→ `/content-governance` — stale document flags become governance escalation items
