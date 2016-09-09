## **Тестовое задание для тестировщика**
Тестовый сервер реализует REST API для пользователей.

Тестовые данные лежат в db.json
В данный момент в базе лежит 10 пользователей вида:

##объект пользователя с требованиями к полям
```javascript
{
    "id": 1, //обязательное поле, int
    "username": "MCummings", //обязательное поле, max 512 символов
    "email": "MSpencer@fringilla.ly", //обязательное поле, email
    "password": "8tsNhWDf", //обязательное поле, минимум 6 символов, буква и цифра 
    "company": "Steward Computing" //необязательное поле, 512 символов max
}
```

пользователи доступны по /users

Необходимо проверить реализацию основных операций (создание, добавление, удаление, редактировние пользователей)

Пункты задания

1. Установить тестовый сервер на локальной машине, используя git (читай README.md)

2. Используя какой-либо фреймворк, Написать функциональные тесты, которые будут проверять работу основных операций для пользователей.

     + получение пользовтелей : GET /users
     + получение пользователя по id: GET /users/:id
     + получение пользователя по параметру: GET /users?username=putin
     + удаление пользователя: DELETE /users/:id
     + создание пользователя: POST /users
     + редактирование пользователя: PATCH /users/:id

    Тестов достаточно по одному позитивному и одному негативному сценарию, на создание проверка нескольких границных условий, больше не надо.

3. Дописать инстукцию по запуску тестов в README.md
4. Залить тесты и инструкцию в удаленный репозитарий

/========================================================/

# **Тестовый сервер:** Инструкция по установке

##Установка nodejs
Установить на машину nodejs последней стабильной версии, воспользовавшись гуглом.

##Сборка
Тестовый  сервер реализует REST API.
Реализован с помощью https://github.com/typicode/json-server.

Установить модули, прописанные в package.json
```bash
npm install
```
##Запуск тестового сервера
Запускаем сервер на порту 8001, тестовые данные лежат в db.json
```bash
json-server --watch db.json --port 8001
```

##Тестируем!!!