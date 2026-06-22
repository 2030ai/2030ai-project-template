# [2026-06-22 12:37] Skill command-name rule

Файл: `agent_docs/development-history/2026-06-22-1237-skill-command-name-rule.md`

## Что сделано

- В `AGENTS.md` добавлено правило для project-local skills: `name`, description, H1 и `agents/openai.yaml display_name` должны совпадать со slash-командой.

## Зачем

Чтобы новые проекты из шаблона не создавали две сущности для одного skill: отдельное название и отдельную команду.

## Обновлено

- [ ] agent_docs/architecture.md (не применимо)
- [ ] agent_docs/adr/YYYY-MM-DD-HHMM-title.md (не применимо)
- [ ] Тесты (не применимо, docs-only)
- [x] Документация

## Связанные решения

- Не применимо.

## Следующие шаги

- Применять правило в template/upstream skill репозиториях.
