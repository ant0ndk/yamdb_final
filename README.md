[![Django-app workflow](https://github.com/DeffronMax/yamdb_final/actions/workflows/main.yml/badge.svg)](https://github.com/ant0ndk/yamdb_final/actions/workflows/main.yml)

## _Учебный проект 13 спринта факультета Python-разработчик Яндекс.Практикум_

## Стек
 - Python
 - Django
 - Docker
 - Nginx

## Запуск проекта

Клонировать репозиторий:
```sh
git clone https://github.com/ant0ndk/infra_sp2.git
```
Создать вируальное окружение
```sh
python3 -m venv venv
source venv/bin/activate
```

Установить зависимости:
```sh
pip install -r requirements.txt
```

Перейти в папку _infra_ и сделать билд docker'a:
```sh
docker-compose up -d --build
```

Миграции:
```sh
docker-compose exec web python manage.py migrate
```

Создание суперпользователя
```sh
docker-compose exec web python manage.py createsuperuser
```

Сборка статики:
```sh
docker-compose exec web python manage.py collectstatic --no-input
```

Остановить приложение в контейнере
```sh
docker-compose down -v
```
## Подробную документацию по проекту можно посмотреть по адресу:
```sh
<адрес_сервера:порт/домен>/redoc/
```
