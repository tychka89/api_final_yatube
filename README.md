# api_final_yatube
api_final_yatube - API-проект для социальной сети блогеров Yatube.

Аутентифицированным пользователям разрешено изменение и удаление своих постов, неаутентифицированным доступ предоставляется только для чтения.

Проект выполнен в учебных целях. 

## Настройка и запуск проекта:

Клонировать репозиторий на локальную машину:

```
git clone git@github.com:tychka89/api_final_yatube.git
```

Перейти в репозиторий в командной строке:

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python -m venv env
```

```
source env/bin/activate
```

```
python -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python manage.py runserver
```

## Документация доступна по ссылке: 
http://127.0.0.1:8000/redoc/

## Доступные эндпоинты

Посты:

```
"/api/v1/posts/",
"/api/v1/posts/{id}/"
```

Группы:

```
"/api/v1/groups/",
"/api/v1/groups/{id}/"
```

Комментарии:

```
"/api/v1/posts/{id}/comments/",
"/api/v1/posts/{id}/comments/{id}/"
```

Подписки:

```
"/api/v1/follow/"
```

Получение токена для доступа к API:

```
"/api/v1/auth/jwt/create/"
```

## Примеры запросов

Получение списка всех постов:

```
Method: GET
Endpoint: "/api/v1/posts/"
```

Публикация поста:

```
Method: POST
Endpoint: "/api/v1/posts/"
Payload:
{
    "text": "string",
    "image": "string",
    "group": 0
}
```

Получение JWT-токена:

```
Method: POST
Endpoint: "/api/v1/auth/jwt/create/"
Payload:
{
    "username": "string",
    "password": "string"
}
```

## Стек технологий: 
- Python 3.7,
- Django 2.2.16,
- djangorestframework 3.12.4,
- djangorestframework-simplejwt 4.7.2,
- Pillow 8.3.1,
- requests 2.26.0,

## Автор:

Родикова Наталия
```
https://github.com/tychka89
```