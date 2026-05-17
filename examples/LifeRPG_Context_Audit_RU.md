# Пример аудита: Example Project

Дата проверки: 2026-05-17

Проект:

```text
C:\Users\<user>\Documents\Example_Project
```

## Итог

Проект хорошо подходит для экономной работы с ИИ, потому что уже содержит папку `07_Context` с актуальным состоянием, следующими задачами и картой проекта.

Основные источники лишнего расхода контекста:

- большой монолитный `04_Prototype/app.js`;
- крупный `04_Prototype/styles.css`;
- дубли документации между `00_Planning` и рабочими папками;
- крупные изображения в `06_Assets`;
- незакоммиченные изменения, которые усложняют ориентацию.

## Что читать в новом чате

Достаточно начать с:

```text
07_Context/CURRENT_STATE.md
07_Context/NEXT_WORK.md
07_Context/PROJECT_MAP.md
```

`00_Planning` лучше считать архивом и не читать без явной причины.

## Размеры, влияющие на контекст

- `04_Prototype/app.js`: около 198 KB, 3636 строк.
- `04_Prototype/styles.css`: около 36 KB, 1923 строки.
- `04_Prototype/index.html`: около 21.6 KB, 433 строки.
- `07_Context/CURRENT_STATE.md`: около 10.3 KB, 101 строка.

## Дубли документации

Найдены пары одинаковых файлов:

```text
00_Planning/02_Product_Brief.md = 01_Product/ProductBrief.md
00_Planning/06_Game_Design.md = 01_Product/GameDesign.md
00_Planning/07_Vertical_Slice_Body_Strength.md = 01_Product/VerticalSlice_BodyStrength.md
00_Planning/09_Monetization_Policy.md = 01_Product/MonetizationPolicy.md
00_Planning/10_Market_Notes.md = 02_Research/MarketNotes.md
00_Planning/11_LevelUp_Inspiration.md = 02_Research/LevelUp_Inspiration.md
00_Planning/12_Sources.md = 01_Product/Sources.md
00_Planning/13_Legal_Notes.md = 03_Legal/LegalNotes.md
```

Рекомендация: в новых запросах прямо писать, что `00_Planning` является архивом.

## Git-состояние на момент проверки

Есть незакоммиченные изменения:

```text
04_Prototype/app.js
04_Prototype/index.html
04_Prototype/styles.css
07_Context/CURRENT_STATE.md
07_Context/NEXT_WORK.md
02_Research/Sensei_Calendar_Archive_Sources_2026-05-17.md
```

Рекомендация: перед крупными задачами фиксировать точку состояния через commit или handoff-summary.

## Проверка промптов

### START EXISTING PROJECT

Работает хорошо: промпт естественно приводит к чтению только `07_Context` и карты проекта.

### FIX BUG CHEAP

Работает хорошо, если пользователь указывает симптом и сценарий. Для такого проекта важно добавлять ограничение: `app.js` не читать целиком, искать функции через `rg`.

### REVIEW UI CHEAP

Работает хорошо для задач вроде мобильной проверки 360-430 px. Должен ограничиваться `index.html`, `styles.css`, релевантными функциями UI в `app.js` и браузерной проверкой.

### CONTINUE IN NEW CHAT

Работает особенно хорошо, потому что в проекте уже есть `07_Context`.

### BEFORE BIG REFACTOR

Актуален для будущего разделения большого `app.js`. Пока правильная рекомендация: не рефакторить весь файл, а сначала выделять зоны риска и менять точечно.

## Рекомендуемый стартовый запрос для похожего проекта

```text
Используй context-economy и project-onboarding.

Проект: C:\Users\<user>\Documents\Example_Project

Сначала прочитай только:
- 07_Context/CURRENT_STATE.md
- 07_Context/NEXT_WORK.md
- 07_Context/PROJECT_MAP.md

00_Planning не читать без явной причины: это архив.
04_Prototype/app.js не читать целиком; сначала искать нужные функции через rg.

Моя задача:
<задача>
```
