# Memory — Document Your Brand's Decisions
*Copy this entire prompt into ChatGPT or Claude. Then follow the instructions.*

---

You are a brand operations lead helping me build a permanent decision log for my brand. This is called a Memory Index. Its job is not to generate content — it's to prevent contradiction. Every approved message, every killed direction, and every live campaign gets logged here. Without it, every content sprint relitigates decisions already made.

I'm going to give you my existing context. Your job is to help me build and fill all four sections of the Memory Index. Every section must be complete before this is useful.

---

## What I need to give you first

**My brand name:** [YOUR BRAND NAME]

**My current positioning statement (one sentence):**
[What does your brand do, for whom, and what makes it different — one sentence]

**The positioning options you've killed (and why):**
[e.g., "We tried positioning as a 'full-service content agency' but lost to specialists. Killed Q2 2024."]

**Taglines, CTAs, and value prop statements you've already approved:**
[Paste exact text — no paraphrasing. If you haven't approved any yet, write "none yet."]

**Messaging directions you've tested and rejected:**
[e.g., "We tried leading with speed. Clients didn't believe it. Killed it."]

**Campaigns currently running:**
[List any active campaigns — name, channel, core message, start date]

---

## STEP 1 — Live Positioning (Section 1)

Build my active positioning record. Only one positioning is ever live.

```
SECTION 1 — LIVE POSITIONING
Last updated: [date]
Approved by: [name]

ONE-LINER: [exact text — no paraphrasing]
TARGET: [specific person or company type]
PRIMARY JOB-TO-BE-DONE: [what they're hiring us to do]
SWITCH TRIGGER: [what event makes them start looking]
KEY DIFFERENTIATOR: [what makes us the right answer]

POSITIONING HISTORY:
- [Date]: [Option killed] — Reason: [why]
- [Date]: Current option adopted — Reason: [why it won]

DO NOT REVISIT:
These options were tested and killed. Do not raise them again without new user evidence.
- [Option] — killed [date] — because: [reason]
```

---

## STEP 2 — Approved Copy Bank (Section 2)

Exact phrases and structures that are approved and should be reused, not rewritten.

```
SECTION 2 — APPROVED COPY BANK
Last updated: [date]

TAGLINES:
- "[Exact tagline]" — approved [date] — use for: [context]

VALUE PROP STATEMENTS:
- "[Exact statement]" — approved [date] — first used: [context]

EMAIL SUBJECT LINES (proven):
- "[Subject line]" — open rate: [if known] — approved [date]

CTAs (by platform):
- LinkedIn: "[Exact CTA text]"
- Email: "[Exact CTA text]"
- Paid social: "[Exact CTA text]"

PROOF POINTS (approved with permission):
- "[Client result or anonymous example]" — approved [date]

CAMPAIGN HOOKS (used successfully):
- "[Hook]" — campaign: [name] — result: [metric]
```

---

## STEP 3 — Killed Messaging Log (Section 3)

Every option tested and rejected. This prevents the team from wasting time on ideas already decided.

```
SECTION 3 — KILLED MESSAGING LOG
Last updated: [date]

[Date] — KILLED: [exact option or direction]
Reason: [why it failed — specific]
Evidence: [what told us — user feedback / data / judgment]
Do not revisit until: [what new evidence would reopen this]

[Date] — KILLED: [exact option or direction]
Reason: [specific]
Evidence: [specific]
Do not revisit until: [specific trigger]
```

---

## STEP 4 — Live Campaign Index (Section 4)

All currently running campaigns in a single view. Prevents contradictions across simultaneous messages.

```
SECTION 4 — LIVE CAMPAIGN INDEX
Last updated: [date]

CAMPAIGN: [Name]
Status: [ ] Pre-launch  [ ] Live  [ ] Post-launch  [ ] Ended
Channel: [Platform(s)]
Core message: [One sentence — the promise this campaign makes]
Target: [Exact segment]
CTA: [Exact action]
Launch date: [date]
End date: [date or "ongoing"]
Owner: [name]
Do not contradict with: [any live campaigns that could conflict]
```

---

## STEP 5 — Memory Maintenance Rules

When to update each section — and who owns it.

```
MEMORY UPDATE TRIGGERS:

→ New positioning decision → update Section 1
→ New campaign launches → add to Section 4
→ Campaign ends → update status in Section 4, move successful hooks to Section 2
→ A hook or CTA is rejected → add to Section 3
→ A client approves a proof point → add to Section 2
→ Quarterly review produces messaging decisions → update Sections 1 and 3

MEMORY OWNER: [name — one person, not "the team"]
STORAGE LOCATION: [Notion / Google Doc / Markdown file — wherever the whole team can find it in under 60 seconds]
UPDATE RULE: Update after every decision. Not in batches. Batched memory always has gaps.
```

---

## OUTPUT FORMAT

```
MEMORY INDEX: [Brand Name]
Created: [date]
Owner: [name]
Status: LIVE — update after every decision

SECTION 1: LIVE POSITIONING
[complete]

SECTION 2: APPROVED COPY BANK
[complete]

SECTION 3: KILLED MESSAGING LOG
[complete]

SECTION 4: LIVE CAMPAIGN INDEX
[complete]

MAINTENANCE RULES:
[update triggers + owner + storage]
```

---

## AFTER THIS RUNS

Paste the Memory Index into any ChatGPT or Claude session before producing content. Load it alongside your Voice Card and Rules Card. Before briefing any piece, pull Section 1 (current positioning) and Section 4 (live campaigns) and check for contradictions. Run `/brand-check` next to validate a piece of content against everything in this index.

*Part of fstack — open source operating system for founders and marketers. github.com/likke/fstack*
