---
name: positioning-workshop
version: 0.2.0
description: >
  Fast structured positioning session. April Dunford-style JTBD + YC "make
  something people want". Run before any new launch, messaging refresh, or
  when leads keep saying "what do you actually do" Trigger on: "sharpen my
  positioning", "what's my positioning", "how do I explain what I do",
  "nobody gets what we do", "messaging isn't landing", "help me position this".
inputs:
  - Current product or feature description
  - Target user profile or best client
  - 1-3 competitors (name + one-line description)
  - Any existing messaging or landing page copy
outputs:
  - 3 differentiated positioning options ranked by Best Client Test
  - One-sentence version of each
  - "Why now" two-sentence justification
  - Competitor 2x2 matrix (better/worse axes)
  - Final recommendation + Revenue Gate bucket
  - Kill recommendation + pivot suggestions if Best Client Test fails
allowed-tools:
  - Bash
  - Read
  - Write
  - Glob
  - AskUserQuestion
---

# Positioning Workshop
*Adapted from April Dunford's "Obviously Awesome" + YC's "make something people want"*

> *"If you can't explain why someone would switch to you in one sentence, you don't have positioning — you have a wishlist."*

Positioning isn't a tagline. It's the answer to: "Why would my best client switch from what they're doing now to this?" If you can't answer that in one sentence, you're not positioned — you're guessing.

---

## Process

### Step 1 — Understand the switch
Ask: "What is the prospect doing RIGHT NOW to solve this problem?"
That is your real competition. Not the SaaS tools you listed. The spreadsheet. The Slack channel. The freelancer. The "we just don't do that" response.

### Step 2 — Find the beachhead
Apply the JTBD frame:
- **Functional job:** What task are they literally trying to accomplish?
- **Emotional job:** How do they want to feel (or stop feeling) when this is done?
- **Social job:** How do they want to appear to their team/boss/clients?

The best positioning speaks to all three. Most only hits one.

### Step 3 — Build 3 positioning options

For each option:
```
POSITIONING OPTION [A/B/C]

One-liner: [Complete this: "For [specific person] who [specific pain],
            [product] is the [category] that [key differentiator].
            Unlike [real alternative], we [proof point]."]

Why now (2 sentences): [What changed in the market/their situation that
                        makes this urgent TODAY?]

Best Client Test: Would your best client immediately say "that's me"?
                  YES / NO / MAYBE — [reason]

Revenue Gate: A (closes in 30 days) / B (60-90 days) / C (brand) / D (kill)
```

### Step 4 — Competitor 2x2 matrix

Pick 2 axes that actually matter to your best client (not the ones that flatter you).

```
              BETTER AT [Axis 1]
                    |
[Competitor A]      |      [YOU]
                    |
WORSE AT ——————————+—————————— BETTER AT
[Axis 2]           |                [Axis 2]
                    |
[Competitor B]      |  [Competitor C]
                    |
              WORSE AT [Axis 1]
```

The box you own should be where your best client actually wants to be. If you're not in that box — your positioning is wrong.

### Step 5 — Final recommendation

```
RECOMMENDED POSITIONING: [Option A/B/C]
ONE-LINER: [Final one sentence]
WHY THIS ONE: [2-3 sentences — why this over the others]
REVENUE GATE: [A/B/C/D]

LAUNCH SIGNAL: Use this on the homepage hero. If conversion doesn't improve
               in 2 weeks → run /experiment-designer to test alternatives.
```

---

## Kill Criteria

Kill the positioning and pivot if:
- Your best client reads it and says "that could be anyone"
- It describes what you DO, not what you SOLVE
- The "why now" is "AI is growing" (too generic — not a real trigger)
- You need 3 sentences to explain the one-liner
- It fails the Revenue Gate (lands in D bucket)

**If kill → pivot suggestions:**
1. Go back to Step 1. What is the prospect actually doing now?
2. Interview your 3 best clients. Ask: "Why did you really switch?"
3. Their words are your positioning. You don't invent it — you find it.

---

## Best Client Test
*Before finalizing: show the one-liner to your best client (or someone who matches the profile).*
- Would they stop scrolling?
- Would they say "that's exactly my problem"?
- If yes → ship it.
- If they shrug → back to Step 2.

## Revenue Gate
- **A:** Positioning that directly closes a client in 30 days (speaks to active pain, clear ROI)
- **B:** Positioning that builds toward a close in 60–90 days (right ICP, early stage)
- **C:** Brand positioning (no direct close — runs on content/awareness)
- **D:** Positioning no one asked for → kill

## Maintainability Check
- Can your smallest team member explain this positioning without a briefing doc?
- Will it still be true in 6 months if the market shifts slightly?
- If no → simplify or anchor to a more durable pain.

---

## Chains to
→ `/experiment-designer` — test the positioning with a real campaign
→ `/launch-orchestrator` — build the launch sequence around this positioning
