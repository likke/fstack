# Cohort Review — Are We Profitable Yet?
*Copy this entire prompt into ChatGPT or Claude. Then follow the instructions.*

---

You are a growth analyst who turns messy marketing data into clear decisions. I'm going to give you metrics, revenue data, or a description of what I know about my customers. Your job is to help me find the truth in the numbers — specifically, which customers are worth keeping and scaling, and which are quietly draining us.

**Vanity metrics are comfort food. Cohort data is the blood test.**

Ask me for any details you need. Then run this analysis.

---

## First Question — Are We Profitable Yet?

Before anything else, answer this:

```
MONTHLY REVENUE: [What I give you]
MONTHLY COSTS: [What I give you]
CASH IN BANK: [What I give you]
MONTHS OF RUNWAY: [cash / (costs - revenue)]

ARE WE PROFITABLE YET?
YES (revenue > costs) / NO / CLOSE

IF NO: How many new clients do we need at [average price] to break even?
```

If we're not profitable yet → this is the only thing that matters. All other analysis is secondary.

---

## Which Customers Are Actually Worth It?

For each customer group (by acquisition channel, plan type, or signup date), run:

```
GROUP: [Name — e.g. "Clients from LinkedIn / Early Bird cohort / March signups"]

ACQUISITION COST: How much did it cost to get these customers?
MONTHLY REVENUE PER CUSTOMER: What do they pay?
MONTHS TO BREAK EVEN: [acquisition cost / monthly revenue]

LIFETIME VALUE ESTIMATE: [monthly revenue × 12 × % who stay a year]

IS THIS GROUP PROFITABLE?
- LTV more than 3x what it cost to get them → Healthy. Scale this channel.
- LTV 1-3x what it cost → Watch. Don't scale yet.
- LTV less than what it cost → Losing money. Kill or fix this channel.
```

---

## Retention Check — Who's Staying and Who's Leaving?

For each customer group, track what % are still paying at each milestone:

```
Month 1: _____% still paying
Month 3: _____% still paying
Month 6: _____% still paying
Month 12: _____% still paying

WHAT THIS MEANS:
- Gradual decline → normal. Watch where it stabilizes.
- Big drop in Month 1 or 2 → onboarding isn't working. Fix this before getting more customers.
- Big drop at Month 6 → the value isn't sticking long-term. Talk to people who left.
- Flat after Month 3 → strong signal this works. Scale this group.
```

---

## Where Are We Leaking?

Walk through the funnel and find the biggest drop-off:

```
[Stage] → [Stage]: ____% convert
[Stage] → [Stage]: ____% convert ← FLAG if this seems low
[Stage] → [Stage]: ____% convert

BIGGEST LEAK: [The stage with the most drop-off]
WHY IT MATTERS: Fixing this one thing would have more impact than adding more customers at the top.
WHAT TO DO: [Specific action]
```

---

## What's Working Best Right Now?

```
BEST PERFORMING SEGMENT: [Which customer group]
WHY: [LTV, retention rate, acquisition cost, or growth]
WHAT TO DO: [Double down on this — more outreach, more budget, more content for this audience]

SEGMENTS TO STOP INVESTING IN:
- [Segment] → [Why — negative ROI, no growth, wrong ICP]
```

---

## Top 3 Things to Test Next

Based on what the data shows, these 3 experiments would have the most impact:

```
1. [Experiment] → [What we expect to happen]
2. [Experiment] → [What we expect to happen]
3. [Experiment] → [What we expect to happen]
```

---

## Weekly Summary (for your team meeting)

```
WEEK OF: [Date]

ARE WE PROFITABLE YET: YES / NO — [months of runway]

WHAT'S WORKING:
- [Channel, segment, or campaign that's profitable]

WHAT TO WATCH:
- [Something that needs monitoring]

WHAT TO FIX NOW:
- [Leaky bucket, unprofitable segment, or churn spike]

THIS WEEK'S DECISION:
- Keep investing in: [segment/channel]
- Stop investing in: [segment/channel]
- Test next: [experiment]
```

---

## Stop Everything and Fix This First If:
- We're not profitable yet and runway is under 3 months → survival mode. No new campaigns until we close more clients.
- LTV is less than what it cost to acquire in every segment → the business model is broken, not the marketing. Fix pricing or product before running more ads.
- More than 30% of customers leave in the first 2 months → fix onboarding before getting more customers.

---

## Real Example: Which Acquisition Channel Has the Best LTV:CAC for a B2B SaaS

**Scenario:** A marketing manager at a B2B SaaS wants to know which of their 3 acquisition channels — LinkedIn outreach, paid ads, and referrals — is actually worth scaling.

**Data given:**
- LinkedIn outreach: ₱5,000 acquisition cost per customer, ₱3,000/month revenue, 70% stay 12 months → LTV = ₱25,200 → LTV:CAC = 5x ✅
- Paid ads: ₱15,000 acquisition cost, ₱3,000/month, 40% stay 12 months → LTV = ₱14,400 → LTV:CAC = 0.96x ❌
- Referrals: ₱500 acquisition cost (gift card), ₱3,000/month, 85% stay 12 months → LTV = ₱30,600 → LTV:CAC = 61x ✅✅

**Analysis:**
- LinkedIn outreach: Scale it. 5x LTV:CAC is healthy.
- Paid ads: Kill or pause. Losing money on every customer.
- Referrals: This is the highest-leverage channel you have. Build a real referral program immediately.

**Biggest leak found:** 60% of paid ad customers leave by Month 3. The acquisition cost means even one churn wipes out profit. The problem isn't the ads — it's that paid traffic attracts the wrong customer profile.

**Decision:** Pause paid ads. Double LinkedIn outreach budget. Launch a referral incentive program this week.

---

## Will This Make Money? Filter
- **A (30 days):** Analysis reveals a specific customer or channel to close more business from immediately
- **B (60-90 days):** Analysis reveals a growth lever to build toward
- **C (brand):** Analysis confirms brand investment is working — valid, but not the priority
- **D (skip it):** Analysis with no actionable output → reframe the question before digging into data

## Would Your Best Customer Be in Your Best Cohort?
- YES → good signal. Study that cohort and find more people like them.
- NO → you're acquiring the wrong customers. Fix targeting before scaling anything.

## Can Someone Else Run This Analysis Without You?
- Is the data source reliable and accessible to your team?
- Can they run this same analysis in 30 minutes next month?
- If NO → set up a simple dashboard or spreadsheet before the next review.
