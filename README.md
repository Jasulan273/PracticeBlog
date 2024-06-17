# Blog API Django (Practice AITU)

This project is a simple blog API implemented in Django, using Django REST Framework.

---

## Running the Project

### Requirements

- Python 3.10+
- Docker

### Installation

Create and activate a virtual environment (optional if not using Docker):

```
python -m venv venv
. venv/bin/activate  # for Unix/macOS
venv\Scripts\activate  # for Windows
```

## Install dependencies:

```
pip install -r requirements.txt
```

### Running with Docker

Build and run the Docker container:

```
docker build -t blogproject .
docker run -p 8000:8000 blogproject
```
### Running without Docker

Apply database migrations:
```
python manage.py migrate
```
Create a superuser for accessing the admin panel:
```
python manage.py createsuperuser
```
Start the development server:
```
python manage.py runserver
```

## Accessing the Admin Panel

The admin panel is available at http://localhost:8000/admin/.
Use the credentials of the superuser created earlier to log in.

---

## Using the API

The API provides the following endpoints:

- `/api/token/`: Obtain JWT token for authentication.
- `/api/token/refresh/`: Refresh JWT access token.
- `/api/posts/`: Endpoints for managing posts (GET, POST, PUT, DELETE).
- `/api/comments/`: Endpoints for managing comments (GET, POST, PUT, DELETE).

To access protected endpoints, include the JWT access token in the Authorization header.

---

## Note

For full functionality of the project, it is recommended to familiarize yourself with Django and Django REST Framework settings and documentation.
