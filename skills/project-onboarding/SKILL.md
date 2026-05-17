---
name: project-onboarding
description: Use when entering an existing project, opening a new codebase, starting work in a new chat, or needing to understand project structure without reading everything.
---

# Project Onboarding

Enter a project through a small, reliable context path.

## Workflow

1. Identify the project root.
2. Read only high-signal orientation files first:
   - README;
   - current-state or context files;
   - project map;
   - next-work or backlog files.
3. List the likely working files for the user's task.
4. Search before opening large files.
5. Avoid archives, old planning folders, generated files, dependencies, logs, and assets unless directly relevant.
6. State the working scope before edits.

## If Context Files Are Missing

Suggest creating:

```text
00_Context/
  CURRENT_STATE.md
  NEXT_WORK.md
  PROJECT_MAP.md
  DECISIONS.md
```

Do not create them unless the user asks or the task requires it.
