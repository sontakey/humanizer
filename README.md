# Humanizer

**Sameer Sontakey's opinionated anti-AI writing system** for Claude Code and OpenCode.

Most "humanize this" prompts do one of two bad things:
- they barely change the text, so it still sounds like ChatGPT wearing loafers
- or they overcorrect into fake personality, fake grit, and weird LinkedIn-guy prose

This repo exists to do the opposite.

It is a practical writing skill for taking AI-shaped text and making it sound like it came from a real person with taste, judgment, and an actual point of view.

## What it does

Humanizer helps remove the tells that make writing feel generated:
- inflated significance
- canned profundity
- AI vocabulary clusters
- overexplained transitions
- tutorial voice
- fake suspense
- em dash addiction
- listicle formatting residue
- chatbot pleasantries
- vague authority gestures
- generic upbeat conclusions
- rhetorical tropes that feel statistically assembled instead of genuinely written

It does **not** try to turn every piece of writing into casual banter.

The goal is not "sound quirky." The goal is **sound real**.

## Why this is better

Most anti-AI writing guides stop at surface cleanup.

This one goes further:

### 1. It treats AI writing as a pattern problem, not a word-replacement problem
It does not just swap out a few obvious phrases. It targets the deeper habits that make text feel machine-generated: rhythm, padding, rhetorical staging, fake depth, and synthetic certainty.

### 2. It combines two useful lenses
This skill merges:
- **Wikipedia / WikiProject AI Cleanup** style signals, which are great for factual and structural cleanup
- **tropes.fyi** style rhetorical signals, which are great for catching the smug, dramatic, over-signposted patterns LLMs fall into

That combination matters. A lot of AI writing is not wrong at the sentence level. It is wrong at the *performance* level.

### 3. It preserves voice instead of flattening everything
If you provide a writing sample, the skill is supposed to match your real cadence and habits instead of imposing generic "clean prose."

### 4. It is opinionated about what bad AI writing actually looks like
This is not neutral. It has taste.

It assumes bad AI writing often looks like:
- padded
- overconfident
- emotionally synthetic
- theatrically structured
- allergic to plain verbs
- addicted to telling you why something matters instead of showing you

### 5. It includes a final anti-AI audit pass
The skill explicitly asks:
1. **What makes the below so obviously AI generated?**
2. **Now make it not obviously AI generated.**

That second pass catches a lot of residue the first pass misses.

## Who this is for

This skill is especially good for:
- founder writing
- executive updates
- internal memos
- customer-facing copy
- essays
- strategic docs
- technical explanations that still need to sound like a person wrote them
- rewrites of model-generated drafts before they leave your machine

## What’s in the skill

The current version includes a structured pattern library covering:
- significance inflation
- fake depth via trailing `-ing` phrases
- promotional language
- vague attribution
- copula avoidance (`serves as`, `stands as`, `boasts`)
- passive voice and subjectless fragments
- rule-of-three overuse
- false ranges
- synonym cycling
- hyphenated word pair overuse
- the "It's not X. It's Y." reframe
- dramatic countdowns
- rhetorical questions used as suspense
- repeated sentence openings
- false suspense transitions
- persuasive authority tropes
- stakes inflation
- simulated self-awareness
- invented compound labels
- staccato fragments
- circular padding
- chatbot pleasantries
- knowledge-cutoff disclaimers
- signposting and tutorial voice
- pedagogical analogies
- generic conclusions
- formatting tells like em dashes, bold-label lists, emojis, arrows, and title-case headings

## Example

### Before

> Great question! Here's what you need to know.
>
> AI-assisted coding represents a pivotal shift in the evolving landscape of software development, highlighting the transformative potential of these groundbreaking tools. It's not just about speed, it's about unlocking creativity, fostering alignment, and ensuring organizations can remain agile in an increasingly complex environment.
>
> The result? A powerful new era of innovation.

### After

> AI coding tools can save time on repetitive work. They're useful for boilerplate, rough drafts, and some test scaffolding.
>
> The problem is that they also sound confident when they're wrong. If you stop paying attention, they help you make mistakes faster.
>
> They're useful. They're not magic.

## Installation

### Claude Code

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/sontakey/humanizer.git ~/.claude/skills/humanizer
```

### OpenCode

```bash
mkdir -p ~/.config/opencode/skills
git clone https://github.com/sontakey/humanizer.git ~/.config/opencode/skills/humanizer
```

> OpenCode can also read skills from `~/.claude/skills`, so one install there may be enough.

## Usage

### Basic

```text
/humanizer

[paste text]
```

Or:

```text
Please humanize this text: [text]
```

### Voice match mode

```text
/humanizer

Here's a sample of my writing for voice matching:
[paste 2-3 paragraphs of your own writing]

Now humanize this:
[paste text]
```

### High-stakes rewrite

```text
/humanizer

This is customer-facing copy. Do a full humanize pass, then run the anti-AI audit and give me the final version only.

[paste text]
```

## Design philosophy

A lot of AI writing is competent in the most dangerous way possible.

It is grammatical. It is smooth. It is polished. And it is dead.

Dead writing is usually not broken at the sentence level. It is broken at the judgment level. It sounds like nobody chose anything. The sentences feel statistically assembled. The emphasis is fake. The transitions are canned. The voice is generic. The structure feels like a model trying to look useful.

That is what this skill is designed to catch.

## Version

**Current version:** `3.0.0`

## License

MIT
