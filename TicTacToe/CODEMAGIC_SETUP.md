# Быстрая инструкция по настройке Codemagic

## Шаг 1: Загрузи конфигурацию на GitHub

```bash
cd C:\scrips\TicTacToe
git add codemagic.yaml
git commit -m 'Add Codemagic workflow configuration'
git push
```

## Шаг 2: В Codemagic нажми "Check for configuration file"

После загрузки `codemagic.yaml`, Codemagic автоматически найдет конфигурацию.

## Шаг 3: Настрой Code Signing

### Вариант А: Автоматическая подпись (Рекомендуется для начинающих)

1. В Codemagic → **iOS code signing**
2. Выбери **"Automatic code signing"**
3. Введи свой **Apple ID** (iCloud email)
4. Создай **App-Specific Password**:
   - Зайди на https://appleid.apple.com
   - Security → App-Specific Passwords
   - Создай новый пароль для "Codemagic"
   - Скопируй сгенерированный пароль
5. Вставь пароль в Codemagic
6. Codemagic автоматически создаст сертификаты

### Вариант Б: Ручная подпись (Требуется Mac)

Если у тебя уже есть сертификаты:
1. Загрузи `.p12` сертификат
2. Загрузи provisioning profile
3. Укажи Bundle ID: `com.tictactoe.app`

## Шаг 4: Настрой email (опционально)

В `codemagic.yaml` замени:
```yaml
recipients:
  - your-email@example.com
```

На свой email для уведомлений о сборке.

## Шаг 5: Запусти сборку

1. Нажми **"Start new build"**
2. Выбери workflow: **"ios-workflow"**
3. Подожди 5-10 минут
4. Скачай IPA из раздела **Artifacts**

## Упрощенная версия (без Apple Developer аккаунта)

Если у тебя нет Apple Developer аккаунта, используй бесплатный способ:

1. Создай бесплатный Apple ID на https://appleid.apple.com
2. В Codemagic используй этот Apple ID для автоматической подписи
3. **Важно:** IPA будет работать только 7 дней, потом нужно пересобирать

## Возможные проблемы

### "No signing certificates found"
- Используй автоматическую подпись Codemagic
- Или создай сертификаты вручную (требуется Mac)

### "Bundle ID is not available"
- Измени Bundle ID в `Info.plist` на уникальный
- Например: `com.yourname.tictactoe`

### "Build failed"
- Проверь логи в разделе Build logs
- Убедись, что scheme shared (уже настроено)
- Проверь, что все файлы загружены на GitHub

## Следующий шаг

После настройки, вернись сюда и скажи результат или какие ошибки появились!
