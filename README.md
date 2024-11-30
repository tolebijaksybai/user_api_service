# User api

```
curl --location 'localhost:8080/api/v1/users'
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

* Для старта с использованием **Docker** необходимо:
* Установить Docker
* Создать образ

```
docker build . --tag=user-api:latest
```

* Запустить контейнер

```
docker run -p 9200:9200 user-api:latest
```

<br/>Отправить запрос:

```
curl --location 'localhost:9200/api/v1/users'
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