---
name: experiment-designer
version: 0.2.0
description: >
  Designs rigorous low-risk growth experiments. Scientific method + YC "do
  things that don't scale". Run before any new campaign, channel test, or
  pricing change. Trigger on: "let's test this", "should we try X", "how do
  we know if this works", "design an experiment", "build a test", "validate this".
inputs:
  - Growth goal or hypothesis
  - Current funnel metrics (if available)
  - Available tools and budget
outputs:
  - Clear hypothesis statement
  - Primary + guardrail metrics
  - Success and kill criteria
  - Minimum viable test spec
  - Launch checklist
  - Revenue Gate + Best Client Test filter
  - Notion/Airtable-style experiment template
allowed-tools:
  - Bash
  - Read
  - Write
  - Glob
  - AskUserQuestion
---

# Experiment Designer
*Scientific method + YC "do things that don't scale" + Garry Tan's "boil the lake" completeness principle*

> *"Every campaign without a kill criterion is a hobby."*

A good experiment is falsifiable. If you can't define failure before you start, you'll rationalize your way through it. Define the kill criterion first. Then design the test.

---

## Process

### Step 1 — Write the hypothesis

Use this format — no exceptions:
```
"We believe that [specific action] will result in [measurable outcome]
for [specific segment] because [reason based on evidence or observation].
We will know this is true when [metric] reaches [specific number]
within [time period]."
```

Bad hypothesis: "We think posting more on LinkedIn will get us more clients."
Good hypothesis: "We believe that posting one case study per week about on-time delivery rates will increase discovery call bookings from Marketing Directors in the Philippines by 20% over 4 weeks, because our last case study post generated 3 inbound leads."

### Step 2 — Define metrics

**Primary metric:** The ONE number that tells you if the experiment worked.
(Discovery calls booked / trial signups / reply rate / conversion rate)

**Guardrail metrics:** What must NOT get worse while you're running this.
(Unsubscribe rate / support tickets / client NPS / burn rate)

If your guardrail metric breaks → stop the experiment immediately regardless of primary metric.

### Step 3 — Set success and kill criteria

```
SUCCESS: Primary metric improves by [X]% over [Y] days
         → Double down: allocate more budget/time to this channel

KILL: Primary metric stays flat or declines after [N] samples or [Y] days
      → Stop immediately, run /cohort-review to understand why

SAMPLE SIZE NOTE: For conversion tests, you need ~300 samples for 95%
                  confidence. For qualitative signals (reply rates, DM
                  responses) — 30 attempts gives directional signal.
                  Don't call it early.
```

### Step 4 — Minimum viable test spec

What is the SMALLEST version of this experiment that can still falsify the hypothesis?

```
CHANNEL: [Where this runs]
AUDIENCE: [Exact segment — not "marketers", say "Marketing Directors at 
           50-200 person B2B SaaS companies in the Philippines"]
COPY VARIANTS: [A = control, B = test — one variable changed only]
DURATION: [Days]
BUDGET: [₱X or $X or "0 — organic only"]
TRACKING: [How you'll know what happened — UTM, Calendly source, 
           spreadsheet tally, PostHog event]
OWNER: [Who runs this — not "the team"]
```

### Step 5 — Launch checklist

- [ ] Hypothesis written in standard format
- [ ] Primary metric defined and trackable
- [ ] Guardrail metrics defined
- [ ] Kill criterion set before launch
- [ ] Audience segment locked (specific, not broad)
- [ ] One variable changed — not three
- [ ] Tracking set up before first asset goes live
- [ ] Owner named
- [ ] Review date calendared (when you check results)

### Step 6 — Experiment template (Notion/Airtable)

```markdown
## Experiment: [Name]
**Status:** Planning / Running / Complete / Killed
**Owner:** [Name]
**Start date:** [Date]
**Review date:** [Date]

### Hypothesis
[Full hypothesis statement]

### Metrics
- Primary: [Metric] → Target: [Number]
- Guardrail: [Metric] → Must stay above: [Number]

### Success criteria
[Specific threshold]

### Kill criteria
[Specific threshold or date]

### Results
[Fill in after experiment]

### Decision
[ ] Double down  [ ] Kill  [ ] Iterate

### Learnings
[What we now know that we didn't before]
```

---

## Kill Criteria

Kill the experiment design if:
- The hypothesis has multiple variables (can't isolate cause)
- You can't track the primary metric without manual effort
- The "success criteria" is "we'll know it when we see it"
- The audience is "everyone who might care"
- Budget or timeline makes it impossible to reach statistical significance

---

## Best Client Test
Would your best client be the primary audience for this experiment?
- YES → proceed
- NO → redefine the audience segment or reclassify to Revenue Gate C/D

## Revenue Gate
- **A:** Test designed to close a client in 30 days (direct response, discovery call CTA)
- **B:** Test building toward close in 60–90 days (nurture, case study, trust signal)
- **C:** Brand test (no direct close measurement — awareness play)
- **D:** Test where you can't define success → kill before it starts

## Maintainability Check
- Can the owner run this experiment without asking you for clarification?
- Is the tracking simple enough to survive a busy week?
- If no → simplify the spec before launching.

---

## Chains to
→ `/cohort-review` — analyze results once data comes in
