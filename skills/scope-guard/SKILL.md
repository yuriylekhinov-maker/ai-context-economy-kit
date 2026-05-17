---
name: scope-guard
description: Use when a request is broad, ambiguous, likely to expand, or needs explicit boundaries before coding, refactoring, reviewing, researching, or planning.
---

# Scope Guard

Keep work bounded and useful.

## Before Heavy Work

Clarify or infer:

- concrete goal;
- files or areas likely involved;
- what should not be changed;
- definition of done;
- minimum useful first step.

## Rules

- If the user asks for "everything", propose a smaller first pass.
- Do not start broad refactors from vague requests.
- Prefer one task, one module, or one user flow at a time.
- Call out when a cheaper scoped version would answer the real need.
- Ask a question only when guessing would be risky; otherwise choose a conservative scope and proceed.

## Cheap Alternative Format

Use:

```text
Можно дешевле: сначала проверить <small scope>. Если там подтвердится проблема, расширим анализ.
```
