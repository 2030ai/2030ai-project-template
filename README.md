# 2030ai-project-template

Шаблон проекта для разработки с ИИ-агентами: Claude Code, Codex, Cursor.

GitHub slug: `2030ai/2030ai-project-template`.

## Важно

В проектах, созданных из шаблона, заполните раздел «Описание проекта» в `AGENTS.md` — это основной контекст для агента. Для свежего репозитория — пройдите `agent_docs/setup-checklist.md` и удалите его. В самом `2030ai-project-template` checklist хранится как часть шаблона.

## Структура проекта

```text
├── AGENTS.md                 # Универсальные правила для всех агентов
├── CLAUDE.md                 # Указатель на AGENTS.md для Claude Code
├── .gitignore                # macOS/Windows/Linux, IDE, Python, Node.js, .env, temp/, logs/
├── .cursorignore             # Скрывает локальные секреты от Cursor/AI-агентов
├── .env.example              # Безопасный шаблон переменных окружения
├── .editorconfig             # Единый whitespace/EOL для всех IDE
├── .markdownlint.json        # Конфигурация markdownlint
├── .github/workflows/        # CI: markdownlint
├── .agents/skills/           # Canonical project-local skills, if needed
├── .claude/skills/           # Claude Code symlink mirrors to .agents
├── .codex/skills/            # Codex symlink mirrors to .agents
├── .cursor/skills/           # Cursor symlink mirrors to .agents
└── agent_docs/               # Проектная документация
    ├── index.md              # Навигация по документам
    ├── glossary.md           # Глоссарий проекта
    ├── architecture.md       # Архитектура и компоненты
    ├── adr/                  # Атомарный журнал значимых решений
    ├── development-history/   # Атомарный журнал итераций
    ├── setup-checklist.md    # Чек-лист инициализации (удалить после)
    ├── guides/               # Гайды (DoD, окружение, логирование, архивация)
    └── templates/            # Шаблоны документов
```

## Быстрый старт

1. Клонируйте или используйте как template репозиторий.
2. Заполните раздел «Описание проекта» в `AGENTS.md`.
3. Пройдите `agent_docs/setup-checklist.md`.
4. Ознакомьтесь с `agent_docs/index.md`.
5. Начните работу.

## Документация

- `AGENTS.md` — принципы работы агента и чек-листы.
- `agent_docs/index.md` — карта всех документов.

## Заметки

- **Project-local skills:** source of truth — `.agents/skills/<name>/SKILL.md`; platform mirrors — `.claude/skills/<name>`, `.codex/skills/<name>`, `.cursor/skills/<name>` symlinks to `../../.agents/skills/<name>`.
- **Slash commands не добавлены** — reusable agent workflows оформляются как skills, а не command-файлы.
- **CLAUDE.md — обычный stub-файл, а не symlink** — symlinks ломаются на Windows, в `git archive` и при zip-extract.
- **Windows-специфичные правила не добавлены** — проект настроен для macOS.
- **Строгие правила безопасности/тестирования не добавлены** — агенты справляются сами. Добавлены: принципы работы агента (`AGENTS.md`), логирование, атомарные журналы (`development-history/` + `adr/`), глоссарий.
