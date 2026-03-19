---
name: ceo-review
description: >
  Pressure-test any feature idea or product decision before your team
  spends time on it. Applies the Client Test, Maintainability Check,
  and Revenue Gate. Recommends ship/simplify/defer/kill.
  Trigger on: "should we build this", "plan this feature", "is this worth
  building", "sprint review", "review this idea", "is this the right scope".
---

# CEO Review

## What This Does
Before any feature gets assigned to your team, run it through this review. Catches wrong scope, wrong product decisions, and features that will never pay back the time spent.

## The Four Questions

1. **Does your best client need this in their first 7 days?**
   - Yes → consider building
   - No → defer until they ask for it

2. **Can your smallest team member maintain this alone?**
   - Yes → proceed
   - No → simplify scope first

3. **Which Revenue Gate bucket is this?**
   - A: Closes a client in 30 days
   - B: Retains an existing client
   - C: Reduces burn
   - D: Everything else → kill until you hit revenue target

4. **What's the smallest shippable version?**
   - Define the version that proves the thesis with minimum effort.
   - Build that first. Expand only after real usage data.

## Output Format
```
IDEA/FEATURE: [plain English description]

CLIENT TEST: Pass / Fail — [does your best client need this in 7 days?]
MAINTAINABILITY: Pass / Fail — [can your smallest team member own this?]
REVENUE GATE: A / B / C / D

SCOPE OPTIONS:
- Full version: [describe] — [effort estimate]
- Smallest shippable: [describe] — [effort estimate]
- Deferred version: [what we skip for now]

RECOMMENDATION: Ship / Simplify / Defer / Kill
ONE-LINE REASON: [why]

IF SHIP:
- Smallest shippable version: [describe]
- Definition of done: [what does "shipped" mean specifically?]
- How do we know it's working: [what signal confirms it's worth expanding?]
```

## Hard Rules
- No building without demand — if no client has asked, it waits.
- No vague scope — if you can't describe what "done" looks like, don't start.
- Ship ugly, fix later — but never ship inaccurate.
- Free tier must work — free tier is your marketing.
