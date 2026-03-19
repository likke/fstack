---
name: cohort-review
version: 0.2.0
description: >
  Analyzes cohort and segment data to find growth truth. Turns messy metrics
  into "default alive" signals. Run weekly during L10 and after any experiment.
  Trigger on: "analyze our metrics", "what do the numbers say", "are we default
  alive", "which channel is working", "cohort analysis", "review our data",
  "where are we leaking".
inputs:
  - Raw metrics dump (Stripe export, PostHog/Mixpanel CSV paste, or descriptive summary)
  - Key segments (acquisition channel, plan type, geo)
  - Time periods to compare
outputs:
  - Which cohorts are profitably growing (LTV:CAC > 3x, retention curves)
  - Highest-leverage segment or channel right now
  - Default alive runway projection (months at current burn)
  - Top 3 recommended next experiments
  - Red flags (leaky buckets, churn spikes)
  - Retro-style summary for weekly L10
---

# Cohort Review
*Adapted from Paul Graham's "default alive" framework + YC's "talk to users" principle applied to data*

> *"Vanity metrics are comfort food. Cohort data is the blood test."*

MRR going up means nothing if your best cohort is churning at 30%. The numbers tell a story — but only if you ask them the right questions. This skill asks them.

---

## Process

### Step 1 — Default Alive Check

The first question is always the same:
```
MONTHLY REVENUE: ₱_____ / $______
MONTHLY BURN: ₱_____ / $______
CASH IN BANK: ₱_____ / $______
MONTHS OF RUNWAY: [cash / (burn - revenue)]

DEFAULT ALIVE: YES (revenue > burn or growing fast enough) / NO
DEFAULT ALIVE AT CURRENT GROWTH RATE: YES / NO
```

If default alive = NO → stop. This is the only number that matters. Everything else is decoration.

### Step 2 — Cohort profitability check

For each acquisition cohort (channel, campaign, time period):
```
COHORT: [Name — e.g. "Waalaxy LinkedIn Q1 2026"]
ACQUISITION COST: ₱_____ / $______
CUSTOMERS ACQUIRED: _____
AVG MONTHLY REVENUE PER CUSTOMER: ₱_____ / $______
MONTHS TO PAYBACK: [CAC / monthly revenue per customer]
LTV (12-month estimate): [monthly revenue × 12 × retention rate]
LTV:CAC RATIO: [LTV / CAC]

VERDICT:
- LTV:CAC > 3x → Healthy. Double down.
- LTV:CAC 1–3x → Watch. Don't scale yet.
- LTV:CAC < 1x → Kill. You're buying customers at a loss.
```

### Step 3 — Retention curve

For each cohort, track what % of customers are still paying at:
- Month 1: _____%
- Month 3: _____%
- Month 6: _____%
- Month 12: _____%

```
RETENTION PATTERN:
- Gradual decline → expected. Monitor floor (where it stabilizes).
- Cliff drop at month 1 or 2 → onboarding failure. Fix before scaling.
- Cliff drop at month 6 → value isn't sticking. Talk to churned users NOW.
- Flat after month 3 → strong PMF signal. Scale this cohort.
```

### Step 4 — Leaky bucket scan

Walk through the funnel. Find the biggest drop-off:
```
[Stage] → [Stage]: ____% conversion
[Stage] → [Stage]: ____% conversion ← RED FLAG if < industry benchmark
[Stage] → [Stage]: ____% conversion
```

The biggest leak is your highest-leverage fix. Everything else is optimization.

### Step 5 — Highest-leverage segment

```
TOP PERFORMING SEGMENT: [Name]
WHY: [LTV, retention, acquisition cost, or growth rate]
WHAT TO DO: [Specific action — double outreach, run targeted campaign, build feature for this segment]

KILL SEGMENTS (negative ROI or no growth signal):
- [Segment] → [Reason to kill or pause]
```

### Step 6 — Top 3 experiments

Based on the data, the three highest-leverage things to test next:
```
1. [Experiment] → [Expected impact] → Chains to /experiment-designer
2. [Experiment] → [Expected impact] → Chains to /experiment-designer
3. [Experiment] → [Expected impact] → Chains to /experiment-designer
```

### Step 7 — L10 summary (for weekly meeting)

```markdown
## Cohort Review — [Date]

**Default alive:** YES / NO
**Runway:** X months at current burn/growth

**Green (working):**
- [What's growing and profitable]

**Yellow (watch):**
- [What needs monitoring]

**Red (fix now):**
- [Leaky buckets, churn spikes, unprofitable cohorts]

**Decision:**
- Double down on: [segment/channel]
- Kill or pause: [segment/channel]
- Run next: [experiment]
```

---

## Kill Criteria

Stop analyzing and act if:
- Default alive = NO and runway < 3 months → this is a survival conversation, not an analysis
- LTV:CAC < 1x in all cohorts → the business model is broken, not the marketing
- Churn cliff at month 1 → ship a fix before running a single new acquisition campaign

---

## Best Client Test
Is your best client in your highest-LTV cohort?
- YES → good signal. Study that cohort obsessively.
- NO → you're acquiring the wrong customers. Fix targeting before scaling.

## Revenue Gate
- **A:** Analysis that reveals an immediate action to close a client in 30 days
- **B:** Analysis that reveals a 60–90 day growth lever
- **C:** Analysis that confirms brand/awareness investment is working
- **D:** Analysis with no actionable output → stop and reframe the question

## Maintainability Check
- Can your team reproduce this analysis in 30 minutes next month?
- Is the data source reliable and accessible without you?
- If no → build a simple dashboard before the next review.

---

## Chains to
→ `/retro` — bring findings into weekly L10
→ `/experiment-designer` — design tests based on findings
