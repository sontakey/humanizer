# Humanizer

Humanizer is an opinionated writing skill for Claude Code and OpenCode.

It takes AI-shaped prose and rewrites it so it sounds like a person wrote it on purpose.

That is the whole point.

Most AI writing is not bad because it is ungrammatical. It is bad because it sounds like nobody made any choices. The sentences are smooth, but dead. The transitions are clean, but generic. The tone is polished, but synthetic. The structure feels like a model performing usefulness.

Humanizer exists to fix that.

## What this repo is based on

This repo builds on the original humanizer skill and pushes it further in a more opinionated direction.

The original repo was already useful because it treated AI writing as a pattern-recognition problem, not just a vocabulary cleanup problem. It focused on recurring tells such as:
- inflated significance
- vague attribution
- trailing `-ing` analysis that says nothing
- ornate or promotional language
- AI-heavy vocabulary clusters
- formulaic transitions and conclusions
- formatting residue from chatbot output

That core idea is still right. Good editing is not just replacing a few suspicious words. It is noticing when the prose performs depth instead of delivering it.

This version keeps that foundation and adds a harder edge.

## What was added from the tropes references

A lot of AI writing does not only sound generic. It also sounds theatrically AI.

That is where the tropes references helped.

The tropes material, especially the writing patterns collected in the referenced gist from tropes.fyi, is useful because it names the rhetorical habits models fall into when they try too hard to sound sharp, profound, or dramatic.

Those patterns include:
- negative parallelism like `It's not X. It's Y.`
- dramatic countdowns like `Not this. Not that. This.`
- self-posed rhetorical questions like `The result? Disaster.`
- repeated sentence openings
- false suspense transitions like `Here's the kicker`
- patronizing analogy setups like `Think of it as...`
- fake vulnerability and polished self-awareness
- inflated stakes for narrow points
- listicles disguised as prose
- em dash abuse and other visible AI formatting habits

These are not just stylistic quirks. They create a very specific kind of fake intensity that now reads as machine-generated to anyone who spends time around model output.

Humanizer uses those references to catch the rhetorical layer, not just the lexical layer.

## What Humanizer actually does

Humanizer is designed to do four things well:

### 1. Remove obvious AI tells
It catches the common markers that make prose feel generated, including vocabulary choices, sentence templates, weak transitions, and fake analysis.

### 2. Preserve meaning
It should not hallucinate facts, invent anecdotes, or add fake specificity just to sound more human.

### 3. Preserve voice
If you give it a writing sample, it should move toward your cadence and habits instead of flattening everything into generic "good writing."

### 4. Improve judgment, not just surface polish
The real goal is not to make the writing more decorative. The goal is to make it sound like someone made decisions.

## What makes this different

A lot of "humanizer" tools are really just one of these two things:
- synonym replacers
- personality injectors

Both fail.

Synonym replacement leaves the structure intact, so the prose still sounds generated.

Personality injection often makes things worse. It replaces AI stiffness with fake swagger, fake grit, or LinkedIn-guy energy.

Humanizer is different because it is built around judgment:
- what should stay
- what should go
- what should be simplified
- what should be said directly
- what should not be made more dramatic than it is

That is closer to real editing.

## Design principles

Humanizer assumes a few things:

### AI writing usually fails at the performance layer
A sentence can be technically fine and still feel fake.

### Fake depth is one of the biggest tells
A lot of AI prose keeps explaining why something matters instead of simply saying something concrete.

### Plain verbs are underrated
Models dodge `is`, `has`, and other simple constructions because they are optimizing for variation. Humans use plain language when it is the clearest option.

### Rhythm matters
A piece can fail because every sentence lands with the same cadence, the same structure, or the same kind of emphasis.

### Restraint matters
Not every paragraph needs a reveal, a twist, a contrast, or a grand conclusion.

## What the skill covers

The skill currently covers patterns like:
- significance inflation
- fake depth via trailing `-ing` phrases
- promotional language
- vague attribution
- copula avoidance
- passive voice and subjectless fragments
- rule-of-three overuse
- false ranges
- synonym cycling
- hyphenated word-pair overuse
- negative parallelism
- dramatic countdowns
- rhetorical question reveals
- repeated sentence openings
- false suspense transitions
- persuasive authority tropes
- stakes inflation
- simulated self-awareness
- invented concept labels
- staccato fragment abuse
- circular padding
- chatbot pleasantries
- signposting and tutorial voice
- pedagogical analogies
- generic positive conclusions
- em dash addiction
- bold-first bullet formatting
- unicode decoration and other visible output residue

## Example

### Before

> Great question. Here's what you need to know.
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

## Who this is for

Humanizer is especially useful for:
- founder writing
- executive updates
- internal memos
- customer-facing copy
- essays
- strategic documents
- technical writing that still needs a human voice
- any draft that started with AI and needs to survive contact with smart readers

## How to use it

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

Then invoke it with a draft, or with a draft plus a voice sample.

### Basic prompt

```text
/humanizer

[paste draft]
```

### Voice match prompt

```text
/humanizer

Here is a sample of my writing:
[paste sample]

Now rewrite this in my voice:
[paste draft]
```

### High-stakes pass

```text
/humanizer

This is customer-facing. Do a full humanize pass, run the anti-AI audit, and give me the final version only.

[paste draft]
```

## Philosophy in one line

The job is not to make AI writing quirky.

The job is to make it sound real.

## Sources and lineage

This repo is informed by:
- the original humanizer skill structure and anti-AI editing approach
- Wikipedia's "Signs of AI writing" and related cleanup guidance
- tropes.fyi pattern observations
- the tropes reference gist by ossa-ma: <https://gist.github.com/ossa-ma/f3baa9d25154c33095e22272c631f5a1>

## License

MIT
