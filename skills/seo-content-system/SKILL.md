---
name: seo-content-system
version: 0.2.0
description: >
  Turns any topic into a full SEO content cluster. Optimized for content-ops
  founders and agencies who want compounding organic traffic, not one-off posts.
  Run when starting a new content program or expanding an existing one.
  Trigger on: "build a content strategy", "SEO content plan", "content cluster",
  "what should I blog about", "keyword research", "pillar page", "content system",
  "SEO strategy", "build content around X".
inputs:
  - Primary topic or keyword
  - Target audience (best client profile)
  - Any existing content or brief
outputs:
  - Primary keyword + search intent analysis
  - 6-10 supporting cluster keywords
  - Title + meta description for pillar page
  - Outline for pillar + 2-3 cluster articles
  - EEAT check (expertise signals to include)
  - Internal linking plan
  - "Would best client share this" filter
  - CTA + conversion goal per piece
  - Brief template ready for /brief-review chaining
allowed-tools:
  - Bash
  - Read
  - Write
  - Glob
  - AskUserQuestion
---

# SEO Content System
*Content cluster strategy + E-E-A-T framework + YC "make something people want to find"*

> *"One blog post is a lottery ticket. A content system is a compounding asset."*

A single blog post ranks occasionally. A content cluster — pillar page surrounded by supporting articles, all internally linked — ranks reliably and compounds over time. This skill builds the cluster, not just the post.

---

## Process

### Step 1 — Primary keyword + search intent analysis

```
PRIMARY KEYWORD: [Exact phrase]

SEARCH INTENT: 
- Informational ("how to X") → educational pillar, no direct CTA
- Navigational ("X tool/brand") → product page or comparison
- Commercial ("best X for Y") → decision-stage content, strong CTA
- Transactional ("buy X" / "X pricing") → conversion page, direct CTA

SEARCH VOLUME ESTIMATE: [High >1k/mo / Medium 100-1k / Low <100 / Unknown]
COMPETITION LEVEL: [High / Medium / Low — based on who currently ranks]
KEYWORD DIFFICULTY: [Hard: major brands dominate / Medium / Low: opportunity]

BEST CLIENT FIT:
Is this the keyword your best client would actually search?
YES / NO — if no, what keyword would they actually use?

REVISED KEYWORD (if needed): [Updated based on best client language]
```

### Step 2 — Cluster keywords (6–10)

Build the cluster around the primary keyword. Each supporting keyword:
- Answers a sub-question the primary keyword raises
- Targets a different stage of awareness or search intent
- Can internally link back to the pillar page

```
CLUSTER KEYWORD [1-10]:
Keyword: [Phrase]
Intent: [Informational / Commercial / Transactional]
Article type: [How-to / List / Comparison / Case study / Definition]
Best client would search this when: [Specific situation]
Internal link to: Pillar / [Other cluster piece]
```

### Step 3 — Pillar page outline

```
PILLAR PAGE

Title: [Primary keyword + clear benefit — under 60 chars]
Meta description: [Under 155 chars — includes keyword, benefit, and implicit CTA]

H1: [Same as title or close variant]

OUTLINE:
1. Introduction (hook + what they'll learn + why this source is credible)
2. [Main section — covers the primary question comprehensively]
3. [Sub-section — supporting depth]
4. [Sub-section — supporting depth]
5. [Sub-section — supporting depth]
6. [Common mistakes or misconceptions section]
7. [Comparison or alternatives section — if commercial intent]
8. [Expert POV or case study — EEAT signal]
9. Conclusion + CTA

WORD COUNT TARGET: [2,000–4,000 for informational / 1,000–2,000 for commercial]
CTA: [One action — trial, download, discovery call, or subscribe]
CONVERSION GOAL: [What happens after they read this?]
```

### Step 4 — Cluster article outlines (2–3)

For each supporting cluster article:
```
CLUSTER ARTICLE [#]

Keyword: [Supporting keyword]
Title: [Under 60 chars]
Meta: [Under 155 chars]
Intent: [Informational / Commercial]
Main question it answers: [One sentence]
Outline: [3–5 H2 sections]
Internal links:
  → Pillar: [Link text]
  → Other cluster: [Link text]
Word count: [500–1,500 for supporting articles]
CTA: [Same as pillar or specific to this article's intent]
```

### Step 5 — EEAT check (Expertise, Experience, Authoritativeness, Trust)

Google ranks content higher when it demonstrates genuine expertise. For each piece:

```
EXPERTISE SIGNALS TO INCLUDE:
- [ ] Author bio with relevant credentials or real-world experience
- [ ] Specific data, case studies, or examples from your actual work
- [ ] Named clients or projects (with permission) as proof
- [ ] Original insight or opinion — not just summarizing other sources
- [ ] Publication date + last updated date

EXPERIENCE SIGNALS:
- [ ] First-person examples ("We ran this for a client and found...")
- [ ] Screenshots or real outputs from your work
- [ ] Process documentation that only comes from doing it

AUTHORITATIVENESS SIGNALS:
- [ ] External citations to credible sources
- [ ] Quotes from other recognized experts
- [ ] Backlink-worthy content (original data, useful tools, definitive guides)

TRUST SIGNALS:
- [ ] Author name visible and linkable
- [ ] Contact information available
- [ ] No broken links or outdated claims
```

### Step 6 — Internal linking plan

```
LINKING MAP:
Pillar ← [Cluster 1] (anchor text: [keyword phrase])
Pillar ← [Cluster 2] (anchor text: [keyword phrase])
Pillar ← [Cluster 3] (anchor text: [keyword phrase])
[Cluster 1] → [Cluster 2] (relevant contextual link)

RULE: Every cluster article links back to the pillar. Pillar links to all clusters.
      New content always links to the most relevant existing piece.
```

### Step 7 — Best client share filter

Before publishing any piece, ask:
```
WOULD YOUR BEST CLIENT SHARE THIS?
- Would they send it to a colleague? YES / NO
- Would they screenshot it? YES / NO
- Would they save it for reference? YES / NO

If 2 or more are NO → the piece is not good enough. Don't publish until it is.
What's missing: [Specificity / Unique insight / Real examples / Depth]
```

### Step 8 — Brief template for /brief-review

Ready to chain to the brief-review skill:
```
CONTENT BRIEF — [Article title]

AUDIENCE: [Best client profile — specific, not demographic]
GOAL: [What action should they take after reading?]
PRIMARY KEYWORD: [Exact phrase]
SEARCH INTENT: [Informational / Commercial / Transactional]
OUTLINE: [Paste from Step 3 or 4]
TONE: [3 adjectives — match your brand voice]
EXAMPLES OF OUR VOICE: [Link or paste a piece that sounds right]
WORD COUNT: [Target]
CTA: [Exact CTA text + destination]
EEAT REQUIREMENTS: [List signals to include from Step 5]
WHAT WE NEVER SAY: [Off-brand phrases, topics to avoid]
```

---

## Kill Criteria

Kill a content piece if:
- The primary keyword is searched by people who will never buy from you
- You can't write it with genuine expertise (EEAT fails)
- The best client share filter returns all NOs
- Revenue Gate is D

---

## Best Client Test
Would your best client bookmark this article and reference it at work?
- YES → publish it.
- NO → it's not specific enough. Add real examples, original data, or a stronger point of view.

## Revenue Gate
- **A:** Content targeting transactional/commercial intent → direct path to trial or discovery call
- **B:** Content targeting decision-stage buyers → 60–90 day nurture path
- **C:** Informational content → awareness and backlinks (valid, but not primary focus)
- **D:** Content no one in your ICP searches for → don't write it

## Maintainability Check
- Can your team update this content quarterly without rebuilding it?
- Is the cluster small enough to execute with your current team?
- If no → cut the cluster in half. Ship 3 pieces well, not 10 pieces poorly.

---

## Chains to
→ `/brief-review` — run each piece through quality gate before publishing
→ `/gtm-review` — validate that the content strategy aligns with GTM priorities
