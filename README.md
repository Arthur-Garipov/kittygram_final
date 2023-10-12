[![Python](https://img.shields.io/badge/-Python-464646?style=flat-square&logo=Python)](https://www.python.org/)
[![Django](https://img.shields.io/badge/-Django-464646?style=flat-square&logo=Django)](https://www.djangoproject.com/)
[![Django REST Framework](https://img.shields.io/badge/-Django%20REST%20Framework-464646?style=flat-square&logo=Django%20REST%20Framework)](https://www.django-rest-framework.org/)
[![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-464646?style=flat-square&logo=PostgreSQL)](https://www.postgresql.org/)
[![Nginx](https://img.shields.io/badge/-NGINX-464646?style=flat-square&logo=NGINX)](https://nginx.org/ru/)
[![gunicorn](https://img.shields.io/badge/-gunicorn-464646?style=flat-square&logo=gunicorn)](https://gunicorn.org/)
[![docker](https://img.shields.io/badge/-Docker-464646?style=flat-square&logo=docker)](https://www.docker.com/)
[![GitHub%20Actions](https://img.shields.io/badge/-GitHub%20Actions-464646?style=flat-square&logo=GitHub%20actions)](https://github.com/features/actions)
[![Yandex.Cloud](https://img.shields.io/badge/-Yandex.Cloud-464646?style=flat-square&logo=Yandex.Cloud)](https://cloud.yandex.ru/)

# Проект Kittygram
Проект Kittygram позволяет Вам публиковать и просматривать котов. Вы можете опубликовать вашего домашнего любимца и дать небольшую информацию о нём, например, его цвет, достижения.

# Технологии
В проекте применяются:
- **Python**
- **Django REST Framework**
- **Djoser**
- **PostgreSQL**
- **Docker**
- **Gunicorn**
- **Nginx**
- **Git**
- **GitHub Actions**

Аутентификация пользователей реализована с помощью **токена**.

# Базовые модели проекта
### *Более подробно с базовыми моделями можно ознакомиться в спецификации API.*

- **User**: пользователи.
- **Cats**: кот.
- **Achievments**: достижения.

# Запуск стека приложений с помощью docker-compose
Склонируйте репозиторий.

В корневой директории создайте файл `.env` с переменными окружения для работы с базой данных. Пример заполнения Вы можете найти в файле `.env.example`

Выполните команду `docker-compose up -d --build` для запуска сервера разработки.

Выполните миграции: `docker-compose exec backend python manage.py migrate`.

Создайте суперпользователя:

`docker-compose exec backend python manage.py createsuperuser`

Выполните _collectstatic_:

`docker-compose exec backend python manage.py collectstatic`.

Проект запущен и доступен по адресу [localhost](http://127.0.0.1/).


# OpenAPI
Документация API реализована с помощью ReDoc. Доступна по адресу [localhost/api/docs/](http://127.0.0.1/api/docs/).

# CI/CD
Для проекта Foodgram настроен _workflow_ со следующими инструкциями:
- автоматический запуск тестов (flake8)
- обновление образов на DockerHub
- автоматический деплой на боевой сервер при пуше в главную ветку master

# Подробности проекта
- Вы можете зарегестрироваться самостоятельно для проверки функционала, либо же использовать одну из учётных записей:

```
e-mail: vasya12@ya.ru
password: rfrltkfent,z123
username: Vasya_Pup
```
