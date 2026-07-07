<h1 align="center">✍️ writing-craft-skill</h1>

<div align="center">

**Teach AI agents to write well, not just avoid sounding like AI.**

[Quick start](#quick-start) · [What's inside](#whats-inside) · [How it's different](#how-its-different) · [Voice calibration](#voice-calibration) · [License](#license)

</div>

---

The humanizer skills strip AI patterns. This skill adds craft.

Short words. Concrete images. Sentence rhythm. The slippery slide. Loss framing. The editing discipline that turns a first draft into writing that holds attention.

Models are trained to produce text that's pleasant to skim and hard to disagree with. RLHF rewards smooth, safe, hedged prose. This skill teaches the opposite: writing specific enough to disagree with, concrete enough to be wrong about something, sharp enough that a reader who skims will miss the point.

## Quick start

Copy one file. That's the install.

```bash
# Claude Code / Kiro CLI (project-level, shared via git)
mkdir -p .kiro/skills/writing-craft
cp SKILL.md .kiro/skills/writing-craft/SKILL.md
```

```bash
# User-level (applies to all your projects)
mkdir -p ~/.kiro/skills/writing-craft
cp SKILL.md ~/.kiro/skills/writing-craft/SKILL.md
```

Works with any agent that reads markdown instructions: Claude Code, Kiro CLI, Cursor, VS Code Copilot, OpenHands.

## What's inside

The skill has two modes:

**Write mode** — draft content from scratch using craft principles. Opens concrete, grounds every claim, closes with action.

**Edit mode** — review existing text, flag problems, rewrite flagged passages. Triggered by "edit this," "review this," or `=C=` (grammar/clarity only).

### Craft principles (the generative half)

Classic copywriting applied to technical writing:

- 🔤 **Word choice** (Ogilvy/Halbert): "use" not "utilize," concrete nouns, active verbs, cut adverbs
- 📐 **Sentence craft** (Sugarman): the slippery slide, short first sentences, one idea per sentence
- 📄 **Paragraph craft** (Zinsser): lead with the point, one thought per paragraph, kill throat-clearing
- 🎵 **Rhythm** (Deutsch): copy works like music, vary length, reprise themes
- 🎯 **Loss framing**: frame what the reader loses by not acting, not what they gain
- 🔍 **Knowledge advantage**: specific frustration beats general benefit
- ✂️ **The editing principle**: "I'm not a great writer, but I'm a hell of an editor" (Ogilvy)

### Anti-pattern checklist (the defensive half)

24 categories of AI writing tells, organized by type:

| Category | Examples |
|----------|----------|
| **Vocabulary** (3 tiers) | delve, tapestry, leverage, robust, seamless, harness, foster, resonate |
| **Structure** | Significance inflation, empty -ing phrases, "Despite" formula, copula avoidance |
| **Formatting** | Em dash overuse, bold-as-study-guide, inline-header lists |
| **Content** | Vague attribution, chatbot artifacts, "Let's explore," rhetorical questions |
| **Rhythm** | Sentence uniformity, paragraph uniformity, missing first-person, over-polishing |

## How it's different

|  | Generic humanizers | This skill |
|--|-------------------|------------|
| **Goal** | "Don't sound like AI" | "Sound like a practiced author" |
| **Method** | Pattern matching (defensive) | Craft principles (generative) + pattern matching |
| **Voice** | Template profiles (casual/professional/blunt) | Calibrated to YOUR writing from a sample |
| **Writing** | Fixes existing text only | Writes well from scratch AND fixes existing text |
| **Depth** | Word swaps and structural flags | Why AI writing fails (RLHF mode collapse) and what to do instead |

The competitors (blader/humanizer at 28k stars, conorbronsdon/avoid-ai-writing) are excellent at removing patterns. They don't teach craft. They produce clean text that reads like... clean text. Not like a person with experience and opinions wrote it.

## Voice calibration

The skill doesn't impose one voice. Provide a writing sample and it matches your patterns:

```
Match my voice — here's a recent post: [paste 3-5 paragraphs]
```

It analyzes: sentence length, contraction rate, opening patterns, register, recurring constructions. Then enforces craft principles within YOUR voice, not a generic template.

See [`references/voice-calibration-guide.md`](references/voice-calibration-guide.md) for a full walkthrough on building a permanent voice profile.

## When NOT to use this

| Situation | Better choice |
|-----------|--------------|
| You need to bypass AI detectors (academic) | This is a craft tool, not a cheating tool |
| You want a grammar-only check | Use a grammar tool; this rewrites for craft |
| Your text is code documentation | Code docs need clarity, not voice; use plain style guides |
| You want longer, more detailed output | This skill cuts. It makes things shorter, not longer. |

## Extending

Add domain-specific rules in `references/`:

```
writing-craft/
├── SKILL.md
└── references/
    ├── voice-calibration-guide.md
    ├── your-industry-terms.md      # Terminology conventions
    └── your-style-overrides.md     # Company/publication style rules
```

The skill loads reference files when relevant context is detected.

## Contributing

Ideas welcome:

- Additional anti-patterns you've seen in AI output (with examples)
- Craft principles from other copywriting traditions
- Domain-specific reference files (legal writing, medical, finance)
- Translations (the skill matches input language, but the checklist is English-first)

## License

MIT — use it, fork it, sell courses around it, put it in your product.

## Credits

Craft principles from: David Ogilvy, Joseph Sugarman, William Zinsser, Gary Halbert, Ernest Hemingway, David Deutsch.

AI anti-pattern research informed by: Wikipedia WikiProject AI Cleanup, Liang et al. (Stanford, 2023), and community work including [avoid-ai-writing](https://github.com/conorbronsdon/avoid-ai-writing) and [humanizer](https://github.com/blader/humanizer).
