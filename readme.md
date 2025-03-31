# Django Ready-to-Go Template

A production-ready Django template to jump-start your web development projects. This template comes with essential packages pre-installed and configurations set up to help you focus on building your application.

## Features

- Pre-configured Django project structure
- SQLite database ready for development (PostgreSQL support included)
- Static files handling with WhiteNoise
- Production-ready with Gunicorn
- Virtual environment included
- Base app with initial setup

## Prerequisites

- Python installed on your system

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/purplebearr/django-ready-template.git
cd django-ready-template
```

### 2. Set up the environment

Install the required packages:

```bash
python -m pip install -r requirements.txt
```

Activate the virtual environment:

- On Windows:
```bash
env\scripts\activate
```



### 3. Run the development server

```bash
python manage.py runserver
```

Your application will be available at `http://127.0.0.1:8000/`

## Database Configuration

The template uses SQLite by default for development. If you want to use PostgreSQL:

1. Update the `DATABASES` setting in `stoark/settings.py`
2. PostgreSQL adapter (psycopg2) is already installed

## Installed Packages

- Django
- WhiteNoise (for static files in production)
- dj-database-url (for database URL configuration)
- psycopg2 (PostgreSQL adapter)
- Gunicorn (WSGI HTTP Server)

## Project Structure

```
django-ready-template/
├── base/                  # Base application
├── env/                   # Virtual environment
├── stoark/                # Main project directory
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── manage.py
└── requirements.txt
```

## Deployment

For production deployment, use Gunicorn:

```bash
gunicorn stoark.wsgi:application
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the Unlicense - see the LICENSE file for details.
