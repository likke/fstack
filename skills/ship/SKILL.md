---
name: ship
description: >
  Release ritual for small teams. Makes every deployment documented,
  reversible, and client-safe. Protects your best accounts from surprise
  breakage. Trigger on: "we're shipping", "ready to deploy", "about to push",
  "ship this", "release this", "go live with".
---

# Ship Ritual
*Adapted from Garry Tan's gstack `/ship` — tests, PR, changelog, post-ship monitoring.*

> *"Shipping is a skill, not an event. Most teams ship badly — no PR description, no test count, no changelog, no release notes. gstack makes shipping a repeatable, documented ritual."*
> — Garry Tan, gstack

On a small team, every deployment that goes wrong becomes a founder emergency. This ritual catches obvious failures before they become client calls.

## Why This Exists
On a small team, every deployment that goes wrong becomes a founder emergency. This ritual catches obvious failures before they become client calls.

## Pre-Ship Checklist

### 1. The 5-Minute Smoke Test
- [ ] Does the happy path work?
- [ ] Does your best client's account work? (Always test the healthiest account)
- [ ] Does the free tier work?
- [ ] Does it work on mobile?
- [ ] Are there any console errors?

### 2. The Rollback Plan
- [ ] Can we roll back in under 5 minutes?
- [ ] Is there a database migration? (If yes → backup confirmed?)
- [ ] What's the worst case if this breaks? (Data loss? Visible downtime? Silent failure?)

### 3. The Communication Check
- [ ] Does the founder/decision-maker know this is shipping?
- [ ] Are there any active client deliveries in the next 4 hours?
- [ ] If something breaks, who do we tell first?

## Ship Output Format
```
WHAT'S SHIPPING: [plain English — what does this change for users?]
BRANCH/PR: [reference]

SMOKE TEST: Pass / Fail / Skipped (reason)
ROLLBACK PLAN: [how and how fast]
DATABASE MIGRATION: Yes / No — [backup status if yes]
WORST CASE: [what breaks if this fails]

BEST CLIENT IMPACT: None / Low / Medium / High
ACTIVE DELIVERY CONFLICT: None / [describe timing]

DECISION-MAKER NOTIFIED: Yes / No
SHIPPING NOW: Yes / Waiting for [X]

POST-SHIP CHECK (30 min after deploy):
- [ ] Error rate normal?
- [ ] Core delivery pipeline working?
- [ ] Any client support messages?
```

## Hard Rules
- Never ship during an active delivery window for your top clients.
- Database migrations always require a backup confirmation first.
- If test count decreased from last ship → explain why or fix tests first.
- Any change to the core delivery pipeline → founder must be aware or explicitly approve async.
