# Blueprint: Social Post — From Brand Context to Published Post
*A starter kit for marketers using the fstack Brand Identity Layer.*

---

## What this blueprint is

This is a step-by-step workflow for producing a single social media post (LinkedIn, X, or Instagram) that passes brand-check before it publishes. Follow it exactly the first time. Once your brand identity layer is built, steps 1–3 collapse to under 5 minutes.

**Time to complete (first run):** 2–3 hours (most of this is building your brand docs — you only do it once)
**Time to complete (subsequent runs):** 15–30 minutes per post

---

## Before You Start

You need three things. If any are missing, build them first using the linked templates.

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

MEMORY — LIVE CAMPAIGNS (do not contradict these):
[paste Section 4 from your Memory Index]

Keep this context active for everything we produce in this session.
```

Press send. The AI will confirm the context is loaded. Now you're ready.

---

### Step 1 — Declare the Post Goal

Tell the AI exactly what you need:

```
I need to write one [LinkedIn post / X thread / Instagram caption] for [BRAND NAME].

Topic or source material:
[Paste the idea, insight, transcript excerpt, or talking point you want to build from]

Target audience for this post:
[Specific person — e.g., "a B2B marketing manager at a 50-person SaaS company"]

Revenue Gate:
[ ] A — This post should generate an inquiry or booking within 30 days
[ ] B — This post should keep us visible in a buyer's feed during their consideration window
[ ] C — This post builds brand recognition or audience over time

CTA I want to use:
[e.g., "Comment below if this sounds familiar." / "Reply and I'll send you the framework." / "Link in bio." — or write "suggest one"]
```

---

### Step 2 — Produce the Draft

The AI will write a first draft based on your brand context and session declaration. If the first draft doesn't feel right, say:

> "This doesn't match my voice. The pace is too slow and it's hedging in the second paragraph. Rewrite using the Voice Card — pace: fast, authority: expert. Cut anything that doesn't earn its place."

Don't accept a draft that feels like something a competitor could have written.

---

### Step 3 — Run Brand Check

Once you have a draft you're considering, paste this:

```
Run a brand check on this draft. Score it on:
D1 — Voice Alignment (check against my Voice Card)
D2 — Forbidden Phrase Scan (check against my Rules Card Layer 1)
D3 — Specificity (are there real numbers, names, or examples?)
D5 — CTA Quality (one CTA, direct, platform-appropriate)
D6 — Platform Rules (check against my Rules Card Layer 5 for [platform])

Give me a score out of 5, a verdict (Ship / Fix / Kill), and specific required changes if it's not a Ship.
```

---

### Step 4 — Fix or Ship

**If Ship (5/5):** Schedule or publish. Log it in your audit trail.

**If Fix:** Make exactly the changes listed. Re-run brand check. Do not publish until it passes.

**If Kill:** The source material or angle was wrong. Go back to Step 1. Pick a different talking point or approach.

---

### Step 5 — Log It

After publishing, add a one-line entry to your audit trail:

```
[Date] — [Post title or first line] — [Platform] — Brand check: [score] — Verdict: Ship — Publish date: [date] — [Result if measurable within 7 days]
```

---

## Common Mistakes

**Skipping Step 0.** You load brand context once per session, not once per post. New session = reload context.

**Accepting the first draft.** The first AI draft will often be technically correct but missing your specific voice. Push it.

**Running brand check on a summary.** Brand check requires the final, exact text. Not a description of what the post will say.

**Multiple CTAs.** One. Every time. Two CTAs = no action taken.

---

## What to Do If Brand Check Fails Repeatedly

If a post fails brand check more than twice on the same dimension, the problem is upstream:

- **D1 fails repeatedly:** Your Voice Card may need more specific examples. Return to `identity.md` and add 2–3 real samples.
- **D2 fails repeatedly:** Your Rules Card forbidden phrase list may be incomplete. Return to `rules.md` and add the patterns you keep seeing.
- **D3 fails repeatedly:** You're starting from ideas that are too abstract. The source material doesn't have specific anchors. Go back to the talking point before writing.

---

## Next Steps After This Blueprint

Once you've produced 5–10 posts using this workflow:
- The patterns that keep failing → update your Rules Card
- The hooks that keep winning → add them to your Memory Copy Bank (Section 2)
- The angles that keep getting killed → add them to your Memory Killed Log (Section 3)

The brand identity layer gets stronger every time you use it.

*Part of fstack — open source operating system for founders and marketers. github.com/likke/fstack*
