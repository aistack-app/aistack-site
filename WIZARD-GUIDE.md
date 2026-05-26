# Пошаговая инструкция по Hermes Setup Wizard

После того как setup.sh дойдёт до Stage 3 (Install Hermes), запустится Hermes Agent Setup Wizard. Он задаст ~6 вопросов. Действуйте так:

## Вопрос 1: "Would you like to see what can be imported?"
**Ответ:** `Y` + Enter

## Вопрос 2: "How would you like to set up Hermes?"
- 1. Quick setup (recommended)
- 2. Full setup

**Ответ:** `1` + Enter

## Вопрос 3: AI Provider Selection (41 опция)
Список большой, нужно ввести номер провайдера. Если вы выбрали в визарде:
- **Anthropic** → введите `1` + Enter
- **OpenAI** → введите `2` + Enter
- **ProxyAPI** → введите `14` + Enter (примерно — посмотрите на экране)
- Если не знаете → `38. custom` → введите свой URL

## Вопрос 4: Terminal backend (8 опций)
**Ответ:** `8` + Enter (Keep current — local)

## Вопрос 5: Connect a messaging platform?
- 1. Set up messaging now
- 2. Skip — set up later

**Ответ:** `2` + Enter (мы настроим ботов отдельно через openclaw, не через Hermes wizard)

## Если что-то пошло не так
- Wizard завис → нажмите Enter ещё раз.
- Ctrl+C не выходит → откройте новый Terminal, выполните `docker kill <container_name>` (для Docker) или `pkill -f hermes` (на сервере).
- После завершения wizard'а скрипт продолжит автоматически.
