# Kittygram

### Небольшая социальная сеть, в которой можно делиться фотографиями котиков и рассказывать об их достижениях

## Технологии:
* Python
* Django
* Nginx
* Docker
* Gunicorn

## Запуск проекта:

- Скопировать репозиторий `git clone https://github.com/nesterovv89/kittygram_final.git`
- В корне проекта создать файл .env для хранения секретных данных, заполнить согласно образца .env.example
- Выполнить команду `docker compose -f docker-compose.production.yml up -d`
- Провести сбор статики и выполнить миграции:
`docker compose -f docker-compose.production.yml exec backend python manage.py migrate
docker compose -f docker-compose.production.yml exec backend python manage.py collectstatic
docker compose -f docker-compose.production.yml exec backend cp -r /app/static_backend/. /backend_static/static/`
-Проект будет доступен на сервере, который вы указали в файле .env

В данный момент проект доступен по этой [ссылк](https://kittygramnesterov.ddns.net)

Автор [Павел Нестеров](https://github.com/nesterovv89)  
