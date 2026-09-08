# ReqRes API Testing — портфолио-проект для Manual QA

Этот проект демонстрирует навыки ручного тестирования REST API на примере публичного тестового сервиса [ReqRes](https://reqres.in).

## Цель проекта

Показать умение:

- работать с REST API (методы `GET`, `POST`, `PUT`, `PATCH`, `DELETE`);
- писать тест-кейсы и чек-листы;
- анализировать статус-коды, заголовки и тело ответа;
- оформлять результаты тестирования.

## Инструменты

- [Postman](https://www.postman.com/downloads/) — отправка запросов, Collection Runner;
- [ReqRes API](https://reqres.in) — публичный тестовый REST API.

## Структура проекта

```text
portfolioQA/
├── ReqRes API Practice/
    ├── README.md
    ├── Test-cases.md # Таблица с тест-кейсами
    ├── Export from Postman/
    │   └── ReqRes API Practice.postman_collection.json # Экспортированная коллекция Postman
    └── Screenshots/
        ├── TC-01 List of users.png
        ├── TC-02 Retrieving a specific user.png
        ├── TC-03 Create a user.png
        ├── TC-04 Complete user update.png
        ├── TC-05 Partial user update.png
        ├── TC-06 Login with valid data.png
        ├── TC-07 Login with an empty password (negative).png
        ├── TC-08 User deletion.png
        └── Collection runner report.png
```

## Что протестировано

### Основные сценарии

| № | Сценарий | Метод | Эндпоинт | Ожидаемый статус |
| --- | --- | --- | --- | --- |
| 1 | Получение списка пользователей | `GET` | `/api/users?page=1` | `200` |
| 2 | Получение конкретного пользователя | `GET` | `/api/users/2` | `200` |
| 3 | Создание нового пользователя | `POST` | `/api/users` | `201` |
| 4 | Полное обновление пользователя | `PUT` | `/api/users/2` | `200` |
| 5 | Частичное обновление пользователя | `PATCH` | `/api/users/2` | `200` |
| 6 | Логин с валидными данными | `POST` | `/api/login` | `200` |
| 7 | Логин с неверным паролем | `POST` | `/api/login` | `400` |
| 8 | Удаление пользователя | `DELETE` | `/api/users/2` | `204` |

## Проверки для каждого запроса

1. Статус-код соответствует ожидаемому (`200`, `201`, `204`, `400`).
2. Структура JSON-ответа соответствует документации.
3. Наличие обязательных полей (`id`, `email`, `name`, `token`, `error` и др.).
4. Типы данных верные (числа, строки, массивы, объекты).
5. Время ответа в пределах нормы (менее 500 мс).
6. Заголовок `Content-Type: application/json`.

## Как запустить тесты

### Вариант 1: Postman

1. Импортируй коллекцию в Postman:
        Открой Postman → **Import** → выбери файл `ReqRes API Practice.postman_collection.json`.
2. Коллекция **ReqRes API Practice** появится в списке.
3. Открой любой запрос и нажми **Send** — запрос отправится.
4. Чтобы запустить все тесты сразу:
        Выбери коллекцию → нажми **Run** → **Run collection** → **Run ReqRes API Practice**.

## Тест-кейсы

Полная таблица с тест-кейсами (ID, шаги, ожидаемый результат) доступна в отдельном файле `Test-cases.md` по ссылке:  
<https://clck.ru/3VhiDW>

## Скриншоты

В папке `Screenshots/` находятся скриншоты:

1. Примеры запросов и ответов в Postman.
2. Отчёт Collection Runner после запуска всей коллекции.

## Навыки, продемонстрированные в проекте

1. **REST API**: понимание методов `GET`, `POST`, `PUT`, `PATCH`, `DELETE` и их семантики.
2. **Статус-коды HTTP**: `200`, `201`, `204`, `400`.
3. **Postman**: создание коллекций, Collection Runner.
4. **Тест-дизайн**: написание тест-кейсов, проверка позитивных и негативных сценариев.
5. **Анализ ответов**: проверка структуры JSON, типов данных, обязательных полей.
6. **Документирование**: оформление результатов в виде README, таблиц, скриншотов.

## Требования к окружению

1. Postman (версия 12.26.3 или новее) — скачать: <https://www.postman.com/downloads/>

## Полезные ссылки

1. Документация ReqRes API: <https://reqres.in>
2. Документация Postman: <https://learning.postman.com>
3. Шпаргалка по HTTP-методам: <https://habr.com/ru/articles/1010240/>

## Контакты

1. Email: kraulerr@yandex.ru
2. Telegram: [@kraulerr](https://t.me/kraulerr)

> **Примечание:** Этот проект создан в учебных целях для демонстрации навыков ручного тестирования API. ReqRes API — публичный сервис, предназначенный для практики тестирования.
