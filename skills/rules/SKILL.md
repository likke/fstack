---
name: rules
version: 0.1.0
description: >
  Define and lock the content rules your brand never breaks. Forbidden phrases,
  platform constraints, compliance lines, and quality floors. Run once per brand,
  update when legal, compliance, or positioning changes. Referenced by
  /brand-check and /brief-review on every production cycle.
  Trigger on: "content rules", "what can't we say", "brand constraints",
  "compliance guidelines", "content limits", "forbidden phrases",
  "what we never write", "content policy", "guardrails".
inputs:
  - Brand name and industry
  - Known legal or compliance constraints (if any)
  - Client sensitivity zones (competitor mentions, pricing, claims)
  - Platform-specific rules (what worked / got flagged before)
  - Voice Card from /identity (required — rules extend voice, not replace it)
outputs:
  - Rules Card (6 constraint layers, locked)
  - Forbidden phrase list with reasons
  - Platform-specific hard limits
  - Compliance flags by content type
  - Quality floor checklist (minimum bar for any piece to ship)
allowed-tools:
  - Bash
  - Read
  - Write
  - Glob
  - AskUserQuestion
---

# Rules — Content Constraint Card
*Adapted from gstack's content governance layer + YC's principle: "Build systems that fail safely."*

> *"The best writers don't follow rules. They've internalized them so deeply they look like instinct."*

Rules aren't censorship. They're quality floors. Without explicit rules, every AI output and every junior writer defaults to the average — vague, legally ambiguous, off-brand, and forgettable. A Rules Card makes the floor visible so your team can build above it instead of through it.

This skill documents what your brand never does, why, and what happens when something crosses a line.

---

## The Process

### Step 1 — Map the constraint layers

Six layers. All six must be filled. "None" is not a valid entry — if you've never thought about it, thinking about it now is the work.

```
RULES CARD: [Brand Name]
Last updated: [date]
Depends on: /identity Voice Card [date]

LAYER 1 — FORBIDDEN PHRASES
Words and constructions never used, in any content type, on any platform.

Core list (add your own):
- "Leverage" — sounds like McKinsey wrote it
- "Unlock" — meaningless in B2B context
- "Empower" — performative, not earned
- "Game-changer" / "Revolutionary" — requires proof we haven't provided
- "In today's fast-paced world" — the floor. This is the floor.
- "It's no secret that..." — false intimacy
- "At the end of the day..." — filler
- "Take your [X] to the next level" — unspecific and tired
- "Synergy" / "Ecosystem" / "Holistic" — consultant speak
- "We're excited to announce..." — never lead with your feelings
- [Add brand-specific terms that signal wrong register]

LAYER 2 — CLAIM CONSTRAINTS
What we never say without evidence.

[ ] Never claim ROI percentages without a real client number to back it
[ ] Never claim we're the "only" or "best" without third-party proof
[ ] Never reference competitor weaknesses by name
[ ] Never imply capability we haven't built yet
[ ] Never publish a client story without written approval

Custom constraints:
- [Claim] — [reason/legal risk]
- [Claim] — [reason/legal risk]

LAYER 3 — LEGAL AND COMPLIANCE FLAGS
Non-negotiable lines, regardless of tone or context.

Industry-specific (fill in relevant):
- [Regulated industry claim, e.g. "this is not financial advice"]
- [Data privacy note required in email — GDPR / Philippine DPA]
- [Healthcare / mental health disclaimer if relevant]
- [Testimonial rules — FTC / ASC disclosure if paid]

Default rules for all content:
- No screenshots of private conversations without written consent
- No client logos in public content without written approval
- No pricing claims that can't be verified within 24 hours
- No forward-looking revenue claims ("you will earn X")

LAYER 4 — COMPETITIVE RULES
How we handle mentions of competitors, adjacent products, or market comparisons.

[ ] Never name a competitor negatively in a public piece
[ ] Comparisons only with verifiable, public data
[ ] "Alternative to [X]" framing is allowed only with proof of differentiation
[ ] No direct pricing comparisons without up-to-date verified data

Approved comparison framing: "[Our approach] vs. the traditional approach"
Never approved: "Unlike [Competitor], we actually..."

LAYER 5 — PLATFORM-SPECIFIC HARD LIMITS

LinkedIn:
- Max 3 hashtags on any post (we target 0–1 for executive register)
- No engagement-bait closing questions ("Agree? Drop a comment!")
- No carousel posts that could be a single well-written post
- No connection request messages with a pitch in the first message

Email:
- No subject lines with all caps or excessive punctuation
- No more than one link in a cold outreach email
- Unsubscribe mechanism required in all marketing emails (legal)
- Never send from a personal address without disclosure

Paid social:
- All claims must be approved by [owner] before going live
- No before/after imagery without written consent
- Testimonials in ads require written approval on file

X (Twitter):
- No threads longer than 7 posts without a genuine reason
- No quote-tweeting a competitor to dunk
- Personal opinions stay in personal accounts, not brand accounts

Client deliverables:
- Every deck includes confidentiality note in footer
- Every report includes data source disclosure
- No placeholder copy ships — "TBD" or "lorem ipsum" = automatic hold

LAYER 6 — QUALITY FLOOR
The minimum bar any piece of content must clear before shipping.
These are not style preferences. Pieces that fail these don't ship.

[ ] Does the first sentence earn the second? (No scene-setting intros)
[ ] Is there exactly one CTA? (Not zero, not three)
[ ] Does it pass the Authorship Test? (Only we could have written this)
[ ] Is every claim backed by a real example, number, or quote?
[ ] Has it been read aloud? (If it sounds robotic → rewrite)
[ ] Does it pass the Cliché Scan? (See /identity Layer Dimension 8)
[ ] If it contains AI-generated language, has it been reviewed by a human? (Yes = proceed / No = hold)
```

### Step 2 — Escalation protocol

What happens when a piece of content crosses a line?

```
ESCALATION LEVELS:

Level 1 — Style violation (forbidden phrase, wrong register):
→ Writer fixes before the next review checkpoint. No escalation.

Level 2 — Claim constraint violation (unverified stat, missing approval):
→ Hold the piece. Flag to [content lead name]. Do not ship until resolved.
→ Resolution time: same day if possible, 24-hour max.

Level 3 — Legal or compliance flag:
→ Immediate hold. No exceptions.
→ Flag to [founder / legal contact].
→ Do not ship until written clearance received.

Level 4 — Client data or reputation risk:
→ Immediate hold and brief [founder name] personally.
→ Document the issue with timestamp.
→ No public statement without founder review.
```

### Step 3 — Rules maintenance cadence

Rules go stale when positioning shifts, products change, or legal context evolves.

```
MAINTENANCE SCHEDULE:

Review trigger: Any of the following:
- Repositioning completed (chains from /positioning-workshop)
- New platform added to content mix
- Legal or compliance event
- New regulated industry client onboarded
- Quarterly audit (add to /l10 rocks)

Review owner: [name]
Review process: Compare Rules Card against last 10 shipped pieces. Any violations found → update Layer 1 or Layer 6.
```

---

## Kill Criteria

Kill the Rules Card draft and return to source if:
- Layer 1 forbidden list has fewer than 10 entries — you haven't looked hard enough
- Layer 3 (legal compliance) is marked "none" for an industry-regulated brand — this is a liability
- Layer 6 quality floor says "it depends" — every floor item must be binary pass/fail
- Rules contradict the Voice Card from /identity — rules must extend voice, not override it. If they conflict, fix the Voice Card first.

---

## Best Client Test
If your best client read your Rules Card, would they say "that's exactly the kind of brand I trust with our content"?
- YES → the rules reflect genuine brand values.
- NO → you're writing compliance theater. Rules should be specific, grounded, and earned — not performative.

## Revenue Gate
- **A:** Documented rules reduce legal exposure and proposal cycle time — clients ask for governance docs at contract stage.
- **B:** Clear rules reduce revision rounds across retained accounts (direct margin improvement).
- **C:** Rules documentation reduces onboarding time for writers and AI tools — measurable burn reduction.
- **D:** Rules created for their own sake with no connection to shipped content → kill. Rules without enforcement are decoration.

## Maintainability Check
- Can a new writer read the Rules Card and self-assess a piece without asking anyone?
- Can the escalation protocol be followed without a Slack message to a founder?
- Is the maintenance cadence owned by a named person, not "the team"?
- If no → the Rules Card isn't operational yet.

---

## Chains to
→ `/identity` — forbidden phrases in Layer 1 extend the Voice Card's Dimension 8
→ `/brand-check` — Rules Card is the scoring rubric for Dimensions 2, 5, and 6
→ `/brief-review` — quality floor in Layer 6 is the minimum bar for Output Review
→ `/context-setup` — load Rules Card as Layer 2 of the brand context stack
→ `/content-governance` — escalation protocol in Step 2 feeds the governance SLA
