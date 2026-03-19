---
name: retro
description: >
  Weekly visibility on team output, client delivery health, and founder
  decisions. Makes invisible work visible. Surfaces what's slipping before
  it becomes a client emergency.
  Trigger on: "weekly retro", "how are we doing", "what shipped this week",
  "retro", "weekly review", "end of week check".
---

# Weekly Retro

## What This Does
Every Friday or Monday morning, pull together what happened across three dimensions: product, delivery, and founder decisions. Make the invisible visible.

## The Three Lenses

### 1. Product (Team output)
- What shipped?
- What was supposed to ship but didn't?
- What's blocked and why?
- Test coverage trend: up/down/flat?
- Technical debt added this week?

### 2. Delivery (Client health)
- For each active client: on-time rate this week? Revision count?
- Any client at negative or low margin? Any migration progress?
- Any client complaints or revision escalations?
- Any at-risk deliveries next week?

### 3. Founder (CEO decisions)
- Outreach: any new discovery calls booked?
- Pipeline: any movement on new client closes?
- Burn: any subscriptions cancelled or reduced?
- Biggest decision made this week: what was it?
- Biggest thing deferred this week: what and why?

## Retro Output Format
```
WEEK OF: [date range]

📦 PRODUCT
Shipped: [list]
Didn't ship: [list]
Blocked: [what and why]
Test coverage: [up / down / flat]
Debt added: [none / low / medium / high]

🎯 DELIVERY
[Client name]: [on-time %] | [avg revision count] | [margin status]
At-risk next week: [any delivery concern]

💰 FOUNDER
Discovery calls booked: [#]
New client leads in pipeline: [#]
Subscriptions/costs cut: [list]
MRR change: [up/down/flat]
Biggest decision: [what]
Biggest deferral: [what and why]

🚦 OVERALL HEALTH
Green: [what's working]
Yellow: [what needs watching]
Red: [what needs immediate action]

NEXT WEEK'S ONE THING: [single most important ship or close]
```

## Escalation Rules
- If any client margin is still negative after 2 retros → founder makes a decision: fix or drop.
- If test coverage drops 2 weeks in a row → address before new features.
- If discovery calls = 0 for 2 weeks → founder reviews outreach with team immediately.
- If best client on-time rate drops below 90% → stop new feature work, fix delivery first.

*The retro is not a performance review. It's a navigation instrument.*
