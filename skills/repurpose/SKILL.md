---
name: repurpose
version: 0.1.0
description: >
  Turn one piece of long-form content into platform-ready assets. Extracts the
  best ideas, reformats for each channel, and runs a brand-check on every
  output variant before distribution. One source. Multiple formats. Zero AI slop.
  Trigger on: "repurpose this", "turn this into posts", "make content from this",
  "extract posts from this transcript", "remix this", "pull LinkedIn posts from
  this", "one piece into many", "repurposing", "content from this video",
  "short-form from long-form".
inputs:
  - Source content (paste full transcript, article, interview, webinar, or email)
  - Source type (podcast / video transcript / blog / webinar / interview / email thread)
  - Session Charter from /context-setup (required — run /context-setup first)
  - Target platforms (select all that apply)
  - Revenue Gate for this repurposing session (A / B / C)
outputs:
  - Talking point extraction (best ideas ranked by shareability and brand fit)
  - Platform-ready variants (one per platform selected)
  - Brand-check score for each variant
  - Distribution-ready package with platform-specific specs
  - Killed formats and reasons for killing them
allowed-tools:
  - Bash
  - Read
  - Write
  - Glob
  - AskUserQuestion
---

# Repurpose — One Source, Many Platforms
*Adapted from gstack's content multiplication principle + YC's "make something people want" applied to distribution: the best content is the content that reaches the right person at the right moment in the right format.*

> *"Your best insight is already written. You just haven't published it in the right format yet."*

Most content operations waste their best ideas. A 60-minute webinar becomes one blog post. A sharp client email becomes nothing. A founder interview gets uploaded and forgotten. This skill reverses that. One piece of source content becomes a week of distribution — but only if every format passes the brand-check.

Repurposing without brand-checking is just spreading noise faster.

---

## Pre-Flight

Before extracting anything, load the session context:

```
PRE-FLIGHT CHECKLIST:
[ ] Session Charter from /context-setup is loaded → active Voice Card, Rules Card, Memory Index
[ ] Source content is pasted in full (no summaries — the raw text)
[ ] Source type identified: [podcast / video transcript / blog / webinar / interview / email]
[ ] Source quality check:
    - Does this source contain at least 3 original ideas not found in a Google search?
    - Does it contain at least one specific, non-generic example or data point?
    - Is the source genuinely useful to the target audience?
    → If no to any → do not repurpose. The source is weak. Repurposing amplifies weakness, not just reach.
[ ] Target platforms selected: [LinkedIn / email / X / short-form video brief / newsletter / blog]
[ ] Revenue Gate for this session: A / B / C
```

If Session Charter is missing → stop. Run /context-setup first. Repurposing without brand context produces fast, wrong output.

---

## The Process

### Step 1 — Talking point extraction

Before writing any format, extract the ideas worth publishing. This is the filter that prevents turning mediocre source content into mediocre posts.

```
TALKING POINT EXTRACTION

Source: [title or description]

RAW IDEAS (list everything that could become a post — no filter yet):
1. [Idea]
2. [Idea]
3. [Idea]
...

FILTER — apply 3 questions to each idea:
[ ] Is this an original insight, or something any content marketer would say?
[ ] Does it connect to the target audience's specific pain or world?
[ ] Does it pass the Scroll Test — would they stop scrolling?

RANKED TALKING POINTS (surviving the filter, ranked by strength):
1. [Strongest idea] — why: [specific reason]
2. [Second idea] — why: [specific reason]
3. [Third idea] — why: [specific reason]
...

KILLED IDEAS (failed the filter):
- [Idea] — reason: [too generic / too obvious / no scroll potential]
- [Idea] — reason: [already in Memory killed log / contradicts positioning]

BEST HOOK CANDIDATES (the first line for any platform):
- "[Hook option 1]" — [why it stops scrolling]
- "[Hook option 2]" — [why it stops scrolling]
- "[Hook option 3]" — [why it stops scrolling]
```

---

### Step 2 — Platform-ready variants

For each selected platform, produce one variant. Then brand-check it. One bad variant can be cut — don't cut the whole session.

---

#### Variant A — LinkedIn Post

```
LINKEDIN POST

Hook (first line — must stand alone):
"[First line]"

Body:
[Content — 3–7 lines. Short paragraphs. Each line earns the next.]

CTA:
"[One CTA — conversation-starting, not begging]"

Specs: 150–300 words. 0–1 hashtags. No emojis unless brand voice allows.

BRAND CHECK (run against active Session Charter):
D1 Voice: PASS / FAIL
D2 Forbidden phrases: PASS / FAIL — violations: [list]
D3 Specificity: PASS / FAIL
D5 CTA: PASS / FAIL
D6 Platform rules (LinkedIn): PASS / FAIL

SCORE: [X/5]
VERDICT: Ship / Fix / Kill
REQUIRED FIXES: [specific, not general]
```

---

#### Variant B — Email (Newsletter or Nurture)

```
EMAIL VARIANT

Subject line: "[Subject]"
Preview text: "[Preview — 50–80 characters]"

Body:
[Content — front-loaded value. Lead with the insight, not the context.]

CTA:
"[One action — named, frictionless]"

Specs: 200–400 words. Plain text preferred unless brand uses designed emails. One link max for cold emails.

BRAND CHECK:
D1 Voice: PASS / FAIL
D2 Forbidden phrases: PASS / FAIL
D3 Specificity: PASS / FAIL
D5 CTA: PASS / FAIL
D6 Platform rules (email): PASS / FAIL

SCORE: [X/5]
VERDICT: Ship / Fix / Kill
REQUIRED FIXES: [specific]
```

---

#### Variant C — X (Twitter) Thread

```
X THREAD

Tweet 1 (hook — must work alone):
"[Hook tweet]"

Tweet 2–6 (body — each tweet one idea, not a continuation):
2. "[Tweet]"
3. "[Tweet]"
4. "[Tweet]"
5. "[Tweet]"
6. "[Tweet]"

Final tweet (CTA or conclusion):
"[Conclusion / CTA]"

Specs: Max 7 tweets unless there's a genuine structural reason for more. Each tweet under 280 characters. No thread that could have been one paragraph.

BRAND CHECK:
D1 Voice: PASS / FAIL
D2 Forbidden phrases: PASS / FAIL
D3 Specificity: PASS / FAIL
D5 CTA: PASS / FAIL
D6 Platform rules (X): PASS / FAIL

SCORE: [X/5]
VERDICT: Ship / Fix / Kill
```

---

#### Variant D — Short-Form Video Brief

```
SHORT-FORM VIDEO BRIEF

Platform: [Reels / TikTok / YouTube Shorts]
Target length: [30–60 sec / 60–90 sec]
Format: [Talking head / B-roll + VO / Screen record + VO]

Hook (first 3 seconds — spoken aloud):
"[Exact words — this determines if they stay]"

Structure:
0–5 sec: Hook — name the problem or surprising statement
5–30 sec: Insight — the 1 thing worth knowing
30–50 sec: Proof — specific example, client, or data point
50–60 sec: CTA — one action, stated once

Script or bullet points:
[Write the exact script or the 3–5 bullets the speaker will use]

Visual notes (if relevant):
[What should be on screen / in background / any text overlays]

BRAND CHECK:
D1 Voice: PASS / FAIL (check spoken register, not written)
D2 Forbidden phrases: PASS / FAIL
D3 Specificity: PASS / FAIL
D5 CTA: PASS / FAIL

SCORE: [X/4]
VERDICT: Brief is ready to shoot / Brief needs revision / Kill this angle
```

---

#### Variant E — Newsletter Section

```
NEWSLETTER SECTION

Section headline: "[Headline]"
Section intro: "[1–2 sentences — what this section is and why it matters]"

Body:
[Content — 150–250 words. Can include a brief list if the ideas require it. Plain prose preferred.]

Link or CTA (optional):
"[Resource link or next step — only if it adds value, not to fill space]"

BRAND CHECK:
D1 Voice: PASS / FAIL
D2 Forbidden phrases: PASS / FAIL
D3 Specificity: PASS / FAIL
D6 Platform rules: PASS / FAIL

SCORE: [X/4]
VERDICT: Ship / Fix / Kill
```

---

### Step 3 — Distribution-ready package

After all variants pass brand-check, compile the session output:

```
REPURPOSE SESSION OUTPUT
Source: [title]
Session date: [date]
Produced by: [name / AI tool]
Reviewed by: [name]

SHIPPED (passed brand-check):
[ ] LinkedIn post — [schedule date if known]
[ ] Email — [sequence name / send date]
[ ] X thread — [schedule date]
[ ] Video brief — [assigned to: name]
[ ] Newsletter section — [issue date]

HELD (failed brand-check — requires fix):
[ ] [Format] — [dimension that failed] — fix owner: [name] — fix deadline: [date]

KILLED (failed filter at Step 1 or multiple brand-check dimensions):
- [Format] — reason: [specific]

MEMORY UPDATE:
Did this session surface any approved hooks or copy worth saving?
→ Add to /memory Section 2 (Approved Copy Bank): [list items]
Did any talking point confirm or contradict live positioning?
→ Update /memory Section 1 if positioning signal is strong.
```

---

## Kill Criteria

Kill the repurposing session and return to source if:
- Source content fails the Pre-Flight quality check — three or more repurposed posts from weak content is three times the noise
- Every variant fails brand-check on Dimension 1 (voice) — the source tone is incompatible with the brand. Either the source needs editing or the brand voice needs revisiting.
- Revenue Gate is D — you're publishing for the sake of publishing. That's D-category work until you're default alive.
- The source contradicts live positioning in Section 1 of Memory — don't repurpose a piece that will confuse the market about what you do

---

## Best Client Test
Would your best client share one of these pieces with a peer — unprompted, without being asked to?
- YES → the repurposed content has value. Ship it.
- NO → the source was interesting to you but not to them. Go back to Step 1 and re-filter.

## Revenue Gate
- **A:** Repurposed pieces that generate discovery calls or product signups within 30 days.
- **B:** Repurposed pieces that keep your brand present in a buyer's feed during their 60–90 day consideration window.
- **C:** Repurposed pieces that build brand equity, audience, or search visibility over time.
- **D:** Repurposing for content calendar's sake — "we need to post something" — without a stated goal or audience → kill.

## Maintainability Check
- Can a writer run this skill on any source content in under 90 minutes for a full 5-platform package?
- Can brand-check be run by the same person who produced the content? (It can — but build in a 30-minute gap between production and review.)
- Is the distribution-ready package stored in a format the scheduler can use without re-formatting?
- If no → simplify the output format before adding platforms.

---

## Chains to
→ `/context-setup` — must run first to load brand context
→ `/brand-check` — runs on every variant before it's added to the shipped list
→ `/memory` — approved hooks and copy from this session go into the Copy Bank
→ `/content-governance` — any held variants enter the approval workflow
→ `/brief-review` (MODE 2) — alternative to brand-check for a lighter review pass
