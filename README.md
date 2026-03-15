# generation-then-comprehension

> An AI skill that pairs every code generation with a comprehension follow-up, turning passive copying into active learning.

This skill exists because the developer using you is a junior JS developer who wants to grow their skills — not just ship code. Research shows that developers who ask "why does this work?" after AI generation score **65%+** on comprehension vs. 24–39% for pure delegators. The behavioral difference is just ~2 extra minutes of follow-up.

## Installation

### Via [skills.sh](https://skills.sh)

Search for **generation-then-comprehension** on [skills.sh](https://skills.sh) and follow the one-click install instructions for your AI coding assistant.

### Manual install

Add this skill to your AI coding assistant by pointing it at the skill file:

```
skills/generation-then-comprehension/SKILL.md
```

Or copy the contents of [`skills/generation-then-comprehension/SKILL.md`](skills/generation-then-comprehension/SKILL.md) directly into your assistant's system prompt / custom instructions.

## What it does

When active, the skill changes every coding response into two parts:

1. **Generated code** — the requested implementation, as usual.
2. **Comprehension follow-up** — a short (~2 min) explanation covering:
   - What the code does in plain English
   - Why each non-obvious part is needed
   - One concept or pattern to explore further

See [`skills/generation-then-comprehension/SKILL.md`](skills/generation-then-comprehension/SKILL.md) for the full skill definition, including a worked example.

## License

[MIT](LICENSE)
