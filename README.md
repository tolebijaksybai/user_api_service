# User api

```
curl --location 'localhost:9201/api/v1/users'
```

* Для старта с использованием **Docker** необходимо:
* Установить Docker
* Создать образ

```
docker build . --tag=user-api:latest
```

* Запустить контейнер

```
docker run -d -p 9201:9200 user-api:latest
```

<br/>Отправить запрос:

```
curl --location 'localhost:9201/api/v1/users'
```

* Пример ответа:

```
[
  {
    "id": 1,
    "firstName": "John",
    "lastName": "Doe",
    "email": "john.doe@mail.com"
  },
  {
    "id": 2,
    "firstName": "Mike",
    "lastName": "Smith",
    "email": "mike.smith@mail.com"
  }
 ]
```