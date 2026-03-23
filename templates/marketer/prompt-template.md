# The Prompt Template — Build Your Own Version
*A modular prompt structure for briefing AI correctly. Three versions: basic, gstack-aligned, and Anthropic-standard. Pick one. Adapt it. Own it.*

---

## Why This Exists

Most AI content fails at the brief stage, not the generation stage. The model is capable. The instructions are vague. This template fixes that by forcing you to declare role, context, task, constraints, and format before the AI writes a single word.

The base structure works everywhere — ChatGPT, Claude, Gemini. The versions below are calibrated for specific operating philosophies. Use the one that matches how you run.

---

## Version 1 — The Basic Template

The foundation. Use this if you're starting fresh, briefing a freelancer, or building your own system on top of it.

```
ROLE: You are a [role] for [brand].

CONTEXT: [Paste from your context stack — brand voice, audience, past examples]

TASK: Write a [content type] about [topic] for [audience].

CONSTRAINTS:
- Tone: [specific tone from brand guide]
- Length: [word count]
- Do NOT use: [banned phrases]
- Include: [required elements]

FORMAT: [Specific output format]
```

**When to use this:** First-time brief. New team member. Starting a new content type. Any situation where you need a clean, unambiguous instruction.

**What each field does:**

- **ROLE** — Tells the model who it's being, not just what to do. A "senior content director" produces different output than "a writer."
- **CONTEXT** — The most skipped field. This is where your brand identity layer goes. No context = generic output.
- **TASK** — One specific output. Not "some content." One piece, one format, one topic, one audience.
- **CONSTRAINTS** — The guardrails. The model will fill every gap you leave with its training data defaults. Fill the gaps yourself.
- **FORMAT** — Tell it exactly how to structure the output. Otherwise it decides.

---

## Version 2 — gstack-Aligned Template

*Calibrated to Garry Tan's gstack principles and fstack's three core tests.*

This version adds three forcing functions the basic template skips: the Revenue Gate, the Best Client Test, and explicit kill criteria. It's designed for founders and operators who need every piece of content to justify itself before it gets produced.

```
ROLE: You are a [role] for [brand]. You operate with senior judgment — you will push back if the brief is unclear or the task fails the Revenue Gate.

CONTEXT:
[Brand Voice Card — paste from /identity output]
[Rules Card — paste from /rules output]
[Live Positioning — paste Section 1 from /memory output]
[Best Client Profile — who is your highest-margin, lowest-friction client right now?]

TASK: Write a [content type] about [topic] for [specific audience segment].

REVENUE GATE:
[ ] A — This piece should generate a client inquiry or booking within 30 days
[ ] B — This piece retains or deepens an existing client relationship
[ ] C — This piece reduces a current operational cost
[ ] D — This piece has no direct business outcome → DO NOT PRODUCE until A, B, or C are clear

BEST CLIENT TEST: Would [your best client's name or profile] find this immediately useful in their first 7 days with us?
[ ] Yes → proceed
[ ] No → revise the brief before producing

CONSTRAINTS:
- Tone: [from Voice Card]
- Length: [word count]
- Do NOT use: [from Rules Card Layer 1 — forbidden phrases]
- Include: [outcome-specific elements, e.g. a specific number, a real example, one CTA]
- Kill criteria: If the draft could have been written by any agency, rewrite it. Specificity is non-negotiable.

FORMAT: [Output format]

AFTER PRODUCING THE DRAFT:
Run a self-check:
1. Does this pass the Revenue Gate bucket selected above?
2. Would the best client publish this under their name without hesitation?
3. Is there any phrase that sounds like it came from a language model's training data? Remove it.

Flag anything that fails. Do not ship a failing draft.
```

**When to use this:** Any content that touches a client or prospect. Anything going live on a channel. Anything a team member will produce without you in the room.

**What gstack adds over the basic template:**

The basic template tells the AI what to do. The gstack version tells it what not to do and why. The Revenue Gate prevents D-bucket content from getting produced. The Best Client Test prevents technically-correct-but-wrong-audience content. The kill criteria prevent AI slop from clearing the gate unchallenged.

*Principle source: fstack's three core tests — Best Client Test, Maintainability Check, Revenue Gate. Adapted from Garry Tan's "Boil the Lake" and YC's "default alive" framework.*

---

## Version 3 — Anthropic-Standard Template

*Built on Anthropic's published prompt engineering best practices for Claude.*

This version restructures the prompt using techniques that consistently produce higher-quality output from Claude: XML tags for clear section boundaries, explicit reasoning steps, positive and negative examples, and a declared output schema. It also uses Claude's extended thinking preference — telling it to reason before it writes.

```xml
<role>
You are a [role] for [brand]. Your job is to produce [content type] that [specific outcome — e.g., "makes a B2B marketing manager book a discovery call"].
</role>

<context>
<brand_voice>[Paste Voice Card — tone dimensions, sounds-like pairs, platform modifiers]</brand_voice>
<audience>[Specific person: role, company size, pain point, what they've already tried]</audience>
<live_positioning>[Current positioning statement — what you do, for whom, and why it's different]</live_positioning>
<banned_phrases>[List from Rules Card — exact phrases never to use]</banned_phrases>
</context>

<examples>
<good_example>
[Paste a piece of your content that performed well and sounds right]
</good_example>
<bad_example>
[Paste a piece that was off-brand, too generic, or failed — or describe the pattern to avoid]
</bad_example>
</examples>

<task>
Write a [content type] about [topic] for [specific audience].

Think step by step before writing:
1. What does this person already believe about [topic]?
2. What do they need to believe differently after reading this?
3. What is the single most important thing this piece needs to say?
4. What is the one action you want them to take?

Then produce the draft.
</task>

<constraints>
- Tone: [from Voice Card — specific dimension values]
- Length: [word count or line count]
- Do NOT use: [banned phrases]
- Must include: [required elements — e.g., a specific number, a named example, one CTA]
- Format: [structure specification]
</constraints>

<output_format>
Produce your response in this exact structure:

REASONING: [2–3 sentences on the approach you chose and why]
DRAFT: [The content]
SELF-CHECK:
- Voice alignment: [Pass / Fail — note]
- Specificity: [Pass / Fail — note]
- CTA: [Pass / Fail — note]
- Banned phrase scan: [Pass / Fail — list any found]
VERDICT: [Ship / Revise — with specific changes if revising]
</output_format>
```

**When to use this:** When you need Claude specifically. When the content is high-stakes (client-facing, paid campaign, thought leadership). When you want the model to show its reasoning before committing to a draft. When you've had repeated quality issues with a particular content type.

**What Anthropic-standard adds over the basic template:**

XML tags prevent section bleeding — Claude reads the boundaries clearly and doesn't blend context into constraints. The examples block is the highest-leverage addition: a real good example plus a real bad example trains the model on your specific standard, not its default. The step-by-step reasoning prompt forces it to think about the audience before it writes for them. The self-check in the output format means the model audits itself before handing you anything.

*Principle source: Anthropic's prompt engineering documentation — role prompting, XML structure, positive/negative examples, chain-of-thought prompting, output format specification. See: [docs.claude.ai/en/docs/build-with-claude/prompt-engineering/overview](https://docs.claude.ai/en/docs/build-with-claude/prompt-engineering/overview)*

---

## Build Your Own Version

The three versions above are starting points, not rules. Here's the architecture so you can fork any of them.

### The five non-negotiables

Every prompt template — regardless of philosophy — needs these five elements. Remove any one of them and quality degrades predictably.

| Element | What it controls | What breaks without it |
|---|---|---|
| ROLE | The model's frame of reference | Output defaults to "generic helpful assistant" |
| CONTEXT | Brand specificity | Output defaults to average of training data |
| TASK | Output scope | Model decides what to produce |
| CONSTRAINTS | Quality floor | Model fills every gap with defaults |
| FORMAT | Output structure | Model decides how to present the answer |

### Modular additions by use case

Add these to the base structure when the situation calls for it:

**For high-stakes content (client-facing, paid):**
Add a self-check block. Force the model to audit before handing you anything.

**For team use (briefing others, not yourself):**
Add a "Can someone run this without asking me a question?" test. If the answer is no, the brief isn't done.

**For recurring content types:**
Lock the constraints once. Save the template with your brand context pre-loaded. Only swap out TASK per piece.

**For revenue-critical content:**
Add the Revenue Gate. Every piece must be an A, B, or C before it gets produced.

**For Claude specifically:**
Use XML tags. Add examples. Include a step-by-step reasoning prompt before the task. Request the self-check in the output format.

**For models other than Claude:**
Skip XML tags. Use plain headers (##). Keep the structure but remove the schema-heavy output format — most non-Claude models handle looser formatting better.

### The one question that upgrades any template

Before you finalize any prompt, ask: *"Could a different brand use this exact prompt and get output that sounds like them?"*

If yes — your CONTEXT block isn't specific enough. Go back and add more of your brand identity layer before running it.

---

## Quick Reference — Version Picker

| Situation | Use |
|---|---|
| New brief, new team member, clean slate | Version 1 — Basic |
| Client-facing content, revenue-critical piece | Version 2 — gstack |
| High-stakes Claude session, thought leadership, paid campaign | Version 3 — Anthropic |
| Recurring content type you run weekly | Version 1 or 2, saved with pre-loaded context |
| Content that keeps failing brand check | Version 3 — add examples of what failed and why |

---

*Part of fstack — open source operating system for founders and marketers. github.com/likke/fstack*
