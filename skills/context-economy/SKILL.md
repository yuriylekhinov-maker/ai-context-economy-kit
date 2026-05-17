---
name: context-economy
description: Use when the user asks to work efficiently with context, reduce token or cost overhead, avoid unnecessary file reads, keep outputs concise, or proactively point out cheaper ways to execute broad requests. Apply to coding, research, project review, debugging, documentation, and multi-file work where scope control matters.
---

# Context Economy

Work in a context-efficient mode without sacrificing correctness.

## Core Rules

- Read only the minimum context needed for the current task.
- Prefer project maps, README files, current-state files, briefs, and direct search before opening large files.
- Do not read large files fully when targeted search by function, class, id, error text, UI text, or keyword is enough.
- Avoid reading archives, old planning documents, logs, generated files, images, assets, dependency folders, and large dumps unless directly relevant.
- If the user's request is broad, identify the smallest useful scope before doing heavy analysis.
- If the request can be done cheaper, say `Можно дешевле:` and propose a shorter or more targeted version.
- Before edits, state which files or areas will be touched.
- Prefer minimal changes that match the existing project style.
- Do not perform wide refactors, architecture changes, or mass rewrites without explicit confirmation.
- Run only relevant checks or tests instead of the full suite unless the risk justifies it.
- Keep final answers short: changed files, verification, remaining risks.
- If the chat becomes long or context-heavy, propose a compact handoff summary for a new chat.

## Default Workflow

1. Understand the user's concrete goal.
2. Inspect minimal orientation files if available.
3. Search for the relevant code or documents.
4. Read only the necessary fragments.
5. Make the smallest effective change or answer.
6. Verify with focused checks.
7. Report concisely.

## Cheapness Warning

When a user asks for something like `analyze everything`, `review the whole project`, `read all files`, `make it better`, or `check everything`, suggest a narrower alternative before proceeding.

For Russian-language chats, phrase the warning naturally:

`Можно дешевле: вместо полного анализа всего проекта сначала проверить только <область/файлы/симптом>.`
