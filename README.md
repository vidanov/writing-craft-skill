# Writing Craft Skill

A reusable skill for AI coding agents (Claude Code, Kiro CLI, Cursor, VS Code Copilot) that teaches the agent to **write well**, not just avoid sounding like AI.

## What makes this different

The humanizer skills strip AI patterns. This skill adds craft.

| Humanizer skills | This skill |
|-----------------|------------|
| Remove AI vocabulary | Teach short words, concrete nouns, active verbs |
| Detect structural patterns | Teach sentence rhythm, the slippery slide, loss framing |
| Generic voice profiles (casual/professional) | Match a specific author's voice from a sample |
| Fix existing text | Write well from scratch AND fix existing text |
| Pattern matching (defensive) | Writing craft (generative) + pattern matching |

## Principles inside

Classic copywriting craft applied to technical writing:

- **Ogilvy**: Short words, short sentences, short paragraphs. Write like you talk.
- **Sugarman**: The slippery slide. Every sentence's only job is to make you read the next one.
- **Zinsser**: Cut every word that doesn't do useful work. Kill qualifiers, filler, throat-clearing.
- **Hemingway**: Active verbs. Concrete details. Be positive, not negative.
- **Deutsch**: The editing IS the craft. Show, don't explain. Copy works like music.

Plus a 24-category AI anti-pattern checklist (vocabulary, structural, formatting, content, rhythm).

## Installation

### Claude Code / Kiro CLI

Copy `SKILL.md` to your project or user skills directory:

```bash
# Project-level (shared via git)
cp SKILL.md .kiro/skills/writing-craft/SKILL.md

# Or user-level
cp SKILL.md ~/.kiro/skills/writing-craft/SKILL.md
```

### Cursor / VS Code Copilot

Add to your project's `.cursor/rules/` or equivalent agent instructions directory.

### Any agent that reads markdown instructions

Copy the content of `SKILL.md` into your system prompt or agent configuration.

## Usage

The skill activates when you ask the agent to write, edit, review, or improve text:

```
write a blog post about integration testing on AWS
```

```
edit this draft — make it sound less like AI
```

```
review this LinkedIn post for AI patterns
```

```
=C=
[paste text here]
```

The `=C=` trigger means: grammar, clarity, readability rewrite only. Output corrected text. No commentary.

## What it catches

**Vocabulary**: 80+ flagged words across three tiers (always-flag, cluster-flag, density-flag)

**Structure**: Significance inflation, empty participle phrases, negative parallelism overuse, the "Despite" formula, copula avoidance, synonym cycling

**Formatting**: Em dash overuse, excessive boldface, inline-header lists, title case headings

**Content**: Vague attributions, chatbot artifacts, conclusion summaries, "Let's" constructions, rhetorical question openers

**Rhythm**: Sentence length uniformity, paragraph uniformity, missing first-person perspective

## What it teaches (that others don't)

- Lead with the point, not the setup
- One idea per sentence, one thought per paragraph
- Loss framing over gain framing
- The knowledge advantage: know the subject deeper than anyone else writing about it
- The Ogilvy test: read it aloud, if you wouldn't say it that way, rewrite it
- Rhythm variation: mix 5-word punches with 22-word flows
- Experience markers: include observations from real work, not abstract claims

## Customization

### Voice matching

Provide a writing sample and the skill will match your specific patterns:

```
Match my voice — here's a recent post: [paste sample]
```

The skill analyzes sentence-length, contraction rate, paragraph openings, and register, then matches those instead of defaulting to generic "professional."

### Domain-specific extensions

Add a `references/` directory with domain-specific rules:

```
writing-craft/
├── SKILL.md
└── references/
    └── aws-service-names.md    # AWS naming conventions
    └── your-domain-terms.md    # Your industry terminology
```

## License

MIT

## Credits

Craft principles distilled from: David Ogilvy (Ogilvy on Advertising), Joseph Sugarman (The Adweek Copywriting Handbook), William Zinsser (On Writing Well), Gary Halbert (The Boron Letters), Ernest Hemingway, David Deutsch.

AI anti-pattern research informed by: Wikipedia WikiProject AI Cleanup, Liang et al. (Stanford, 2023), and community projects including [conorbronsdon/avoid-ai-writing](https://github.com/conorbronsdon/avoid-ai-writing) and [blader/humanizer](https://github.com/blader/humanizer).
