# Социальная сеть домашних животных (API)

### Разработчик:

👨🏼‍💻Олег Чужмаров: https://github.com/floks41


## Стек технологий
[![Python](https://img.shields.io/badge/-Python-464646?style=flat-square&logo=Python)](https://www.python.org/)
[![Django](https://img.shields.io/badge/-Django-464646?style=flat-square&logo=Django)](https://www.djangoproject.com/)

- Python 3.9
- Django 3.2.3
- Django REST framework 3.12.4
- Djoser 2.1.0

:small_orange_diamond: **Пояснение.**
> Проект API социальной сети владельцев домашних животных реализован на базе фреймворка Django REST. Реализованы функции создание животного, выбор окраса, загрузка фото, создание и прикрепление достижений.

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/floks41/kittygram_final.git
```

```
cd kittygram_backend
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

* Если у вас Linux/macOS

    ```
    source env/bin/activate
    ```

* Если у вас windows

    ```
    source env/scripts/activate
    ```

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```
#  Как работает CI/CD  

Настроен запуск проекта Kittygram в контейнерах и CI/CD с помощью GitHub Actions.

Бекенд (реализован автором), фронтенд (предоставлен) и gateway (настроен автором) упакованы  в контейнеры docker compose, настроено развертывание на облачном сервере с использованием GitHub Actions.

Docker файлы бекенда, фронтенда и gateway сохранены в соответствующих папках проекта.

Пример action сохранен в файле `kittygram_workflow.yml` в корневой директории проекта, при необходимости запуска скопируйте содержимое файла в `.github/workflows/main.yml`.

Файл `docker-compose.yml` для локального запуска всего проекта находится в корне проекта.

Файл `docker-compose.production.yml` для запуска проекта на облачном сервере с использованием Github Action находится в корне проекта.

Файл настроек для gateway сервера nginx находится в папке `nginx/nginx.conf`

Проект использует базу данных PostgreSQL 13, создание соответствующего контейнера описано в файлах docker-compose.
Параметры и учетные данные базы данных задаются в файле .env.
