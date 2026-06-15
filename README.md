# ТеКтоРядом — прототип

Маркетплейс для поиска проверенных сиделок и медсестёр рядом с пользователем.
Кликабельный прототип MVP: 6 экранов, стиль Soft Glassmorphism.

> ⚠️ Это демонстрационный прототип с моковыми данными (без бэкенда). Подходит для
> показа инвесторам и закрытого тестирования, **не** для публичной публикации в сторах.

## Структура

```
prototype/
├─ www/
│  └─ index.html          # само приложение (HTML/CSS/JS, без сборки)
├─ capacitor.config.json  # конфиг нативной обёртки (Capacitor)
├─ package.json
└─ README.md
```

## Веб-версия (Vercel)

Приложение статическое — деплоится как есть.
В настройках проекта Vercel укажите **Root Directory = `www`**.

Локальный просмотр:

```bash
npx serve www      # или любой статический сервер
```

## Android-сборка (APK для демо)

Требуется установленный **Android Studio** (включает SDK + JDK + Gradle).

```bash
npm install
npx cap add android      # один раз: создаёт папку android/
npx cap sync             # после любых правок в www/
npx cap open android     # откроет Android Studio
```

В Android Studio: **Build → Build Bundle(s)/APK(s) → Build APK(s)**.
Готовый `app-debug.apk` отправьте инвестору — установится как обычное приложение.

## iOS

Нативная сборка iOS требует Mac + аккаунт Apple Developer ($99/год).
Пока для iPhone используйте PWA-ярлык: открыть веб-ссылку в Safari →
«Поделиться» → «На экран “Домой”».
