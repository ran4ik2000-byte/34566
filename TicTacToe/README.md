# Крестики-Нолики iOS 🎮

<div align="center">
  <h3>Красивое iOS приложение с игрой в крестики-нолики</h3>
  <p>SwiftUI • Gradient Design • Smooth Animations</p>
</div>

---

## 🎨 Особенности

- ✨ Современный градиентный дизайн
- 🎭 Плавные анимации и переходы
- 🎯 Интуитивный интерфейс
- 🏆 Автоматическое определение победителя
- 🔄 Быстрая перезагрузка игры
- 📱 Поддержка iPhone и iPad

## 🚀 Быстрая установка IPA

### Способ 1: Codemagic (Рекомендуется)

1. **Регистрация:**
   - Зайди на [codemagic.io](https://codemagic.io)
   - Зарегистрируйся через GitHub
   - 500 минут сборки бесплатно каждый месяц

2. **Добавление приложения:**
   - Нажми **"Add application"**
   - Выбери **"Add from custom source"** или подключи GitHub
   - Укажи репозиторий: `https://github.com/YOUR_USERNAME/TicTacToe`

3. **Настройка проекта:**
   - Codemagic автоматически найдет `codemagic.yaml`
   - Выбери workflow: **"ios-workflow"**
   - Или выбери **"iOS App"** при ручной настройке

4. **Code Signing (Подпись кода):**
   
   **Вариант A: Автоматическая подпись Codemagic (проще всего)**
   - В настройках проекта → Code signing
   - Выбери **"Codemagic code signing"**
   - Введи свой Apple ID и пароль приложения
   - Codemagic сам создаст сертификаты
   
   **Вариант B: Свои сертификаты**
   - Загрузи свой .p12 сертификат
   - Загрузи provisioning profile
   - Укажи Bundle ID: `com.tictactoe.app`

5. **Запуск сборки:**
   - Нажми **"Start new build"**
   - Подожди 5-10 минут
   - Скачай IPA из раздела **Artifacts**

### Способ 2: GitHub Actions

Проект уже настроен для автоматической сборки через GitHub Actions.

**Требования:**
- Аккаунт Apple Developer (бесплатный или $99/год)
- Сертификаты разработчика (требуется Mac для создания)

**Инструкция:** См. файл [SETUP_GUIDE.md](SETUP_GUIDE.md)

### Способ 3: Bitrise

1. Зайди на [bitrise.io](https://bitrise.io)
2. Добавь GitHub репозиторий
3. Выбери **iOS** workflow
4. Настрой code signing
5. Запусти сборку

## 📱 Установка IPA на iPhone

### AltStore (Windows/Mac) 

**Лучший вариант для Windows!**

1. Скачай [AltStore](https://altstore.io/)
2. Установи AltStore на свой ПК
3. Установи AltStore на iPhone через Mail-плагин
4. Перетащи IPA файл в AltStore на iPhone

**Важно:**
- IPA работает 7 дней с бесплатным Apple ID
- Нужно обновлять каждую неделю через AltStore

### Sideloadly (Windows/Mac)

1. Скачай [Sideloadly](https://sideloadly.io/)
2. Подключи iPhone к ПК через USB
3. Открой Sideloadly
4. Перетащи IPA файл
5. Введи свой Apple ID
6. Нажми **Start**

### Apple Configurator (только Mac)

1. Установи Apple Configurator из App Store
2. Подключи iPhone через USB
3. Добавь устройство
4. Перетащи IPA файл на устройство

## 🎯 Как играть

1. Игроки ходят по очереди (крестики и нолики)
2. Первый игрок - крестики (✕), второй - нолики (◯)
3. Цель: выстроить три символа в ряд (горизонталь, вертикаль, диагональ)
4. Победная линия подсвечивается желтым
5. Кнопка **"Новая игра"** перезапускает игру

## 📁 Структура проекта

```
TicTacToe/
├── TicTacToeApp.swift                 # Точка входа
├── ContentView.swift                  # UI компоненты
├── GameViewModel.swift                # Игровая логика
├── Info.plist                         # Конфигурация
├── TicTacToe.xcodeproj/              # Xcode проект
│   └── xcshareddata/
│       └── xcschemes/
│           └── TicTacToe.xcscheme    # Shared scheme
├── codemagic.yaml                     # Конфигурация Codemagic
├── .github/workflows/                 # GitHub Actions
│   ├── build-ipa.yml                 # Основная сборка
│   └── build-ipa-unsigned.yml        # Тестовая сборка
└── SETUP_GUIDE.md                     # Подробная инструкция
```

## 🎨 Дизайн

- **Фон:** Градиент #667eea → #764ba2
- **Крестики:** Красный #ff6b6b
- **Нолики:** Бирюзовый #4ecdc4
- **Эффекты:** Glassmorphism, тени, анимации
- **Шрифт:** SF Rounded

## 🔧 Технологический стек

- **SwiftUI** - Декларативный UI
- **Combine** - Реактивность
- **MVVM** - Архитектурный паттерн
- **GitHub Actions / Codemagic** - CI/CD

## ⚙️ Требования для разработки

- macOS 13.0+
- Xcode 15.0+
- iOS 15.0+ SDK
- Swift 5.9+

## 🏗️ Локальная разработка (требуется Mac)

```bash
# Клонируй репозиторий
git clone https://github.com/YOUR_USERNAME/TicTacToe.git
cd TicTacToe

# Открой в Xcode
open TicTacToe.xcodeproj

# Или собери через терминал
xcodebuild -project TicTacToe.xcodeproj \
  -scheme TicTacToe \
  -sdk iphonesimulator \
  -destination 'platform=iOS Simulator,name=iPhone 15' \
  build
```

## ⚠️ Важная информация

### Бесплатный Apple Developer аккаунт:
- ✅ Бесплатно
- ⏰ IPA работает 7 дней
- 🔄 Нужно переустанавливать еженедельно
- 📱 Максимум 3 приложения одновременно
- 🔐 Только на зарегистрированных устройствах (UDID)

### Платная подписка Apple Developer ($99/год):
- ✅ IPA работает 1 год
- 🚀 Публикация в App Store
- 🧪 TestFlight для бета-тестирования
- 📱 До 100 устройств для Ad Hoc distribution
- 📊 App Analytics

## 🐛 Решение проблем

### "Untrusted Developer" на iPhone
1. Открой **Settings** → **General** → **VPN & Device Management**
2. Найди свой профиль разработчика
3. Нажми **"Trust [Your Name]"**

### Codemagic не находит проект
- ✅ Убедись, что `codemagic.yaml` в корне репозитория
- ✅ Проверь, что scheme shared (в папке `xcshareddata`)
- ✅ Попробуй "Detect project type" в настройках

### GitHub Actions не запускается
- Проверь все secrets в Settings → Secrets
- Убедись, что сертификаты в base64
- Проверь Bundle ID совпадает везде

### IPA не устанавливается
- Убедись, что UDID твоего iPhone добавлен в Provisioning Profile
- Проверь, что сертификат не истек
- Используй метод экспорта "ad-hoc" или "development"

## 📚 Полезные ссылки

- [Подробная инструкция по настройке](SETUP_GUIDE.md)
- [Apple Developer Portal](https://developer.apple.com/)
- [SwiftUI Documentation](https://developer.apple.com/documentation/swiftui)
- [Codemagic iOS Guide](https://docs.codemagic.io/yaml-quick-start/building-a-native-ios-app/)
- [AltStore FAQ](https://altstore.io/faq/)

## 🤝 Нужна помощь?

Если что-то не получается:
1. Проверь раздел "Решение проблем" выше
2. Прочитай [SETUP_GUIDE.md](SETUP_GUIDE.md)
3. Создай Issue в репозитории

## 📄 Лицензия

Проект создан в образовательных целях. Свободно используй и модифицируй!

---

<div align="center">
  <p>Сделано с ❤️ на SwiftUI</p>
</div>
