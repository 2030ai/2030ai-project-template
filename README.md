# 2030AI Project Template

Шаблон проекта для разработки с ИИ-агентами: Claude Code, Codex, Cursor.

## Важно

Перед началом работы заполните раздел «Описание проекта» в `AGENTS.md` — это основной контекст для агента. Для свежего репозитория — пройдите `agent_docs/setup-checklist.md` и удалите его.

## Структура проекта

```text
├── AGENTS.md                 # Универсальные правила для всех агентов
├── CLAUDE.md                 # Указатель на AGENTS.md для Claude Code
├── .gitignore                # macOS/Windows/Linux, IDE, Python, Node.js, .env, temp/, logs/
├── .editorconfig             # Единый whitespace/EOL для всех IDE
├── .markdownlint.json        # Конфигурация markdownlint
├── .github/workflows/        # CI: markdownlint
└── agent_docs/               # Проектная документация
    ├── index.md              # Навигация по документам
    ├── glossary.md           # Глоссарий проекта
    ├── architecture.md       # Архитектура и компоненты
    ├── adr/                  # Журнал значимых решений (по файлу на решение)
    ├── development-history.md # История разработки
    ├── setup-checklist.md    # Чек-лист инициализации (удалить после)
    ├── guides/               # Гайды (DoD, окружение, логирование, архивация)
    └── templates/            # Шаблоны документов
```

## Быстрый старт

1. Клонируйте или используйте как template репозиторий.
2. Пройдите `agent_docs/setup-checklist.md`.
3. Заполните раздел «Описание проекта» в `AGENTS.md`.
4. Ознакомьтесь с `agent_docs/index.md`.
5. Начните работу.

## Документация

- `AGENTS.md` — принципы работы агента и чек-листы.
- `agent_docs/index.md` — карта всех документов.

## Заметки

- **Symlinks для Cursor/CLINE/Windsurf не добавлены** — школа рекомендует Claude Code, остальные инструменты подтягивают `AGENTS.md` автоматически.
- **CLAUDE.md — обычный stub-файл, а не symlink** — symlinks ломаются на Windows, в `git archive` и при zip-extract.
- **Windows-специфичные правила не добавлены** — проект настроен для macOS.
- **Строгие правила безопасности/тестирования не добавлены** — агенты справляются сами. Добавлены: принципы работы агента (`AGENTS.md`), логирование, двухуровневая история (`development-history.md` + `adr/`), глоссарий.
