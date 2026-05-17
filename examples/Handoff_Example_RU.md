# Пример handoff-summary

Project:
Example Project

Path:

```text
C:\Users\<user>\Documents\Example_Project
```

Current Goal:
Подготовить локальный браузерный прототип к первому ручному тесту.

Current State:
- Есть рабочий прототип в `04_Prototype`.
- Основной актуальный контекст лежит в `07_Context`.
- Главный цикл: сферы, ежедневные задания, принятие квеста, выполнение, XP/ОР, история.
- Следующие задачи: ручной desktop-сценарий, мобильная ширина, 3-дневный тест.

Important Decisions:
- `00_Planning` является архивом, не рабочим источником правды.
- ИИ-сенсей, сеть, аккаунты, рейтинги и платные функции отложены.
- Сервер нужно запускать из корня проекта, не из `04_Prototype`.

Relevant Files:
- `07_Context/CURRENT_STATE.md`: текущее состояние.
- `07_Context/NEXT_WORK.md`: ближайшие задачи.
- `07_Context/PROJECT_MAP.md`: карта проекта.
- `04_Prototype/app.js`: логика прототипа, большой файл.
- `04_Prototype/styles.css`: стили.
- `04_Prototype/index.html`: структура UI.

Next Work:
1. Пройти прототип вручную как пользователь.
2. Проверить мобильную ширину 360-430 px.
3. Подготовить 3-дневный тест.

Do Not Do:
- Не читать `00_Planning` без причины.
- Не читать `app.js` целиком без необходимости.
- Не добавлять сеть, аккаунты, рейтинги, ИИ-сенсея и платежи.

Suggested Start Prompt:

```text
Используй context-economy и project-onboarding.
Прочитай только 07_Context/CURRENT_STATE.md, 07_Context/NEXT_WORK.md и 07_Context/PROJECT_MAP.md.
Дальше работай точечно по моей задаче.
```
