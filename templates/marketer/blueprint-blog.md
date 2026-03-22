# Blueprint: Blog Post — From Brand Context to Published Article
*A starter kit for marketers using the fstack Brand Identity Layer.*

---

## What this blueprint is

This is a step-by-step workflow for producing a blog post or long-form article that passes brand-check before it publishes. It works whether you're writing from scratch or repurposing existing content (a webinar, a talk, a client conversation).

**Time to complete (first run):** 3–4 hours (most of this is building your brand docs — you only do it once)
**Time to complete (subsequent runs):** 60–90 minutes per article

---

## Before You Start

You need three things. If any are missing, build them first.

| What you need | Where to get it | Status |
|---|---|---|
| Voice Card | Run `templates/marketer/identity.md` | [ ] Done |
| Rules Card | Run `templates/marketer/rules.md` | [ ] Done |
| Memory Index | Run `templates/marketer/memory.md` | [ ] Done |

---

## The Workflow

### Step 0 — Load Your Brand Context

Open a new ChatGPT or Claude session. Paste this at the top:

```
I'm producing content for [BRAND NAME]. Here is my brand context:

VOICE CARD:
[paste your full Voice Card here]

RULES CARD:
[paste your full Rules Card here]

MEMORY — LIVE POSITIONING:
[paste Section 1 from your Memory Index]

MEMORY — LIVE CAMPAIGNS (do not contradict):
[paste Section 4 from your Memory Index]

Keep this context active for everything we produce in this session.
```

---

### Step 1 — Define the Article

Before writing anything, declare the full brief:

```
I need to write a blog post / article for [BRAND NAME].

Working title:
[Your best working title — not the final one, just something to aim at]

Primary keyword or topic:
[What search term or topic is this targeting?]

Target reader:
[Specific person — e.g., "a marketing director at a professional services firm who is considering AI tools for their team"]

The one thing this article must do:
[e.g., "Make the reader trust us as the right partner for this problem." / "Rank for 'content marketing for B2B SaaS' and generate organic leads." / "Give the reader one framework they can use tomorrow."]

Revenue Gate:
[ ] A — Should generate an inquiry within 30 days (strong CTA, bottom-of-funnel)
[ ] B — Should keep existing contacts engaged during a 60–90 day consideration window
[ ] C — Should build brand recognition and search visibility over time

Source material (if repurposing):
[Paste transcript, notes, or raw content — or write "starting from scratch"]

Desired length:
[e.g., 800 words / 1,200–1,500 words / comprehensive guide (2,000+)]
```

---

### Step 2 — Build the Outline First

Do not ask for a full draft yet. Ask for the outline:

```
Based on the brief above, produce an outline for this article. Include:
- A working headline (3 options)
- Intro approach (what problem or tension does it open on?)
- 3–5 main sections with one-line descriptions
- The specific claim or insight that anchors each section
- The CTA at the end

Do not write the full article yet. Just the structure.
```

Review the outline before the draft. A bad outline produces a good draft of the wrong article. Push back here if anything is generic, too abstract, or doesn't match the positioning.

---

### Step 3 — Produce Section by Section

Long-form content produced in one pass is usually weaker than content produced section by section. After approving the outline, produce each section separately:

```
Write Section 1: [section title from the approved outline]

Requirements:
- Match Voice Card: pace [fast/moderate/slow], formality [setting], authority [setting]
- Open with the most specific claim or example you have — no scene-setting
- Include at least one real data point, named example, or client reference
- Do not use these phrases: [paste top 5 from your Rules Card forbidden list]
```

Repeat for each section. This keeps quality consistent and makes revisions surgical.

---

### Step 4 — Assemble and Check

Once all sections are written and approved, assemble the full article. Then run brand check:

```
Run a full brand check on this article draft. Score it on:
D1 — Voice Alignment (check against my Voice Card)
D2 — Forbidden Phrase Scan (check my Rules Card Layer 1)
D3 — Specificity (does every major claim have a number, name, or example?)
D4 — Message Alignment (does this reinforce or contradict my live positioning?)
D5 — CTA Quality (one CTA, appropriate for the article's Revenue Gate)
D6 — Platform Rules (check my Rules Card Layer 5 for blog / owned media)
D7 — Revenue Gate Fit (is this article designed to do its stated job?)

Score out of 7. Give me a verdict (Ship / Fix / Kill) and specific required changes.
```

---

### Step 5 — Final Check Before Publishing

Before hitting publish, run this checklist manually:

```
PUBLISH CHECKLIST:
[ ] Headline: does it earn the click without being click-bait?
[ ] Opening line: does it earn the second line? (No "In today's world...")
[ ] Every major claim: backed by a specific example, number, or named client?
[ ] Forbidden phrases: clear?
[ ] CTA: one, clear, appropriate to funnel stage?
[ ] Read aloud: does it sound like a human who knows their subject — or like a content brief?
[ ] Brand check: Ship verdict?
```

If all 7 pass → publish. If any fail → fix before publishing.

---

### Step 6 — Log It

After publishing:

```
[Date] — [Article title] — [Platform/URL] — Brand check: [X/7] — Verdict: Ship — Publish date: [date] — [Traffic / conversion result if measurable within 30 days]
```

---

## Common Mistakes

**Writing the draft before the outline.** Outlines are not optional for long-form. The draft will be harder to fix than a bad outline.

**Producing in one pass.** Section-by-section production catches problems earlier and produces more consistent quality.

**Skipping D4 (Message Alignment).** A blog post that contradicts your live positioning does brand damage at scale — especially if it ranks.

**Weak opening.** The first paragraph of most AI-generated blog posts is scene-setting that tells the reader nothing. Delete it. Start at the interesting part.

---

## If You're Repurposing Source Content

Run `templates/marketer/repurpose.md` first to extract and filter the best talking points. Then use the ranked talking points from that session as your source material for Step 1. This produces stronger outlines with less wasted time.

---

## Next Steps After This Blueprint

- Headlines that perform well → add to Memory Approved Copy Bank
- Positioning angles that resonate → strengthen Memory Section 1
- Angles that got killed in outline review → log in Memory Killed Messaging Log

*Part of fstack — open source operating system for founders and marketers. github.com/likke/fstack*
