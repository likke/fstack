---
name: growth-sprint
version: 0.2.0
description: >
  Orchestrates the full growth loop across all fstack growth skills.
  Runs positioning, experiment design, launch, cohort review, and retro
  as a single coordinated cycle. Run at the start of any new growth push
  or quarterly reset. Trigger on: "run a growth sprint", "full growth cycle",
  "start the growth loop", "growth planning", "quarterly growth review".
inputs:
  - Current business goal (MRR target, user milestone, channel objective)
  - Time horizon (2 weeks / 4 weeks / quarter)
  - Available team and budget
  - Current metrics snapshot (MRR, burn, top channels)
outputs:
  - Ordered growth sprint plan with skill chain
  - Week-by-week execution sequence
  - Decision gates between each phase
  - Success and kill criteria for the full cycle
  - L10-ready summary for team sync
allowed-tools:
  - Bash
  - Read
  - Write
  - Glob
  - AskUserQuestion
---

# Growth Sprint (Orchestrator)
*Chains all fstack growth skills into a single coordinated cycle. Inspired by Garry Tan's gstack orchestration philosophy.*

> *"Growth isn't a department. It's a loop."*

Positioning without experimentation is theory. Experimentation without cohort review is guessing. The growth loop only compounds when all stages connect. This skill runs the whole cycle.

---

## The Growth Loop

```
/customer-interview-synthesizer
         ↓
/positioning-workshop
         ↓
/experiment-designer
         ↓
/launch-orchestrator
         ↓
/cohort-review
         ↓
/retro  ──────→ back to /customer-interview-synthesizer
```

Each stage feeds the next. The loop never ends — it just gets faster and more accurate.

---

## Process

### Step 0 — Sprint setup

Before running any skill, define the sprint:

```
SPRINT GOAL: [One sentence — what does success look like at the end?]
TIME HORIZON: [ ] 2 weeks  [ ] 4 weeks  [ ] Quarter
REVENUE GATE: A / B / C (What bucket is this sprint serving?)
TEAM: [Who owns what]
CURRENT MRR: _____ | BURN: _____ | RUNWAY: _____ months
```

### Phase 1 — Talk to users (Week 1)
**Skill: `/customer-interview-synthesizer`**

Run 5–10 user interviews. Synthesize before doing anything else.

Decision gate:
- Top JTBD identified? → proceed to Phase 2
- Wrong segment flag? → stop, redefine ICP, restart interviews
- No clear pain? → escalate to founder review before proceeding

### Phase 2 — Lock positioning (Week 1)
**Skill: `/positioning-workshop`**

Build 3 positioning options. Pick one. Lock it for the sprint.

Decision gate:
- Best Client Test passes? → proceed to Phase 3
- Revenue Gate A or B? → proceed
- Revenue Gate D? → kill sprint, reframe goal

### Phase 3 — Design the experiment (Week 1–2)
**Skill: `/experiment-designer`**

Design the smallest test that can prove or disprove the positioning.

Decision gate:
- Hypothesis falsifiable? → proceed
- Kill criterion defined? → proceed
- No tracking set up? → do not launch until it is

### Phase 4 — Launch (Week 2)
**Skill: `/launch-orchestrator`**

Execute the launch sequence. Day 0 is not the time to improvise.

Decision gate:
- Hook passes Garry RT filter? → launch
- Hook fails? → rewrite and retest against positioning
- Assets incomplete? → delay launch, do not skip prep

### Phase 5 — Review cohorts (Week 3–4)
**Skill: `/cohort-review`**

Pull data. Find truth. Default alive check.

Decision gate:
- LTV:CAC > 3x on target cohort? → scale this channel
- LTV:CAC 1–3x? → optimize before scaling
- LTV:CAC < 1x? → kill channel, rerun Phase 2
- Default alive? → continue sprint
- Not default alive? → escalate immediately

### Phase 6 — Retro and reset (Week 4 / End of sprint)
**Skill: `/retro`**

Review the full cycle. What did we learn? What do we ship next sprint?

```
SPRINT RETRO:

What we tested: [Positioning + experiment]
What worked: [Channels, messages, segments]
What didn't: [Kill list]
What we now know about our best client: [Updated profile]
Next sprint goal: [Feed back into Phase 1]
```

---

## Sprint Templates

### 2-Week Sprint
```
Day 1-3:   /customer-interview-synthesizer (5 interviews min)
Day 3-4:   /positioning-workshop (lock one option)
Day 4-5:   /experiment-designer (design + launch checklist)
Day 6-10:  /launch-orchestrator (execute)
Day 11-14: /cohort-review (read results)
Day 14:    /retro (decisions + next sprint brief)
```

### 4-Week Sprint
```
Week 1: /customer-interview-synthesizer + /positioning-workshop
Week 2: /experiment-designer + launch prep
Week 3: /launch-orchestrator (full rollout)
Week 4: /cohort-review + /retro
```

### Quarterly Sprint
```
Month 1: Research + Positioning
Month 2: Experiment + Launch
Month 3: Cohort review + Retro + Plan next quarter
```

---

## Kill Criteria

Kill the sprint and reset if:
- Default alive check fails and runway < 3 months → survival mode only
- Revenue Gate flips to D at any phase → stop and reframe
- Best Client Test fails in Phase 2 and no alternative positioning exists
- Launch day-of completion rate < 60% on the asset checklist

---

## Best Client Test
At the end of the sprint: did you get closer to your best client profile — or further away?
- Closer → the loop is working. Run it again, faster.
- Further → something broke in Phase 1 or 2. Restart from user interviews.

## Revenue Gate
- **A:** Sprint targeting a direct close within the sprint window
- **B:** Sprint building toward a 60–90 day close
- **C:** Sprint for brand/SEO/awareness compounding
- **D:** Sprint with no clear success metric → don't start

## Maintainability Check
- Can your team run this loop without you in the room for Phase 3–5?
- Is the retro documented well enough that the next sprint starts with real context?
- If no → document the handoff before ending the sprint.
