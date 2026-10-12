# 🎮 Следующий шаг: Загрузка на GitHub

## 1. Создай репозиторий на GitHub

1. Зайди на https://github.com
2. Нажми **"New repository"** (зеленая кнопка)
3. Название: `TicTacToe` (или любое другое)
4. Описание: `iOS Tic-Tac-Toe game with beautiful gradient design`
5. Выбери **Public** (чтобы Codemagic мог получить доступ)
6. **НЕ** добавляй README, .gitignore или license (они уже есть)
7. Нажми **"Create repository"**

## 2. Загрузи код на GitHub

После создания репозитория GitHub покажет команды. Используй эти:

```bash
# В PowerShell выполни:
cd C:\scrips\TicTacToe

# Добавь удаленный репозиторий (замени YOUR_USERNAME на свое имя)
git remote add origin https://github.com/YOUR_USERNAME/TicTacToe.git

# Загрузи код
git push -u origin main
```

### Полная команда для PowerShell:

```powershell
$env:Path = [System.Environment]::GetEnvironmentVariable("Path","Machine") + ";" + [System.Environment]::GetEnvironmentVariable("Path","User")
cd C:\scrips\TicTacToe

# Замени YOUR_USERNAME на свое имя на GitHub!
& "C:\Program Files\Git\bin\git.exe" remote add origin https://github.com/YOUR_USERNAME/TicTacToe.git
& "C:\Program Files\Git\bin\git.exe" push -u origin main
```

При запросе введи:
- **Username:** твое имя на GitHub
- **Password:** используй **Personal Access Token** (не обычный пароль)

## 3. Как создать Personal Access Token

Если GitHub попросит пароль:

1. Зайди на https://github.com/settings/tokens
2. Нажми **"Generate new token"** → **"Generate new token (classic)"**
3. Название: `Codemagic TicTacToe`
4. Выбери срок действия: `90 days`
5. Отметь галочку: `repo` (Full control of private repositories)
6. Нажми **"Generate token"**
7. **СКОПИРУЙ ТОКЕН** (он больше не покажется!)
8. Используй этот токен вместо пароля

## 4. После успешной загрузки

Вернись в Codemagic и:

1. Нажми **"Check for configuration file"** (в правом верхнем углу)
2. Codemagic найдет `codemagic.yaml`
3. Увидишь workflow: **"ios-workflow"**
4. Настрой Code Signing (автоматическую подпись с Apple ID)
5. Запусти сборку!

## Нужна помощь?

Напиши свое имя пользователя на GitHub, и я дам точные команды для загрузки!

---

**Статус:** ✅ Локальный репозиторий готов
**Следующий шаг:** Создать репозиторий на GitHub и загрузить код
