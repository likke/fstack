---
name: customer-interview-synthesizer
version: 0.2.0
description: >
  Distills raw user call notes and transcripts into actionable strategy.
  Turns expensive small talk into positioning, product, and GTM decisions.
  Run after any batch of user interviews. Trigger on: "synthesize my user
  calls", "what did users say", "analyze my interviews", "what are the
  patterns", "JTBD analysis", "what do users actually want", "synthesize
  this feedback".
inputs:
  - Paste of 5–20 call notes, transcripts, or summary bullets
  - Current best client profile
  - JTBD framework prompt (optional)
outputs:
  - Top 3–5 Jobs-to-be-Done (functional + emotional)
  - Most frequent objections and delight moments
  - Updated best client persona
  - Messaging and positioning implications
  - Flag if talking to wrong segment (Revenue Gate fail)
  - Prioritized next questions for future calls
  - Notion-style synthesis document
---

# Customer Interview Synthesizer
*April Dunford's JTBD framework + YC's "talk to users" + Paul Graham's "make something people want"*

> *"Talking to users without synthesizing is just expensive small talk."*

Interviews are raw material. The synthesis is the product. Without a structured process for turning call notes into decisions, you'll remember the last thing someone said and ignore everything else. This skill forces the synthesis.

---

## Process

### Step 1 — Extract the raw signals

For each interview in the batch, pull out:
```
INTERVIEW [#]: [Name/role if available]
PROBLEM THEY DESCRIBED: [Exact quote or close paraphrase]
WHAT THEY'RE DOING NOW TO SOLVE IT: [Their current workaround]
MOMENT OF DELIGHT: [If any — what made them say "yes, exactly"]
OBJECTION OR HESITATION: [What made them slow down or push back]
UNEXPECTED THING THEY SAID: [Anything you didn't anticipate]
```

Do this for every interview before looking for patterns. Don't cluster yet.

### Step 2 — Find the Jobs-to-be-Done

For each distinct job you're hearing, complete this frame:
```
JOB [#]: [Name]

FUNCTIONAL JOB:
"When I [situation], I want to [functional goal], so I can [outcome]."

EMOTIONAL JOB:
"When I [situation], I want to feel [emotional state] because [underlying fear or desire]."

SOCIAL JOB:
"When I [situation], I want to appear [how they want to look to others]."

FREQUENCY: [How often does this come up across interviews?]
INTENSITY: [High / Medium / Low — how much do they care?]
QUOTES: [Best 1–2 direct quotes]
```

Rank by frequency × intensity. Top 3–5 are your product and messaging priorities.

### Step 3 — Objections and delight moments

```
MOST COMMON OBJECTIONS (ranked):
1. [Objection] — heard in [X/N] interviews
   → What this really means: [underlying fear or concern]
   → How to address: [positioning change, feature, or proof point]

2. [Objection] — heard in [X/N] interviews

DELIGHT MOMENTS (what made them lean in):
1. [Moment] — heard in [X/N] interviews
   → Why it resonated: [what job it speaks to]
   → How to amplify: [messaging, feature, onboarding change]
```

### Step 4 — Update the best client profile

Based on this batch:
```
BEST CLIENT PROFILE (updated):

Title/Role: [Most common role among high-engagement interviews]
Company size: [Range]
Industry: [Specific — not "B2B"]
Situation: [What's happening in their world that makes this urgent]
Primary JTBD: [The #1 job from Step 2]
Current workaround: [What they're doing without you]
Switch trigger: [What would make them switch to you today]
Red flag (wrong segment): [Who you DON'T want — and why they showed up]
```

### Step 5 — Messaging and positioning implications

```
WHAT TO SAY DIFFERENTLY:
- [Current messaging] → [New messaging based on interviews]
- [What you're emphasizing] → [What they actually care about]

WHAT TO STOP SAYING:
- [Phrase or angle that keeps triggering objections]

NEW PROOF POINTS TO DEVELOP:
- [Evidence, case study, or stat that would answer the top objection]

POSITIONING IMPLICATION:
→ Chains to /positioning-workshop if the shift is significant
```

### Step 6 — Wrong segment flag

```
SEGMENT CHECK:
Are the people you're talking to your best client profile?
YES / NO / PARTIALLY

IF NO:
- Who are you actually talking to? [Profile]
- Why are they showing up? [Acquisition or word-of-mouth issue]
- Revenue Gate for this segment: A / B / C / D
- Recommendation: [Redirect outreach / adjust ICP / keep both segments]
```

### Step 7 — Next questions for future calls

Based on gaps and surprises in this batch:
```
TOP QUESTIONS FOR NEXT ROUND:
1. [Question — designed to falsify or confirm a specific hypothesis]
2. [Question]
3. [Question]

HYPOTHESIS TO TEST IN NEXT BATCH:
"We believe [X] based on these interviews. We'll confirm or kill this by asking [Y]."
```

### Step 8 — Notion-style synthesis doc

```markdown
# User Interview Synthesis — [Date]
## Batch: [N] interviews | [Date range]

### Top Jobs-to-be-Done
1. [Job] — [Frequency] — [Intensity]
2. [Job] — [Frequency] — [Intensity]
3. [Job] — [Frequency] — [Intensity]

### Top Objections
1. [Objection] → [How to address]
2. [Objection] → [How to address]

### Top Delight Moments
1. [Moment] → [How to amplify]

### Updated Best Client Profile
[One paragraph]

### Messaging Changes
[Bullet list]

### Next Questions
[Bullet list]

### Decisions Made
- [ ] [Action from this synthesis — owner + due date]
- [ ] [Action]
```

---

## Kill Criteria

Stop the synthesis and escalate if:
- Fewer than 5 interviews → not enough signal (directional only, don't make product decisions)
- All interviews are from the same company or referral chain → biased sample
- Nobody described a problem worth solving → product-market fit question, not synthesis question
- Revenue Gate check shows you're talking to D-bucket prospects → wrong audience

---

## Best Client Test
Do the top JTBDs map to your best client's actual situation?
- YES → your product is solving the right thing. Double down.
- NO → you're either talking to the wrong people or building the wrong thing. Escalate.

## Revenue Gate
- **A:** Interviews reveal an urgent, budget-confirmed pain you can close in 30 days
- **B:** Interviews reveal a genuine pain with a 60–90 day path to close
- **C:** Interviews reveal interest but no urgency → content/brand play
- **D:** Interviews reveal no clear pain → stop building and reframe the product

## Maintainability Check
- Can someone who wasn't on the calls read this synthesis and make decisions from it?
- Will it still be useful in 3 months as a reference?
- If no → add more context and direct quotes.

---

## Chains to
→ `/positioning-workshop` — update positioning based on what you heard
