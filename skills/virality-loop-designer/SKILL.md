---
name: virality-loop-designer
version: 0.2.0
description: >
  Analyzes product for natural referral and viral potential. Designs concrete
  loops that turn users into acquisition channels. Run when growth is
  plateauing or when you want to reduce paid acquisition dependency.
  Trigger on: "how do I get users to refer", "design a referral program",
  "viral loop", "k-factor", "growth loop", "how do I get word of mouth",
  "referral mechanic", "make this shareable".
inputs:
  - Product description and core loop
  - Current metrics (invite rate, k-factor if known)
  - Target user behavior
outputs:
  - Current viral coefficient diagnosis
  - 3 new loop ideas with incentive copy, success metric, and effort estimate
  - Best Client Test + Revenue Gate scoring for each loop
  - Prioritized recommendation with quick MVP spec
allowed-tools:
  - Bash
  - Read
  - Write
  - Glob
  - AskUserQuestion
---

# Virality Loop Designer
*Andrew Chen's growth loop framework + YC "make something people want to share" + Garry Tan's completeness principle*

> *"If your users aren't bringing you more users, you have a product — not a growth engine."*

Virality isn't luck. It's architecture. Every product has moments where a user could bring another user — most products just never build the door. This skill finds those moments and builds the door.

---

## Process

### Step 1 — Diagnose current viral coefficient

```
CURRENT STATE:
Total users acquired last 30 days: _____
Users acquired via referral/word-of-mouth: _____
Referral rate: [referral / total] = _____%

K-FACTOR (if known): _____
(k-factor = invites sent per user × invite acceptance rate)
(k-factor > 1 = viral. k-factor 0.2–0.5 = decent. k-factor < 0.1 = no viral loop)

CURRENT VIRAL MECHANISMS (if any):
- [List anything that currently causes sharing — even passively]

DIAGNOSIS:
- k-factor > 1: You have virality. Optimize and protect it.
- k-factor 0.2–0.9: Viral potential exists. Design a real loop.
- k-factor < 0.2: No viral signal. Start from zero — find the natural share moment.
```

### Step 2 — Find the natural share moments

Walk through the user journey. Where does value become visible to others?

Ask: "When does using this product naturally involve or impress someone else?"

```
SHARE MOMENT AUDIT:
[ ] Does the output of the product look good when shared? (shareable artifacts)
[ ] Does the product require collaboration? (co-creation invite)
[ ] Does the product create proof of achievement? (badge, certificate, milestone)
[ ] Does the product let users compare or compete? (leaderboard, benchmark)
[ ] Does the product let users give something to others? (gift, recommendation, report)
[ ] Is there a result the user would want to brag about? (outcome worth showing off)
```

The share moments you checked are your loop candidates.

### Step 3 — Design 3 loops

For each loop candidate:

```
LOOP [A/B/C]: [Name]

MECHANISM: [What triggers the share moment]
INCENTIVE: 
  - For sender: [What they get for sharing]
  - For recipient: [What they get for accepting]
INCENTIVE COPY: 
  - CTA (sender): "[Exact button text or message]"
  - Message (recipient): "[Exact invite message — 2 sentences max]"
SUCCESS METRIC: [How you'll know this loop is working]
  Primary: [metric + target]
  Timeframe: [days to first signal]
IMPLEMENTATION EFFORT: Low (< 1 day) / Medium (1–5 days) / High (> 5 days)
DEPENDENCY: [What needs to be true for this to work]

BEST CLIENT TEST:
Would your best client send this to someone they respect?
YES / NO — [reason]
If no → kill this loop.

REVENUE GATE:
A (drives direct acquisition → closes client in 30 days)
B (drives awareness → 60–90 day path)
C (brand / engagement only)
D (unlikely to produce meaningful referrals) → kill

QUICK MVP SPEC:
Smallest version we can ship to test this loop:
[2–3 sentences — what's the minimum that's still real?]
```

### Step 4 — Rank and recommend

```
RECOMMENDED LOOP: [A/B/C]
WHY: [2 sentences — highest Best Client Test score + lowest implementation effort + Revenue Gate A or B]

IMPLEMENTATION ORDER:
1. [Highest priority loop — ship first]
2. [Second priority — ship after validating #1]
3. [Lowest priority — or kill if #1 works]

SUCCESS CRITERIA FOR RECOMMENDATION:
Run for [X] days. If k-factor doesn't move from baseline by [Y]% → kill and try loop #2.
```

---

## Reference: Loop Types

| Loop Type | Mechanism | Best for |
|-----------|-----------|----------|
| Shareable artifact | Output is worth showing off | Reports, certifications, scorecards |
| Collaborative invite | Product requires another person | Shared workspaces, co-editing |
| Give-a-gift | User can gift access/value | Free trial, credits, report |
| Social proof | Milestone worth bragging about | Achievements, leaderboards |
| Referral credit | Explicit incentive to invite | SaaS products with clear LTV |
| Embed/widget | Product output lives elsewhere | Tools that create embeddable assets |

---

## Kill Criteria

Kill a loop design if:
- The incentive feels manipulative ("invite 5 friends to unlock a feature")
- Your best client would not send the invite message to someone they respect
- The implementation effort is HIGH and k-factor is already < 0.1 (fix product before building loops)
- Revenue Gate is D

---

## Best Client Test
Would your best client share this product with a peer without being incentivized?
- YES → you have natural virality. Amplify it.
- NO → figure out why. Is the output private? Is there no shareable artifact? Fix that first.

## Revenue Gate
- **A:** Loop drives direct new client acquisition (referred user is ICP, converts in 30 days)
- **B:** Loop drives brand awareness and indirect pipeline (60–90 day path)
- **C:** Loop increases engagement but no clear acquisition path
- **D:** Loop is hypothetical and has no user behavior to anchor it → don't build yet

## Maintainability Check
- Can the loop run without manual intervention once set up?
- Can your smallest team member monitor the success metric weekly?
- If no → simplify the mechanic before shipping.
