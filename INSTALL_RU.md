# Установка

## Установка одного навыка

Выберите навык из папки `skills` и скопируйте его в папку пользовательских навыков Codex.

Windows:

```powershell
Copy-Item -Recurse .\skills\context-economy "$env:USERPROFILE\.codex\skills\context-economy"
```

macOS/Linux:

```bash
cp -R ./skills/context-economy ~/.codex/skills/context-economy
```

После установки начните новый чат и напишите:

```text
Используй навык context-economy.
```

## Установка всех навыков

Windows:

```powershell
Copy-Item -Recurse .\skills\* "$env:USERPROFILE\.codex\skills\"
```

macOS/Linux:

```bash
cp -R ./skills/* ~/.codex/skills/
```

## Проверка

В новом чате попросите:

```text
Используй навык project-onboarding и войди в этот проект экономно по контексту.
```

Если Codex видит навык, он должен следовать его правилам.
