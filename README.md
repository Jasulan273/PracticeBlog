Blog API Django (Practice AITU)

Этот проект представляет собой простой API для блога, реализованный на Django, с использованием Django REST Framework.

## Запуск проекта


### Требования

- Python 3.9+
- Docker

### Установка

Создать и активировать виртуальное окружение (опционально, если не используется Docker):

python -m venv venv
. venv/bin/activate  # для Unix/macOS
venv\Scripts\activate  # для Windows


Установить зависимости:
pip install -r requirements.txt

Запуск с использованием Docker
Собрать и запустить контейнер:
docker build -t blogproject .
docker run -p 8000:8000 blogproject


Запуск без Docker
Применить миграции базы данных:
python manage.py migrate

Создать суперпользователя для доступа к админке:
python manage.py createsuperuser

Запустить сервер разработки:
python manage.py runserver

Доступ к админ панели
Админ панель доступна по адресу http://localhost:8000/admin/.
Используйте учетные данные созданного суперпользователя для входа.

Использование API
API предоставляет следующие эндпоинты:
/api/token/: Получение JWT токена для аутентификации.
/api/token/refresh/: Обновление JWT access токена.
/api/posts/: Эндпоинты для управления постами (GET, POST, PUT, DELETE).
/api/comments/: Эндпоинты для управления комментариями (GET, POST, PUT, DELETE).
Для доступа к защищенным эндпоинтам требуется передача JWT access токена в заголовке Authorization.

Примечание
Для полного функционирования проекта рекомендуется ознакомиться с настройками и документацией Django и Django REST Framework.
