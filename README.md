# Проект "Docker deploy"

Суть этого проекта заключается в упаковке проекта в контейнеры Docker.


# Технологии

 - Python
 - Django
 - Docker
 - Django Rest Framework
 - Gunicorn
 - NGINX

## Запуск проекта

Для запуска проекта необходимо выполнить следующие действия:

 1. Установить Docker
 2. Клонировать репозиторий с проектом
 3. Перейти в корневую директорию проекта и в терминале выполнить команду `docler build -t yamdb .`
 4. Перейти в директорию infra и выполнить команду `docker-compose up -d --build`
 5. Выполнить следующие команды:
	 - `docker-compose exec web python manage.py makemigrations reviews`
	 - `docker-compose exec web python manage.py migrate`
	 - `docker-compose exec web python manage.py createsuperuser`
	 - `docker-compose exec web python manage.py collectstatic --no-input `
 6. Перейти по адресу http://localhost/

 

Автор проекта: [Павел Корчилов](https://github.com/pencool)
