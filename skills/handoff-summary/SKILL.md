---
name: handoff-summary
description: Use when the user needs to continue work in a new chat, compact a long conversation, summarize project state, preserve decisions, or reduce future context cost by creating a short handoff summary.
---

# Handoff Summary

Create compact summaries that let a new chat continue work without reading the full history.

## Output Structure

Use this structure unless the user asks otherwise:

```text
Project:
<name and path if known>

Current Goal:
<one or two sentences>

Current State:
- <what exists now>
- <what was recently changed>

Important Decisions:
- <decision and reason>

Relevant Files:
- <path>: <why it matters>

Next Work:
1. <next practical step>
2. <next practical step>

Do Not Do:
- <known constraints>

Suggested Start Prompt:
<short prompt for the next chat>
```

## Rules

- Keep the summary short enough to paste into a new chat.
- Prefer current state over historical detail.
- Include file paths and commands only when useful.
- Do not include long logs, full code, or long explanations.
- If the project has context files, recommend updating them instead of relying only on chat history.
