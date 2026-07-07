# Contributing

## Ideas welcome

- Additional anti-patterns you've seen in AI output (with before/after examples)
- Craft principles from other copywriting traditions
- Domain-specific reference files (legal writing, medical, finance, academic)
- Translations (the skill matches input language, but the checklist is English-first)
- Bug reports: cases where the skill flags something that's actually good writing

## How to contribute

1. Fork the repo
2. Make your changes
3. Run the validation: the CI checks JSON syntax, frontmatter, and banned vocabulary in the README
4. Submit a PR with a clear description of what you added and why

## Structure

When adding content, put it in the right place:

| What | Where |
|------|-------|
| Core skill rules | `SKILL.md` (then copy to `kiro/`, `claude/`, `plugins/`) |
| Reference material | `references/` |
| ChatGPT version | `chatgpt/PROMPT.md` (condensed, no frontmatter) |
| Examples | `examples/` (create if needed) |

## Style

This repo practices what it preaches. Your PR should:

- Use short words over long ones
- Have zero em dashes
- Use sentence case for headings
- Not introduce any banned vocabulary into prose (quoting as examples is fine)
