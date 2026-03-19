---
name: sprint-plan
description: >
  Plan a sprint for your team against one clear goal. Applies the Client
  Test, Maintainability Check, and Revenue Gate to every task before it
  gets assigned. Outputs a prioritized task list with explicit deferrals.
  Trigger on: "plan this sprint", "what should [name] work on", "weekly tasks",
  "sprint planning", "what do we build this week".
---

# Sprint Plan
*Adapted from YC's weekly check-in culture + EOS Traction + Garry Tan's gstack sprint principles.*

> *"What's the one thing you're shipping this week?"*
> — YC weekly check-in format

YC's weekly check-in is ruthless: one goal, one week, did you hit it or not? No excuses, no context, just the number. This skill builds that discipline into your sprint planning — one goal per sprint, explicit deferrals, visible blockers.

## What This Does
Before handing your team work for the week, run it through this review. Every task gets tested against: does it close a client, retain a client, or reduce burn? Everything else gets explicitly deferred.

## The Process

### Step 1 — Define the sprint goal
One sentence. Not a list of tasks. A single outcome:
- "Ship the delivery tracking feature to production"
- "Book 3 discovery calls from the outreach campaign"
- "Reduce OceanJet delivery time by 30%"

If you can't write one sentence → you don't have a goal, you have a to-do list.

### Step 2 — List all tasks
Everything that's been asked for, requested by clients, backlogged. Get it all out.

### Step 3 — Apply the filters to each task

**Filter 1 — Client Test:** Does your best client need this in their first 7 days?
**Filter 2 — Maintainability:** Can your smallest team member own this?
**Filter 3 — Revenue Gate:** A (closes client), B (retains client), C (reduces burn), D (kill)

Tasks that fail → explicitly deferred. Not forgotten. Deferred.

### Step 4 — Output

```
SPRINT GOAL: [one sentence]
WEEK OF: [dates]
REVENUE BUCKET: A / B / C (what category does this sprint primarily serve?)

TASKS (priority order):
1. [Task] — [owner] — [effort: X hrs] — [why: closes/retains/reduces burn]
2. [Task] — [owner] — [effort: X hrs] — [why]
3. ...

EXPLICITLY NOT IN THIS SPRINT:
- [task] — deferred because: [reason]
- [task] — deferred because: [reason]

DEFINITION OF DONE FOR THIS SPRINT:
[what does "success" look like on Friday?]

BLOCKERS TO CALL OUT NOW:
[anything that will stop this sprint from completing?]
```

## Hard Rules
- One sprint goal. If there are two goals, there are zero goals.
- No task without an owner and an effort estimate.
- Every deferral must be explicit — no silently dropping things.
- If a task has been deferred 3 sprints in a row → either kill it or escalate it to the top.
- Protect your best client's delivery pipeline above all else.
