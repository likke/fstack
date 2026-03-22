# Files — Index Your Brand Documents So the Right One Is Always Obvious
*Copy this entire prompt into ChatGPT or Claude. Then follow the instructions.*

---

You are a document operations lead. My team has accumulated brand documents — brand guides, campaign briefs, style guides, old decks, Slack decisions, client briefs. Some are current. Some are stale. Some contradict each other. No one knows which one to use.

My job is to audit everything I have, assign authority tiers, flag what's stale, map any conflicts, and produce a Brand Doc Index that every writer and AI tool loads before touching content. A stale document used confidently is worse than no document at all.

I'm going to list everything I have. Your job is to help me build the index.

---

## What I need to give you first

**Brand name:** [YOUR BRAND NAME]

**Every document currently in use (or sitting in a folder, stale or not):**

| Document name | Location / link | Type | Created | Last reviewed | Owner |
|---|---|---|---|---|---|
| [Name] | [Link or folder] | [Type] | [Date] | [Date or "unknown"] | [Name] |
| [Name] | [Link or folder] | [Type] | [Date] | [Date or "unknown"] | [Name] |
| [Add all of them — don't pre-filter] | | | | | |

**Document types (reference):** brand guide, campaign brief, client brief, style guide, template, research, approved copy, one-off decision

**Any conflicts you already know about:**
[e.g., "Our 2023 brand guide says use sentence case. Our 2024 email templates use title case. We've never resolved this."]

**Documents you suspect are obsolete but haven't deleted:**
[List them — it's better to surface them now than find them in use later]

---

## STEP 1 — Authority Tiering

Assign every document a tier. When two documents conflict, the higher tier wins. This is the resolution system your team uses instead of asking the founder.

```
PRIORITY STACK

TIER 1 — System rules (highest authority):
- Voice Card (/identity) — location: [link] — reviewed: [date]
- Rules Card (/rules) — location: [link] — reviewed: [date]
- Signed client contract scope — location: [link] — reviewed: [date]

TIER 2 — Active briefs:
- [Campaign brief name] — location: [link] — active: [date range] — owner: [name]
- [Client brief name] — location: [link] — active: [date range] — owner: [name]

TIER 3 — Standing guides:
- [Brand guide name] — location: [link] — reviewed: [date] — owner: [name]
- [Style guide name] — location: [link] — reviewed: [date] — owner: [name]

TIER 4 — Reference material:
- [Template name] — location: [link] — type: [content type] — reviewed: [date]
- [Research doc name] — location: [link] — topic: [what it covers] — reviewed: [date]

TIER 5 — Informal decisions (lowest authority):
- [Slack screenshot / email decision / meeting note] — location: [link]
→ Any Tier 5 item referenced more than once: escalate. Write it up as a Tier 3 guide.
```

---

## STEP 2 — Freshness Assessment

A stale document used confidently produces confidently wrong output. Every document gets a freshness status.

```
FRESHNESS ASSESSMENT

FRESH (reviewed within 90 days — safe to use):
- [Document name] — last reviewed: [date]

STALE (90–180 days — use with caution, flag for review):
- [Document name] — last reviewed: [date] — review owner: [name] — review due: [date]

CRITICAL (>180 days or unknown review date — do not use until reviewed):
- [Document name] — last reviewed: [date or "unknown"] — review owner: [name] — review due: [date]

STALE DOC PROTOCOL:
For every stale or critical document:
1. Owner reviews against current live positioning (Memory Section 1)
2. If still accurate → update review date, status → FRESH
3. If has gaps → update doc before it re-enters the index
4. If obsolete → archive it (don't delete — record why it was retired)
```

---

## STEP 3 — Conflict Map

Two documents disagreeing about the same thing is a decision waiting to happen. Map it now, before a writer makes the wrong call.

```
CONFLICT MAP

CONFLICT 1:
Document A: "[name]" says — "[exact position or rule]"
Document B: "[name]" says — "[exact position or rule]"
On topic: [what they disagree about]
Resolution: Document [A/B] wins — reason: [higher tier / more current / founder decision]
Action: Update [lower-tier doc] to match. Done by: [name] by [date].

CONFLICT 2:
[Same structure]

UNRESOLVED CONFLICTS (escalate to founder):
- [Conflict description] — flagged to: [name] — deadline: [date]
```

---

## STEP 4 — Build the Index

Final output. This is what `/context-setup` loads as Layer 4.

```
BRAND DOC INDEX: [Brand Name]
Last updated: [date]
Owner: [name]

TIER 1 — SYSTEM RULES:
- Voice Card — [location] — Reviewed: [date] — Status: [GREEN/YELLOW/RED]
- Rules Card — [location] — Reviewed: [date] — Status: [GREEN/YELLOW/RED]

TIER 2 — ACTIVE BRIEFS:
- [Campaign brief] — [location] — Active: [date range] — Owner: [name]
- [Client brief] — [location] — Active: [date range] — Owner: [name]

TIER 3 — STANDING GUIDES:
- [Brand guide] — [location] — Reviewed: [date] — Status: [GREEN/YELLOW/RED]
- [Style guide] — [location] — Reviewed: [date] — Status: [GREEN/YELLOW/RED]

TIER 4 — REFERENCE:
- [Template name] — [location] — Type: [content type] — Reviewed: [date]
- [Research doc] — [location] — Topic: [what it covers] — Reviewed: [date]

STALE FLAGS (require review before next use):
- [Document] — owner: [name] — review due: [date]

ARCHIVED (retired — do not use):
- [Document name] — archived: [date] — reason: [why]

PRIORITY RESOLUTION RULE:
When in doubt, the higher tier wins. If two Tier 2 documents conflict → escalate to founder. Do not guess.
```

---

## STEP 5 — Maintenance Protocol

The index is only useful if it stays current.

```
UPDATE TRIGGERS:

Add a document: New campaign brief → add to Tier 2 immediately.
Remove a document: Campaign ends → archive from Tier 2. Do not leave ended campaigns as "active briefs."
Conflict found: Writer produces contradictory output → investigate source, update conflict map.
Freshness review: Monthly for Tier 1 and 2. Quarterly full audit for Tier 3 and 4.

MAINTENANCE OWNER: [name — one person]
STORAGE LOCATION: [Where the whole team can find this in under 60 seconds]
```

---

## AFTER THIS RUNS

Save the Brand Doc Index somewhere your whole team can access without asking. Load it as part of `/context-setup` (Layer 4) at the start of every content session. Any document not in the index should not be referenced in production — if it's worth using, it's worth adding. Run `/context-setup` next to build the full session context using this index.

*Part of fstack — open source operating system for founders and marketers. github.com/likke/fstack*
