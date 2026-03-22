---
name: identity
version: 0.2.0
description: >
  Capture and lock your brand's complete identity into a reusable document:
  voice, visual system, brand architecture, and kill criteria. Every other
  brand skill depends on this. Run once per brand. Update when positioning
  changes, a new product is added, or a client segment shifts.
  Trigger on: "define our brand voice", "capture our tone", "voice guidelines",
  "what does our brand sound like", "write our identity", "brand personality",
  "set up our voice", "document our tone", "brand identity", "brand document",
  "visual identity", "brand architecture", "who are we".
inputs:
  - Brand name and core offer
  - 3–5 real writing samples that already sound right (required)
  - Anti-examples: content you'd never publish or brands you never want to sound like
  - Visual assets if available (color codes, font names, logo)
  - Products/services list with pricing and format (optional)
  - Bio copy in any length (optional)
outputs:
  - Section 1: Voice Card (8 dimensions, table format, locked)
  - Section 2: Sounds Like / Doesn't Sound Like (contrast pairs table)
  - Section 3: Voice Tests + Banned Phrases list
  - Section 4: Platform Modifiers (all active channels)
  - Section 5: Visual Identity System (color, type, imagery, layout)
  - Section 6: Brand Architecture (offer, products, positioning, entity map, bios)
  - Section 7: How to Use This Document (for AI, writers, designers, and owner)
  - Section 8: Kill Criteria (10 mandatory tests + custom)
  - Changelog
allowed-tools:
  - Bash
  - Read
  - Write
  - Glob
  - AskUserQuestion
---

# Identity — Brand Identity Document
*Adapted from gstack's brand layer system + April Dunford's positioning principle: "Your brand is what people say about you when you're not in the room."*

> *"Professional but approachable is not a voice. It's what everyone writes when they haven't thought about this yet."*

Voice is not a vibe. Visual identity is not a color palette you liked on Dribbble. Brand architecture is not a one-liner you wrote when you launched. A Brand Identity Document is a set of specific, testable, locked decisions that every writer, designer, and AI tool can reference before producing anything under your name.

Without it, every output regresses to the mean. Generic. Forgettable. Replaceable.

This skill builds the complete document — one time, correctly — so you never have to explain your brand again.

---

## Before You Start

Paste 3–5 pieces of content that already sound right. Emails, LinkedIn posts, client proposals, Slack messages — anything written in a voice you'd keep and publish.

For each sample, extract:
- What makes this sound like you and not anyone else?
- What specific word choices, sentence structures, or rhythms repeat?
- What would you never write in this style?

**If you don't have 3 real samples → stop.** Write 3 sentences about your best client's problem first. That's your starting material. Never define voice in the abstract — it always lies.

---

## SECTION 1 — VOICE CARD

*Purpose: Define 8 measurable voice dimensions. These are dials — not vibes. Status is LOCKED once filled. Changes require a version bump.*

Fill every row. Vague answers disqualify the card — a setting without a real example is a preference, not a rule.

| # | Dimension | Setting | What This Means in Practice | Real Example (from your content) |
|---|-----------|---------|----------------------------|----------------------------------|
| 1 | **PACE** | [fast / moderate / slow] | How long are your sentences? How quickly do you reach the point? | [Quote from your site or posts] |
| 2 | **FORMALITY** | [casual / professional / editorial] | Register — how you'd speak in the room you're writing for | [Quote] |
| 3 | **AUTHORITY** | [peer / expert / mentor / commander] | How much do you assert vs. suggest? | [Quote] |
| 4 | **HUMOR** | [none / dry / warm / sharp] | When and how humor shows up — or doesn't | [Quote] |
| 5 | **JARGON** | [none / light / heavy] | Industry language tolerance — what you assume the reader knows | [Quote] |
| 6 | **EMOTION** | [restrained / controlled / open] | How much feeling is permitted to bleed through | [Quote] |
| 7 | **SPECIFICITY** | [abstract / balanced / hyper-specific] | Do you name names, numbers, tools — or speak in concepts? | [Quote] |
| 8 | **POV** | [first / second / third] | Default perspective — I/we, you, or they | [Quote] |

**Enforcement rule:** If an AI generates content that violates 2 or more dimensions, the output is rejected entirely — not edited. Editing a fundamentally wrong-voice piece is always slower than re-briefing.

---

## SECTION 2 — SOUNDS LIKE / DOESN'T SOUND LIKE

*Purpose: Contrast pairs that calibrate tone instantly for any writer or AI. The contrast teaches faster than rules.*

Pull the "Sounds Like" column from your existing content. Write the "Doesn't Sound Like" column as what a lazy AI or junior writer would default to instead. Minimum 5 pairs.

| Sounds Like (✓) | Doesn't Sound Like (✗) |
|---|---|
| [Your real sentence] | [The generic version a language model would produce] |
| [Another real example] | [The corporate / templated version] |
| [A line from a proposal or email you're proud of] | [What a consultant would write instead] |
| [A direct, specific claim you've made] | ["We help businesses achieve their goals through innovative solutions"] |
| [Your strongest hook from any platform] | ["In today's fast-paced digital landscape..."] |

**The floor:** "In today's fast-paced digital landscape..." is the floor. Every line you write must clear it. If it doesn't, it doesn't publish.

---

## SECTION 3 — VOICE TESTS + BANNED PHRASES

*Purpose: Binary pass/fail tests any AI or human can run on draft content before it ships.*

### The 5 Voice Tests

Every piece of content passes all 5 or it goes back:

1. **Best Client Test** — Could your best client read this and think "that's exactly how they talk"? If no → rewrite.
2. **Read-Aloud Test** — Read it out loud. Does it sound like you in [YOUR TYPICAL SETTING — coffee meeting, boardroom, podcast]? If no → rewrite.
3. **First-Line Test** — Does the first line earn the second? If the opening is throat-clearing → cut it.
4. **Cliché Scan** — Does it contain any phrase from the banned list below? One strike = rewrite that sentence. Two strikes = kill the piece and re-brief.
5. **Specificity Test** — Can you replace a vague claim with a number, name, or date? If yes and you didn't → rewrite.

### Banned Phrases

Customize this list. Every brand's list will differ — these are the defaults:

```
BANNED PHRASES — [Brand Name]

Core list (never use, on any platform, in any content type):
- "Innovative solutions"
- "Take your business to the next level"
- "Unlock your potential" / "Unlock [anything]"
- "Best-in-class"
- "Leverage [anything]"
- "Game-changer" / "Revolutionary"
- "In today's fast-paced world..."
- "It's no secret that..."
- "At the end of the day..."
- "We're excited to announce..."
- "Synergy" / "Ecosystem" / "Holistic"
- "Empower" / "Inspire" (without a specific action attached)
- [Add brand-specific terms]
- [Add phrases your best client would roll their eyes at]
- [Add anything that sounds like your least-liked competitor]
```

---

## SECTION 4 — PLATFORM MODIFIERS

*Purpose: Voice stays constant. Tone, pace, and CTA format shift per channel.*

Check every platform you're active on. Delete the rest.

```
PLATFORM MODIFIERS — [Brand Name]

[ ] WEBSITE
- Formality: [adjustment — e.g., "default + editorial confidence"]
- Pace: [e.g., "punchy headlines, measured body copy"]
- CTA: [e.g., "direct command — 'Book a strategy call'"]
- Avoid: [e.g., "FAQ-style writing, passive voice, long hero sections"]

[ ] LINKEDIN
- Formality: [e.g., "+1 from default — executive register"]
- Pace: [e.g., "short hook, 3–5 short body paragraphs, hard close"]
- CTA: [e.g., "one question or low-pressure invitation — not 'DM me for pricing'"]
- Avoid: [e.g., "hashtag stacks, 'Thoughts?', self-congratulation, carousels that should be posts"]

[ ] TWITTER / X
- Formality: [e.g., "-1 from default — more direct, drier"]
- Pace: [e.g., "one idea per tweet; threads only when 5+ real sub-points exist"]
- CTA: [e.g., "often none — let the idea land"]
- Avoid: [e.g., "dunking on competitors, threads that should be blog posts"]

[ ] NEWSLETTER / SUBSTACK
- Formality: [e.g., "peer register — written to one person, not a list"]
- Pace: [e.g., "longer form is earned — open with the most interesting sentence you wrote this week"]
- CTA: [e.g., "one link per email, positioned after the value has been delivered"]
- Avoid: [e.g., "'Hope this finds you well', multiple asks, section headers on short emails"]

[ ] PODCAST
- Formality: [e.g., "conversational — same register as a peer coffee meeting"]
- Pace: [e.g., "slower than written — pause where you'd use a dash in text"]
- CTA: [e.g., "one ask per episode — named, frictionless, repeated once"]
- Avoid: [e.g., "reading from a script, overly produced intros, rambling setups"]

[ ] WORKSHOP / COURSE
- Formality: [e.g., "instructional — direct, no hedging, assume the participant chose to be here"]
- Pace: [e.g., "short concepts, immediate application, no theory without exercise"]
- CTA: [e.g., "'Try this now' — make the action happen in the room"]
- Avoid: [e.g., "slides full of text, reading bullets aloud, 10-minute intros"]

[ ] CLIENT DELIVERABLES
- Formality: [e.g., "executive register — lead with outcome, support with method"]
- Pace: [e.g., "shorter than you think — clients read the first paragraph and the last"]
- CTA: [e.g., "named next step, named owner, named date — never 'let us know your thoughts'"]
- Avoid: [e.g., "passive voice, 'we feel that', ambiguous next steps, cc-all"]

[ ] SPEAKING / KEYNOTES
- Formality: [e.g., "peer register — you're in the room, not above it"]
- Pace: [e.g., "build to one idea — don't give them 7"]
- CTA: [e.g., "one action the room can take before they leave the building"]
- Avoid: [e.g., "'So, um', 'basically', self-deprecating openers, apologizing for slide quality"]

[ ] YOUTUBE
- Formality: [e.g., "conversational but edited — no filler, no hesitation in final cut"]
- Pace: [e.g., "front-load value in the first 30 seconds or lose them"]
- CTA: [e.g., "one per video — subscribe or next video, not both"]
- Avoid: [e.g., "long intros, 'smash the like button', begging for engagement"]

[ ] INSTAGRAM
- Formality: [e.g., "visual-first — copy supports image, not the other way around"]
- Pace: [e.g., "short captions unless the caption is the content"]
- CTA: [e.g., "'Link in bio' only when the link is worth the click"]
- Avoid: [e.g., "excessive hashtags, caption as essay, vague inspiration content"]
```

---

## SECTION 5 — VISUAL IDENTITY SYSTEM

*Purpose: Voice without visual is half a brand. This section locks the design language so nothing ships that looks like a default SaaS template.*

### Color Palette

For each color: name, hex, RGB, and usage rule.

```
COLOR PALETTE — [Brand Name]

Primary accent:    [Name] | #[HEX] | RGB([R],[G],[B]) | [Usage — e.g., "CTAs, key highlights, links"]
Background:        [Name] | #[HEX] | RGB([R],[G],[B]) | [Usage — e.g., "page background, dark sections"]
Primary text:      [Name] | #[HEX] | RGB([R],[G],[B]) | [Usage — e.g., "all body copy"]
Secondary text:    [Name] | #[HEX] | RGB([R],[G],[B]) | [Usage — e.g., "labels, captions, metadata"]
Surface / card:    [Name] | #[HEX] | RGB([R],[G],[B]) | [Usage — e.g., "cards, containers, hover states"]
[Add additional colors]

COLOR RULE:
[One sentence that governs how colors interact and what each one is for.]
Example: "Dark background is the stage. White text delivers. Red makes you act. Everything else supports."
```

### Typography

```
TYPOGRAPHY — [Brand Name]

Headlines:   [Font name] | [Weight] | [Style description — e.g., "Strong, no-nonsense, commands attention"]
Body / UI:   [Font name or stack] | [Weight] | [Style description — e.g., "Clean, readable, no decorative elements"]
Labels:      [Treatment — e.g., "Uppercase, wide letter-spacing, used for navigation and wayfinding only"]

TYPE HIERARCHY:
1. [What commands attention — e.g., "Hero headline — one per page"]
2. [What orients — e.g., "Section headline — tells the reader where they are"]
3. [What informs — e.g., "Body copy — delivers the argument"]
4. [What converts — e.g., "CTA label — names the action, nothing else"]
```

### Imagery Rules

```
IMAGERY — [Brand Name]

Allowed:
- [Real photography vs. illustration vs. stock — what's permitted]
- [Crop and framing preferences — e.g., "face-forward, natural light, mid-shot"]
- [Contexts and settings that are on-brand]

Banned:
- [Explicitly off-brand imagery types — e.g., "generic stock smiles, fake office environments"]
- [Visual styles that conflict with brand personality]
- [Formats that break on primary platforms]
```

### Layout System

```
LAYOUT — [Brand Name]

Page structure:    [e.g., "Dark, full-bleed, single-column scroll, no sidebars"]
Section rhythm:    [e.g., "Hero → Problem → Solution → Proof → CTA. No deviation."]
Whitespace:        [e.g., "Generous. Content earns its space. Padding before density."]
Components:        [e.g., "Cards over carousels. Tables over bullet lists. No accordions on primary pages."]
Mobile rule:       [e.g., "Design for mobile first. If it breaks at 375px, it doesn't ship."]
```

---

## SECTION 6 — BRAND ARCHITECTURE

*Purpose: What you sell, who you sell to, and why you're different — in a format an AI can reference when generating any content.*

### Core Offer

[1–2 sentences. What you do for whom. No jargon. If your best client read this, they'd say "yes, that's exactly what I needed."]

### Products and Services

| Product | Format | Description | Price | Timeline |
|---------|--------|-------------|-------|----------|
| [Name] | [Retainer / project / workshop / product] | [What the client gets — outcomes, not features] | [If public] | [Duration or delivery window] |
| [Name] | [Format] | [Description] | [Price] | [Timeline] |

### Positioning Statement

[One paragraph. Who you are, who it's for, what you do, and what makes you different. This is the paragraph a writer reads when they don't know where to start.]

### Competitive Distinction

```
Not a [CATEGORY A]:  [Why you're different from this type of provider]
Not a [CATEGORY B]:  [Why you're different]
Not a [CATEGORY C]:  [Why you're different]
```

### Target Audience

```
PRIMARY:    [Who — role, company type, situation] | [Pain — what's breaking for them] | [Stage — where in the buyer journey]
SECONDARY:  [Who] | [Pain] | [Stage]
TERTIARY:   [Who] | [Pain] | [Stage]
```

### Entity Map

For founders running multiple brands, companies, or platforms:

| Entity | Type | Location | Relationship to Personal Brand |
|--------|------|----------|-------------------------------|
| [Name] | [Holding co / product / platform / consultancy] | [Where registered or operating] | [How it relates — e.g., "primary vehicle for client work"] |

### Content Assets

| Asset | Format | Platform | Frequency | URL |
|-------|--------|----------|-----------|-----|
| [Podcast / show name] | [Audio / video] | [Where published] | [Cadence] | [Link] |
| [Newsletter name] | [Email] | [Platform] | [Cadence] | [Link] |
| [Lead magnet] | [PDF / course / template] | [Delivery method] | [Evergreen / dated] | [Link] |

### Bio Variants

```
50-WORD BIO:
[Paste here]

100-WORD BIO:
[Paste here]

250-WORD BIO:
[Paste here]
```

---

## SECTION 7 — HOW TO USE THIS DOCUMENT

*This section is read by everyone who touches content under this brand.*

**For AI Assistants:**
Load this document as context before generating any content for [BRAND NAME]. Every output must pass the Voice Tests in Section 3 and the Kill Criteria in Section 8. If uncertain on tone, default to shorter, more direct, and more specific. When in doubt, pick the version that sounds like it was written by a human who knows what they're talking about — not a model completing a prompt.

**For Human Writers:**
Read Sections 1–3 before writing anything. Check your draft against the Kill Criteria in Section 8. If you used a banned phrase from Section 3 — you didn't read this document. Read it again before the next draft.

**For Designers:**
Section 5 is your reference. If the output looks like a default SaaS template, a Canva preset, or a brand you could name, start over. The visual system exists to make the brand recognizable, not pleasant.

**For [OWNER NAME]:**
This is the filter. When someone asks "what does [BRAND NAME] sound like?" — hand them this file. When a contractor delivers something that feels off, point to the specific section that was violated. This document isn't aspirational. It's operational. Every section should describe what you do today, not what you hope to be.

---

## SECTION 8 — KILL CRITERIA

*Purpose: Binary tests. If content matches ANY of these, it does not publish. No exceptions.*

Mandatory tests (do not remove these — add your own below):

```
1. GENERIC AUDIENCE TEST
   Could this have been written for anyone in your industry, targeting anyone who markets?
   If yes → kill. Rewrite for a specific person in a specific situation.

2. CLICHÉ SCAN
   Does it contain any phrase from the Banned List in Section 3?
   One strike = rewrite that sentence.
   Two strikes = kill the piece. Re-brief from Section 1.

3. FORMALITY DRIFT
   Does it sound like a press release, a LinkedIn influencer post, or a corporate brochure?
   If you can't hear [OWNER NAME] saying this in [YOUR TYPICAL SETTING] → kill it.

4. PASSIVE VOICE CHECK
   Is the subject hiding? "Mistakes were made." "Results can be achieved."
   Kill passive constructions. Name who does what.

5. EMPTY CTA TEST
   Does the CTA say "Learn More" or "Get Started" with no specificity?
   Kill it. Every CTA must name the action, the outcome, or the next step explicitly.

6. VISUAL IDENTITY VIOLATION
   Does the design break any rule from Section 5?
   Wrong color, wrong font, wrong layout, wrong imagery → kill before it ships.

7. CHANNEL MISMATCH
   Is the tone, length, or format wrong for the platform per Section 4?
   A LinkedIn post formatted like a newsletter is not a LinkedIn post → kill it.

8. CREDENTIAL INFLATION TEST
   Does it claim a credential, result, or expertise not documented in Section 6?
   If no proof exists in the brand record → kill it. Don't fabricate authority.

9. ENTITY CONFUSION TEST
   Does it say "your company" or "the brand" without naming which entity from Section 6?
   Ambiguous entity references confuse your audience and your team → kill it.

10. ORIGIN STORY EXPLOITATION TEST
    Does it use a backstory or personal hardship as a persuasion mechanism rather than context?
    If it reads like a sob story engineered to sell → rewrite. Context earns trust. Manipulation loses it.
```

Custom kill criteria (add yours — minimum 2):
```
[ ] [YOUR KILL TEST] — [what it catches]
[ ] [YOUR KILL TEST] — [what it catches]
```

---

## CHANGELOG

| Version | Date | Changes |
|---------|------|---------|
| 0.2.0 | [date] | Added Sections 5–8: Visual Identity, Brand Architecture, How to Use, expanded Kill Criteria. Voice Card converted to table format. Sounds Like converted to contrast pair table. Banned phrases list added to Section 3. Platform modifiers expanded to 10 platforms. |
| 0.1.0 | [date] | Initial release |

---

## Kill Criteria (Skill-Level)

Kill this skill output and rebuild if:
- The "Sounds Like" column in Section 2 is filled with aspirational brands, not brands that actually sound like you today — your samples beat your preferences
- The Banned Phrases list in Section 3 has fewer than 10 entries — you haven't looked hard enough at what you actually sound like vs. what you want to avoid
- Section 1 confidence dimension says "collaborative" but real writing samples are declarative — samples override stated preferences, every time
- Section 5 (Visual Identity) is marked as "TBD" while Section 1 is filled — voice and visual are inseparable. Lock both or lock neither.
- Section 6 (Brand Architecture) Core Offer takes more than two sentences — if you can't say it in two, it's not a positioning statement, it's a list of capabilities. Run `/positioning-workshop` first.

---

## Best Client Test
Would your best client read this document and say "this is exactly who they are — I'd give them my brand to work on"?
- YES → the document is operational. Lock it, version it, share it.
- NO → something is aspirational instead of accurate. Find the section that describes who you want to be rather than who you are. Fix that section first.

## Revenue Gate
- **A:** Clients pay premiums for brands they trust. A complete, locked identity document directly supports pricing conversations and proposal close rates.
- **B:** Consistent brand identity reduces revision rounds across all retained accounts — direct margin improvement.
- **C:** A fully documented identity reduces onboarding time for writers, designers, and AI tools — measurable burn reduction every time you bring someone new in.
- **D:** Identity work that exists in a document no one references, updates, or uses to evaluate content → maintenance without impact. Make it operational or archive it.

## Maintainability Check
- Can a new writer use this document to produce on-brand content on day one without asking a single question?
- Can a designer use Section 5 to build an on-brand asset without a briefing call?
- Is every example in the document from real content — not invented to fill the template?
- Does the Changelog have a named owner and a last-updated date?
- If no to any → the document isn't operational yet. Incomplete sections are worse than missing ones — they signal "this was filled out for the sake of filling it out."

---

## Chains to
→ `/rules` — Banned Phrases in Section 3 extend into the Rules Card's forbidden phrase Layer 1
→ `/memory` — Positioning Statement and Core Offer in Section 6 anchor the Memory Index Section 1 (Live Positioning)
→ `/brand-check` — Voice Card (Section 1) is the rubric for Dimension 1; Kill Criteria (Section 8) maps to all 7 brand-check dimensions
→ `/context-setup` — full Identity Document loads as Layer 1 of the brand context stack
→ `/positioning-workshop` — if Section 6 Positioning Statement isn't landing, run positioning-workshop before returning here
