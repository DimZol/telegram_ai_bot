## Запуск
### Сборка образа
```bash
docker build -t telegram-ai-bot .
```

### Запуск контейнера
```bash
docker run -d \
  --name telegram-bot \
  -e TELEGRAM_TOKEN="telegram_токен" \
  -e AI_API_KEY="api_ключ" \
  telegram-ai-bot
```

### Проверка логов
```bash
docker logs -f telegram-bot
```

## Переменные окружения

| Переменная | Описание | По умолчанию |
|------------|----------|--------------|
| TELEGRAM_TOKEN | Токен бота Telegram | Обязательно |
| AI_API_KEY | Ключ API ИИ | Обязательно |
| AI_API_URL | URL API | https://api.openai.com/v1/chat/completions |
| MODEL | Модель ИИ | gpt-3.5-turbo |

## Команды бота
- `/start` - Начать общение
- `/help` - Показать справку