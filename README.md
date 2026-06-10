# AI Automation Suggester (форк с поддержкой Cloud.ru)

Это форк [AI Automation Suggester](https://github.com/ITSpecialist111/ai_automation_suggester) — интеграции для Home Assistant, которая использует большие языковые модели для анализа вашего умного дома и предлагает готовые автоматизации в формате YAML.

**Что добавлено в этом форке:**
- Поддержка моделей из [Cloud.ru Foundation Models](https://cloud.ru/marketplace/ai-ml) (Qwen, GPT-OSS и другие).
- Ответы на русском языке по умолчанию.
- Настройка Project ID и API-ключа Cloud.ru через интерфейс Home Assistant.
- Модель по умолчанию: `Qwen/Qwen3-Coder-Next`.

## Подробности

О том, зачем это нужно и как работает, я рассказал в [этом посте в блоге](https://mansmarthome.info/mini/ii-assistient-kak-nieirosiet-sama-priedlaghaiet-avtomatizatsii-na-osnovie-vashikh-dannykh/).

## Установка

### Через HACS (рекомендуется)

1. Убедитесь, что у вас установлен [HACS](https://hacs.xyz/)
2. Используйте [ссылку на My Home Assistant](https://my.home-assistant.io/redirect/hacs_repository/?owner=black-roland&repository=ai_automation_suggester&category=integration) или вручную добавьте этот репозиторий как пользовательский:
   - HACS → Интеграции → три точки (⋮) → `Пользовательские репозитории`
   - URL: `https://github.com/black-roland/ai_automation_suggester`
   - Категория: `Интеграция`
3. Нажмите `Добавить`
4. Найдите `AI Automation Suggester` в списке и установите
5. Перезапустите Home Assistant
6. После перезапуска: Настройки → Устройства и службы → + Добавить интеграцию → найдите `AI Automation Suggester`

### Вручную

Скопируйте папку `custom_components/ai_automation_suggester` в директорию `custom_components` вашей конфигурации Home Assistant и перезапустите Home Assistant.

## Настройка Cloud.ru

При добавлении интеграции выберите провайдера **Cloud.ru** и укажите:
- **Project ID** — идентификатор проекта в Cloud.ru
- **API Key** — ключ API для доступа к моделям
- **Модель** (опционально) — можно изменить на любую доступную в Cloud.ru

Все остальные параметры (температура, лимиты токенов) настраиваются так же, как и для других провайдеров.

## Оригинальный проект

Огромное спасибо [ITSpecialist111](https://github.com/ITSpecialist111) за создание этой замечательной интеграции.
Оригинальный репозиторий: [ai_automation_suggester](https://github.com/ITSpecialist111/ai_automation_suggester)
