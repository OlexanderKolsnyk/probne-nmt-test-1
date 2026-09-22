# Пробне НМТ — тест 1

Партнерський тестовий стенд. Публічні файли містять завдання, але не містять ключів правильних відповідей.

## Структура

- `index.html` — розмітка;
- `assets/styles.css` — стилі;
- `assets/app.js` — логіка тесту;
- `assets/exam-data.js` — публічний контент завдань без правильних ключів;
- `formuli.pdf` — довідкові матеріали.

## Підключення Google Sheets

1. Створіть Google-таблицю **Пробне НМТ — тест 1**.
2. Відкрийте **Розширення → Apps Script**.
3. Вставте приватний серверний код Apps Script і запустіть функцію `setup`.
4. Розгорніть як Web app: виконувати від вашого імені, доступ — anyone.
5. Вставте URL розгортання в `CONFIG.SHEETS_ENDPOINT` у `assets/app.js`.
6. Запустіть `setupDailyBackup`, щоб створити першу копію таблиці та щоденний backup-trigger.

Таблиця матиме аркуші: `Registrations`, `Attempts`, `Answers`.

Перед публікацією:

```powershell
node work\validate_exam_integrity.js
node work\test_resilience_round.js
```

Серверний код із ключами відповідей навмисно не публікується в репозиторії.
