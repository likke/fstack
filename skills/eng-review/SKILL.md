---
name: eng-review
description: >
  Architecture and safety review for code before it ships to production.
  Simulates the missing senior engineer or CTO. Catches technical debt,
  security gaps, and maintainability issues before they become client emergencies.
  Trigger on: "review this PR", "review this code", "before we ship",
  "architecture review", "is this safe to deploy", "check this".
---

# Engineering Review

## What This Does
Simulates a senior technical review. For small teams where one developer owns the entire codebase, this review protects you from bugs that become client emergencies.

## The Three Questions

### 1. Can your smallest team member maintain this alone?
- Is the code readable without context?
- Are non-obvious parts commented?
- If the developer left today, could someone new understand it in 2 hours?
- If no → simplify before shipping.

### 2. Does it break anything for your best client?
- Does this touch the core delivery pipeline?
- Does it affect client-facing visibility or tracking?
- Does it affect the feature your highest-margin client uses most?
- If yes → require explicit testing on that client's account before deploy.

### 3. Does it introduce a liability?
- Any hardcoded credentials or API keys?
- Any unvalidated user input?
- Any data exposed that shouldn't be?
- Any change that could cause data loss?

## Review Output Format
```
WHAT IT DOES: [plain English — what does this change for users?]
BRANCH/PR: [reference]

MAINTAINABILITY: Pass / Fail / Needs simplification
- [specific issue if fail]

BEST CLIENT SAFETY: Safe / Needs testing / Risky
- [specific concern if not safe]

LIABILITY CHECK:
- Credentials: Clean / FLAG
- Input validation: Clean / FLAG
- Data exposure: Clean / FLAG
- Data loss risk: None / FLAG

TECHNICAL DEBT ADDED: None / Low / Medium / High
- [describe if medium/high]

TEST COVERAGE: [what is tested vs what isn't]

VERDICT: Ship / Fix first / Revert
REQUIRED BEFORE SHIP: [specific fixes if not clean]
```

## Hard Rules
- Never ship on a Friday before a client deadline.
- Any database migration requires backup confirmation before deploy.
- Any new external API → check rate limits and failure mode first.
- Free tier must work correctly — free tier is your marketing.
- If test count decreased from last ship → explain why or fix tests first.
