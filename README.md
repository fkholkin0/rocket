# rocket — эталонный шаблон Obsidian-vault

Чистая **стартовая заготовка** для персональной системы управления знаниями в Obsidian.
Содержит только настройки, плагины и каркас папок — **без личного контента**. Из неё
разворачивается новый vault под конкретную задачу: клонируешь, открываешь в Obsidian,
переключаешь git-remote на свой репозиторий и наполняешь.

> Прародитель — рабочий vault `patronus`, из которого перенесена вся конфигурация
> (см. историю в [`00_setup_log.md`](00_setup_log.md)).

---

## Что внутри

```
rocket/
├── .obsidian/          ← вся конфигурация Obsidian + 22 плагина с настройками
├── content/            ← вложения (изображения, Excalidraw) — пусто
├── Daily notes/        ← ежедневные заметки — пусто
├── Archive/            ← архив — пусто
├── CLAUDE.md           ← инструкции для Claude Code при работе с vault
├── 00_setup_log.md     ← лог развёртывания: что и откуда перенесено
├── README.md           ← этот файл
└── .gitignore
```

Пустые папки удерживаются в git файлами `.gitkeep`.

## Предустановленная конфигурация (`.obsidian/`)

| Файл | Назначение |
|------|-----------|
| `app.json` | Формат ссылок, папка вложений → `content/` |
| `appearance.json` | Тема Moonstone, шрифты Noto Sans / PT Mono, акцент `#4db4cb` |
| `hotkeys.json` | Горячие клавиши: `Cmd+U` — git push, `Cmd+M` — Excalidraw, `Cmd+D` — дневник |
| `core-plugins.json` | Встроенные плагины (граф, бэклинки, canvas, дневник, шаблоны) |
| `community-plugins.json` | Список community-плагинов |
| `daily-notes.json` | Папка дневника → `Daily notes/` |
| `canvas.json`, `graph.json`, `types.json` | Настройки Canvas, графа знаний, типов свойств |

### Установленные community-плагины (22)

Синхронизация и структура: `obsidian-git`, `hide-folders`, `obsidian-icon-folder`,
`note-refactor-obsidian`, `metadata-menu`, `templater-obsidian`.

Визуализация и Canvas: `obsidian-excalidraw-plugin`, `advanced-canvas`, `enhanced-canvas`,
`canvas-minimap`, `canvas-card-bg-remover`, `optimize-canvas-connections`.

Работа с данными и текстом: `dataview`, `spreadsheets`, `table-editor-obsidian`,
`colored-tags`, `fast-text-color`, `url-into-selection`, `editor-width-slider`.

Команды и интеграции: `cmdr`, `shortcuts-extender`, `post-webhook`.

> Полное описание каждого плагина — в [`00_setup_log.md`](00_setup_log.md).

---

## Как развернуть новый vault из шаблона

1. Клонировать репозиторий в новую папку:
   ```bash
   git clone git@github.com:fkholkin0/rocket.git my-new-vault
   cd my-new-vault
   ```
2. Переключить remote на свой пустой репозиторий:
   ```bash
   git remote set-url origin git@github.com:<user>/<new-repo>.git
   ```
3. Открыть папку как vault в Obsidian — все настройки и плагины подхватятся автоматически.
4. Настроить плагин `obsidian-git` под новый remote (автосинхронизация push по `Cmd+U`).
5. Наполнять `content/`, `Daily notes/` и собственную структуру папок под задачу.

## Принципы наполнения

Заложены в [`CLAUDE.md`](CLAUDE.md):

- **1 файл = 1 концепт** — особенно в тематических папках.
- **Человеческие названия** на русском, без номеров и дефисов.
- **Самодостаточные документы** — каждый файл объясняет сам себя.
- **Связи через `[[wikilinks]]`** для навигации по графу знаний.

---

*Язык vault — русский. Шаблон рассчитан на командную работу: у каждого участника —
свой личный `CLAUDE.local.md` (в `.gitignore`).*
