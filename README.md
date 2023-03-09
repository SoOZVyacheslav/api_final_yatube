# api yatube

## Описание

API для Yatub представляет собой проект социальной сети в которой реализованы следующие возможности, 
публиковать записи, комментировать записи, а так же подписываться или отписываться от авторов.

## Стек технологий

* Python 3.9,
* Django 4.2,
* DRF,
* JWT + Djoser

## Запуск проекта в dev-режиме

- Клонировать репозиторий и перейти в него в командной строке.

```bash
git clone git@github.com:SoOZVyacheslav/api_final_yatube.git
```
- Установите и активируйте виртуальное окружение c учетом версии Python 3.9 (выбираем python не ниже 3.9):

```bash
python -m venv venv
```

```bash
source venv/Scripts/activate
```

```bash
python -m pip install --upgrade pip
```

- Затем нужно установить все зависимости из файла requirements.txt

```bash
cd yatube_api
```

```bash
pip install -r requirements.txt
```

- Выполняем миграции:

```bash
python manage.py migrate
```

- Создаем суперпользователя:

```bash
python manage.py createsuperuser
```

- Запускаем проект:

```bash
python manage.py runserver
```

## Примеры работы с API

Для неавторизованных пользователей работа с API доступна в режиме чтения, что-либо изменить или создать не получится.

```r
GET api/v1/posts/ - получить список всех публикаций.
При указании параметров limit и offset выдача должна работать с пагинацией
GET api/v1/posts/{id}/ - получение публикации по id
GET api/v1/groups/ - получение списка доступных сообществ
GET api/v1/groups/{id}/ - получение информации о сообществе по id
GET api/v1/{post_id}/comments/ - получение всех комментариев к публикации
GET api/v1/{post_id}/comments/{id}/ - Получение комментария к публикации по id
```
#### Остальные примеры API есть в документация по адресу http://localhost:8000/redoc/


