# Лог развёртывания vault rocket

**Дата:** 2026-03-05
**Источник:** vault `patronus`
**Репозиторий:** git@github.com:fkholkin0/rocket.git

---

## Итерация 1 — Инициализация проекта

### Что сделано

#### 1. Git-репозиторий
- Создана директория `/Users/admin/Projects/rocket`
- Выполнен `git init`
- Установлен remote origin: `git@github.com:fkholkin0/rocket.git`
- Переименована ветка в `main`

#### 2. Перенос Obsidian-конфигурации (`.obsidian/`)
Скопирована вся `.obsidian/` директория из vault `patronus`:

**Конфигурационные файлы:**
| Файл | Назначение |
|------|-----------|
| `app.json` | Основные настройки Obsidian (формат ссылок, вложения → `content/`) |
| `appearance.json` | Тема: Moonstone, шрифты: Noto Sans / PT Mono, акцент: `#4db4cb` |
| `hotkeys.json` | Горячие клавиши (Cmd+U — git push, Cmd+M — Excalidraw, Cmd+D — дневник) |
| `core-plugins.json` | Встроенные плагины (граф, бэклинки, canvas, дневник, шаблоны...) |
| `community-plugins.json` | Список установленных community-плагинов |
| `daily-notes.json` | Папка дневника: `Daily notes/` |
| `canvas.json` | Настройки Canvas |
| `graph.json` | Настройки графа знаний |
| `types.json` | Типы свойств |

**Установленные плагины (22 шт.):**

| Плагин | Описание |
|--------|---------|
| `obsidian-git` | Автосинхронизация vault через git |
| `obsidian-excalidraw-plugin` | Рисование схем и диаграмм |
| `dataview` | SQL-подобные запросы по заметкам |
| `spreadsheets` | Таблицы внутри Obsidian |
| `colored-tags` | Цветные теги |
| `cmdr` | Кастомные команды в интерфейсе |
| `hide-folders` | Скрытие папок в файловом дереве |
| `note-refactor-obsidian` | Разбивка и рефакторинг заметок |
| `post-webhook` | Отправка данных через webhook |
| `templater-obsidian` | Шаблоны с логикой (js) |
| `shortcuts-extender` | Расширение горячих клавиш |
| `advanced-canvas` | Расширенный Canvas |
| `table-editor-obsidian` | Удобное редактирование таблиц |
| `metadata-menu` | Меню для frontmatter-метаданных |
| `url-into-selection` | Вставка URL в выделенный текст |
| `obsidian-icon-folder` | Иконки для папок |
| `canvas-card-bg-remover` | Убирает фон карточек Canvas |
| `canvas-minimap` | Мини-карта Canvas |
| `editor-width-slider` | Управление шириной редактора |
| `fast-text-color` | Быстрая окраска текста (Alt+T) |
| `optimize-canvas-connections` | Оптимизация соединений Canvas |
| `enhanced-canvas` | Дополнительные функции Canvas |

#### 3. Перенос технических файлов из `patronus`
- `CLAUDE.md` — инструкции для Claude Code при работе с vault

#### 4. Создана базовая структура папок
```
rocket/
├── .obsidian/          ← конфиги + все плагины с настройками
├── content/            ← вложения (изображения, excalidraw)
├── Daily notes/        ← ежедневные заметки
├── Archive/            ← архив
├── CLAUDE.md           ← инструкции для Claude Code
└── 00_setup_log.md     ← этот файл
```

---

## Следующие шаги

- [ ] Первый коммит и push на GitHub
- [ ] Настроить `obsidian-git` под новый репозиторий
- [ ] Наполнить структуру под задачи проекта rocket
