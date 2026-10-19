# BeedBrowser

**Быстрый. Минималистичный. Твой.**

*Fast. Minimal. Yours.*

Спокойный браузер для Windows на Electron, React и TypeScript.

*A calm Windows browser built with Electron, React and TypeScript.*

![Главный экран BeedBrowser](docs/home.png)

---

## Русский

### Что это

BeedBrowser — браузер без лишнего: графитовая поверхность, волосяные линии,
интерфейс на русском языке. Всё, что не нужно каждый день, убрано в меню и
настройки, а не вынесено на экран.

### Возможности

| Раздел | Что умеет |
| --- | --- |
| Окно | Безрамочное, фон заполняет всё окно, квадратные кнопки управления |
| Вкладки | Создание, закрытие, дублирование, закрепление, меню по правой кнопке |
| Адресная строка | Поиск и переход по адресу, замок для HTTPS |
| Левое меню | Главная, вкладки, закладки, история, загрузки, настройки; сворачивается в иконки |
| Главный экран | Часы, погода, поиск, быстрые ссылки, закладки, последние посещения |
| Контекстные меню | Текст, ссылки, картинки, поля ввода |
| Настройки | Основные, вкладки, безопасность, конфиденциальность, внешний вид, синхронизация, документы, соц сети, о браузере |
| Внешний вид | Тёмная, светлая или системная тема, три плотности, масштаб страниц |

### Скриншоты

| Компактное меню | Контекстное меню |
| --- | --- |
| ![Компактное левое меню](docs/compact.png) | ![Контекстное меню страницы](docs/context-menu.png) |
| *Только иконки, без подписей* | *Правая кнопка на странице* |

| Светлая тема | Документы |
| --- | --- |
| ![Светлая тема](docs/light.png) | ![Политика и соглашение](docs/documents.png) |
| *Тема и настройки внешнего вида* | *Политика конфиденциальности и соглашение* |

| Поиск | Загрузки |
| --- | --- |
| ![Поиск](docs/search.png) | ![Загрузки](docs/downloads.png) |
| *Открывает настоящую выдачу* | *Список файлов* |

### Запуск

- `release/BeedBrowser.exe` — портативная сборка, установка не нужна.
- `release/BeedBrowser-Setup.exe` — установщик с выбором языка (русский или английский).

### Горячие клавиши

| Клавиши | Действие |
| --- | --- |
| `Ctrl` + `T` | Новая вкладка |
| `Ctrl` + `W` | Закрыть вкладку |
| `Ctrl` + `L` или `Ctrl` + `K` | Перейти в адресную строку |
| `Ctrl` + `R` | Обновить страницу |
| `Ctrl` + `D` | Добавить страницу в закладки |
| `Ctrl` + `,` | Настройки |
| `Ctrl` + `1` | На главную |
| `Esc` | Закрыть меню или контекстное меню |

### Сборка из исходников

```bash
npm install
npm run dev              # окно с горячей перезагрузкой
npm run typecheck        # проверка типов main и renderer
npm run dist:portable    # release/BeedBrowser.exe
npm run dist:installer   # release/BeedBrowser-Setup.exe
```

Требуется Node.js 20 или новее.

### Иконка

Иконкой приложения служит `icon.png` в корне проекта. Скрипт обрезает рисунок по
прозрачности и выравнивает его, после чего собираются `.ico` и PNG-размеры:

```bash
python scripts/prepare-icon.py   # build/icon-source.png
npm run icons                    # build/icon.ico и PNG-размеры
```

Для первого шага нужен Python с библиотекой Pillow.

### Что ещё не сделано

- Синхронизация — раздел есть, но данные хранятся только на устройстве.
- Подсказки поиска в адресной строке.
- Расширения.
- Закреплённые вкладки и компактный режим меню не сохраняются между запусками.

---

## English

### What it is

BeedBrowser keeps only what matters: a graphite surface, hairline borders and a
quiet interface. Anything not needed every day lives in a menu or in settings
instead of on screen.

### Features

| Area | What it does |
| --- | --- |
| Window | Frameless, background fills the whole window, square window buttons |
| Tabs | New, close, duplicate, pin, full right-click menu |
| Address bar | Search or navigate, HTTPS padlock |
| Left rail | Home, tabs, bookmarks, history, downloads, settings; collapses to icons |
| Home screen | Clock, weather, search, quick links, bookmarks, recents |
| Context menus | Text, links, images, editable fields |
| Settings | General, tabs, security, privacy, appearance, sync, documents, social, about |
| Appearance | Dark, light or system theme, three densities, page zoom |

### Screenshots

| Compact rail | Context menu |
| --- | --- |
| ![Compact rail](docs/compact.png) | ![Page context menu](docs/context-menu.png) |
| *Icons only, no labels* | *Right click on a page* |

| Light theme | Documents |
| --- | --- |
| ![Light theme](docs/light.png) | ![Privacy policy and terms](docs/documents.png) |
| *Theme and appearance settings* | *Privacy policy and user agreement* |

| Search | Downloads |
| --- | --- |
| ![Search](docs/search.png) | ![Downloads](docs/downloads.png) |
| *Opens real results* | *Download list* |

### Run

- `release/BeedBrowser.exe` — a portable build, nothing to install.
- `release/BeedBrowser-Setup.exe` — an installer that asks for the language
  (Russian or English).

### Keyboard shortcuts

| Keys | Action |
| --- | --- |
| `Ctrl` + `T` | New tab |
| `Ctrl` + `W` | Close tab |
| `Ctrl` + `L` or `Ctrl` + `K` | Focus the address bar |
| `Ctrl` + `R` | Reload the page |
| `Ctrl` + `D` | Bookmark the page |
| `Ctrl` + `,` | Settings |
| `Ctrl` + `1` | Home |
| `Esc` | Close a menu or the context menu |

### Build from source

```bash
npm install
npm run dev              # hot-reloading window
npm run typecheck        # main and renderer types
npm run dist:portable    # release/BeedBrowser.exe
npm run dist:installer   # release/BeedBrowser-Setup.exe
```

Requires Node.js 20 or newer.

### Not built yet

- Sync — the section exists, but data stays on this device.
- Address-bar search suggestions.
- Extensions.
- Pinned tabs and the compact rail are not restored between launches.

---

## Как это устроено · How it works

**URL активной вкладки — единственный источник истины** для того, что показывает
окно: адрес `beed://` рисует один из экранов BeedBrowser, любой другой адрес
показывает webview вкладки. Благодаря этому адресная строка, левое меню и область
просмотра не могут разойтись.

The **active tab's URL is the single source of truth** for what the window shows:
a `beed://` URL renders one of BeedBrowser's own screens, anything else renders the
tab's web view. That one rule keeps the address bar, the rail and the viewport from
ever disagreeing.

```
src/
  main/          Electron main process: windows, IPC, storage, beed:// protocol
  preload/       the only bridge exposed to the renderer
  renderer/      React UI
    src/views/       home, downloads, history, bookmarks, settings, tabs
    src/components/  chrome, brand mark, context menu, tab strip
    src/styles/      design tokens and chrome layout
  shared/        types and helpers used by both processes
scripts/         icon pipeline, screenshot tooling, README checks
build/           application icon, generated from icon.png
docs/            screenshots used in this file
```

Токены оформления лежат в `src/renderer/src/styles/global.css`, разметка оконной
рамки — в `src/renderer/src/styles/chrome.css`. Тема — это подмена палитры по двум
атрибутам (`data-theme` и `data-density`), поэтому переключение внешнего вида не
перерисовывает интерфейс.

Design tokens live in `src/renderer/src/styles/global.css`, the window chrome in
`src/renderer/src/styles/chrome.css`. A theme is a palette swap driven by two
attributes (`data-theme` and `data-density`), so changing the appearance never
re-renders the UI.

## Инструменты разработки · Development tooling

```bash
npm run shot -- .shots/home.png --view settings   # снимок окна 1536×1024
node scripts/render-html.mjs in.html out.png      # отрисовать HTML в PNG
node scripts/check-readme.mjs                     # проверить ссылки в README
```

`npm run shot` открывает настоящее окно в отдельном профиле (`BEED_USER_DATA`) и
закрывает его после снимка. `render-html.mjs` просто отрисовывает указанный файл и
профиль не использует.

## Лицензия · Licence

MIT. Иконка и логотип принадлежат автору проекта.

*MIT. The icon and logo belong to the project author.*
