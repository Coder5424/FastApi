# fastApi

## Установка и запуск:
### Запуск сервера:
1. `docker-compose up --build`
2. `http://localhost:8001/docs#/`

### Запуск тестов:
1. `docker-compose -f docker-compose.pytest.yml up --build`


## Реализованы следующие end-point'ы:
Работа с файломи:
- /frames/ -post - загружает изображения
- /frames/{code} - get - выводит информацию о изображении
- /frames/{code} - delete - удаляет выбраное изображение

Авторизация:
- /auth/sign-up -post - регистрация
- /auth/sign-in -post - вход в профиль
- /auth/user -get - получает данные о пользователе

## Описание приложения:
- В качестве базы данных выбрана sqlite, поскольку её достаточно для решения поставленной задачи, она достаточно легко разворачивается, в особенности в сравнении с PostgreSQL
- Реализованы юнит-тесты
- Реализована аутентификация Oauth
- Реализована контейнеризация с помощью docker-compose
