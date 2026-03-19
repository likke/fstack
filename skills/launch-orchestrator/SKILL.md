---
name: launch-orchestrator
version: 0.2.0
description: >
  Builds and sequences a realistic launch campaign for indie and early-stage
  products. Optimized for Product Hunt, X, LinkedIn, Reddit, and founder
  networks. Run when shipping anything worth announcing. Trigger on: "help me
  launch", "plan a launch", "how do I announce this", "launch strategy",
  "Product Hunt prep", "launch sequence", "how do I get traction on launch day".
inputs:
  - Product one-liner and key benefit
  - Launch date and time
  - Target communities
  - Existing audience size and assets
outputs:
  - Timed rollout plan (-7 days to Day 0 to +3 days)
  - Copy variants for PH title/tagline, X thread, LinkedIn post
  - Seeding list template (50 relevant accounts to DM or tag)
  - "Would Garry RT this?" filter on your hook
  - Asset checklist
  - Demo-day 2-min story arc
  - Post-launch retro prompts
---

# Launch Orchestrator
*Garry Tan's gstack launch philosophy + YC Demo Day storytelling + "do things that don't scale" outreach*

> *"A launch without coordination is just noise with a countdown."*

A great launch is 80% prep and 20% execution. The day-of is just following a plan you already built. If you're writing copy the night before launch, you already lost.

---

## Process

### Step 1 — Hook filter: "Would Garry RT this?"

Before building the launch plan, test the hook.

Garry Tan RTs things that are:
- Specific (not "we built an AI tool")
- Counterintuitive or surprising (challenges an assumption)
- Tied to a real problem real people have
- Under 15 words for the core claim

Run your hook through this filter:
```
HOOK: [Your current one-liner or launch headline]

GARRY TEST:
- Is it specific? YES / NO → if no, name the exact person it's for
- Is it surprising? YES / NO → if no, what's the unexpected angle?
- Real problem? YES / NO → can you name 3 people who have it right now?
- Under 15 words? YES / NO → trim ruthlessly

REVISED HOOK: [Improved version]
```

If it fails all four → stop. Rewrite the hook before building the sequence.

### Step 2 — Launch timeline (-7 to +3)

```
DAY -7: FOUNDATION
- [ ] Landing page live with the revised hook
- [ ] Asset checklist complete (see below)
- [ ] Seeding DMs drafted (not sent yet)
- [ ] PH hunter identified + scheduled (if launching on PH)
- [ ] Internal team briefed — everyone knows their role

DAY -3: WARM-UP
- [ ] Tease post on X/LinkedIn: "Something's coming Monday..."
- [ ] DM 10 most engaged followers/community members: preview + ask to support
- [ ] Schedule all launch day posts (don't wing it live)
- [ ] Test all links, demo video, signup flow end-to-end

DAY -1: FINAL CHECK
- [ ] All copy finalized and approved
- [ ] PH submission queued (launches at 12:01 AM PST)
- [ ] Team in Slack/Discord channel — ready to upvote, comment, share
- [ ] Personal network notified: "Tomorrow. Please support."

DAY 0: LAUNCH
- [ ] PH goes live at 12:01 AM PST — upvote immediately
- [ ] X thread posted at 9 AM (your audience's time zone)
- [ ] LinkedIn post at 10 AM
- [ ] Reply to every comment within first 4 hours — no exceptions
- [ ] DM seeding list: 50 accounts (10 in first hour, 40 throughout the day)
- [ ] Post in 3-5 relevant communities (Reddit, Slack, Discord, Facebook groups)
- [ ] Share in personal networks: WhatsApp, Telegram, direct messages

DAY +1: MOMENTUM
- [ ] Thank you post: results so far + lessons
- [ ] Share a data point: "X signups in 24 hours"
- [ ] Reply to everyone who commented or shared

DAY +3: RETRO
- [ ] Run /retro with launch metrics
- [ ] Identify highest-converting channel
- [ ] Kill lowest-performing channel
- [ ] Plan follow-up content cycle
```

### Step 3 — Copy variants

**Product Hunt:**
```
TITLE: [Product name — max 5 words]
TAGLINE: [One sentence — max 60 chars — what it does + for who]
DESCRIPTION OPENER: [First 2 sentences — lead with the pain, not the feature]
FIRST COMMENT: [Founder story — 3 paragraphs: problem, insight, what you built]
```

**X Thread (opener only — most important line):**
```
HOOK TWEET: [One sentence — surprising, specific, problem-first]
THREAD STRUCTURE:
1. Hook (the problem)
2. Why existing solutions fail
3. What you built (one sentence)
4. Key benefit or stat
5. Who it's for
6. Link + CTA
```

**LinkedIn Post:**
```
OPENING LINE: [No "I'm excited to announce" — lead with the pain or insight]
STRUCTURE:
- Line 1: The hook (pain or counterintuitive statement)
- Lines 2-4: The story (brief, specific, personal)
- Lines 5-7: What you built and why it's different
- Line 8: Who it's for
- Final line: CTA with link
```

### Step 4 — Seeding list template

Build a list of 50 relevant accounts to DM or tag on launch day.

**Categories:**
- 10 × journalists/writers who cover your space
- 10 × founders who might use or share it
- 10 × community influencers (active in your target communities)
- 10 × past customers or beta users
- 10 × direct ICP decision-makers (potential buyers)

**DM template:**
```
Hey [Name] — launching [product] today on [PH/X/etc]. It [one-line benefit].
Given your work on [relevant thing], thought you'd find it interesting.
Would mean a lot if you checked it out: [link]
```

### Step 5 — Asset checklist

- [ ] Demo video (60–90 seconds — shows the product working, not a walkthrough)
- [ ] GIF or screenshot for PH thumbnail
- [ ] Social card (OG image for link previews)
- [ ] Landing page with the revised hook (above the fold, CTA visible)
- [ ] Signup or waitlist working + confirmation email set up
- [ ] Analytics tracking live before launch

### Step 6 — Demo-day 2-min story arc

Structure for any live demo or pitch video:
```
0:00–0:20 — THE PROBLEM: "Most [target person] struggle with [specific pain]."
0:20–0:40 — THE INSIGHT: "We discovered that [unexpected truth about the problem]."
0:40–1:10 — THE DEMO: Show the product solving exactly that problem. No feature tour.
1:10–1:40 — THE PROOF: One real result. Number, name, or story.
1:40–2:00 — THE ASK: "Here's how to get started." [Link or CTA]
```

---

## Kill Criteria

Kill the launch plan if:
- The hook doesn't pass the Garry test
- You don't have a working product to demo (waitlist launches for unknown founders = low signal)
- Your seeding list is under 20 people you can actually reach
- The launch timeline is under 3 days away and assets aren't ready

---

## Best Client Test
Would your best client share this launch post without being asked?
- YES → your hook is landing. Ship it.
- NO → back to Step 1. The hook isn't right yet.

## Revenue Gate
- **A:** Launch with direct CTA to paid signup or discovery call
- **B:** Launch with free trial or waitlist (qualify → convert in 60–90 days)
- **C:** Launch for brand/awareness (no direct revenue path — valid for community building)
- **D:** Launch with no clear CTA or audience → don't launch until this is fixed

## Maintainability Check
- Can Charlene (or whoever runs ops) execute the Day 0 tasks without you being available?
- Is the sequence documented well enough to reuse for the next launch?
- If no → document the runbook before pressing go.

---

## Chains to
→ `/retro` — review results on Day +3
→ `/experiment-designer` — test which channel performed best
