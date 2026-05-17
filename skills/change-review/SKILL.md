---
name: change-review
description: Use after code, document, or project changes to verify the change scope, summarize modified files, check focused tests, and identify risks without rereading the whole project.
---

# Change Review

Review what changed with minimal context.

## Workflow

1. Inspect the changed file list.
2. Separate intended changes from unrelated existing changes.
3. Review only the relevant diffs or file sections.
4. Run focused checks that match the change.
5. Report concise results.

## Final Report

Use:

```text
Changed:
- <file>: <change>

Verified:
- <command/check>

Risks:
- <remaining risk or "none obvious">
```

## Rules

- Do not revert unrelated user changes.
- Do not run expensive full-suite checks unless risk justifies it.
- If the diff is huge, summarize by area and inspect the highest-risk sections first.
