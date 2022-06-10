### Учебный проект по Docker
Этот проект может многое.
### Технологии
Python 3.7
Django 2.2.16
gunicorn 20.0.4
postgresql 13
nginx 1.21.3
### Запуск проекта
- клонировать проект с GitHub
- Перейти в каталог с docker-compose
cd .../infra_sp2/infra
- Собрать контейнер 
docker-compose up
- сделать миграции, создать пользователя и собрать статику
```
docker-compose exec web python manage.py migrate
```
```
docker-compose exec web python manage.py createsuperuser
```
```
docker-compose exec web python manage.py collectstatic --no-input
```