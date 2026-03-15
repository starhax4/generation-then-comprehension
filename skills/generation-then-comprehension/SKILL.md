---
name: generation-then-comprehension
description: Use when a junior JavaScript developer wants to understand AI-generated code, not just copy-paste it. After generating any code, always follow up with a comprehension section explaining what the code does, why each part is needed, and what the developer should learn. Triggers on "explain this code", "why does this work", "help me understand", "generation then comprehension", "teach me", or whenever writing code for a developer who wants to grow their skills.
---

# Generation-Then-Comprehension

## Overview

This skill ensures that AI-assisted coding sessions promote genuine learning. Instead of just generating code, the AI always pairs code output with a comprehension follow-up — turning passive copying into active understanding.

Research shows that developers who ask "why does this work?" after AI generation score **65%+ on comprehension** vs. **24–39%** for pure delegators. The behavioral difference is just ~2 extra minutes of follow-up.

## Behavior

When this skill is active, every code generation response includes two parts:

### 1. Generated Code
The requested code, as usual.

### 2. Comprehension Follow-Up
A short follow-up section (≤2 minutes to read) covering:
- **What it does** — a plain-English summary of the code's purpose
- **Why each key part is needed** — line-by-line or block-by-block explanation of non-obvious choices
- **What to learn** — one concept or pattern the developer should look up or practice further

## Example

> **Developer:** "Write a `debounce` function in JavaScript."

**Generated Code:**
```js
function debounce(fn, delay) {
  let timer;
  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn.apply(this, args), delay);
  };
}
```

**Comprehension Follow-Up:**

- **What it does:** Returns a new function that delays invoking `fn` until after `delay` milliseconds have passed since the last time it was called.
- **Why `clearTimeout`?** It cancels any previously scheduled invocation so only the last call in a burst actually fires.
- **Why `fn.apply(this, args)`?** It preserves the calling context and forwards any arguments to the original function.
- **What to learn:** Closures — `timer` lives in the closure scope so each debounced function has its own independent timer.

## Target Audience

Junior JavaScript developers who want to grow their skills, not just ship code.

## References

- [The Generation Effect (Wikipedia)](https://en.wikipedia.org/wiki/Generation_effect)
- [Make It Stick: The Science of Successful Learning (book)](https://www.hup.harvard.edu/books/9780674729018)
