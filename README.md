# Django Tree Data (Hierarchical Data with MPTT)

A Django web application that uses `django-mptt` to manage and display hierarchical (tree-structured) data — similar to a Dropbox-style folder/file structure. Users can create nested "folders" and "files" of arbitrary depth and browse the tree in the admin panel.

## Features

- Hierarchical folder/file structure using Modified Preorder Tree Traversal (MPTT)
- Django admin integration for managing the tree
- Browse nested nodes via a web interface

## Tech Stack

- Python 3.8+
- Django 3.x
- django-mptt
- SQLite (default database)
- [Poetry](https://python-poetry.org/) — dependency management

## Prerequisites

- [Python](https://www.python.org/) 3.8+
- [Poetry](https://python-poetry.org/): `pip install poetry`

## Getting Started

### 1. Install dependencies

```bash
git clone https://github.com/ahasan09/django-tree-data
cd django-tree-data
poetry install
```

### 2. Apply migrations

```bash
poetry run python manage.py makemigrations
poetry run python manage.py migrate
```

### 3. Create a superuser

```bash
poetry run python manage.py createsuperuser
# Or use the pre-seeded credentials:
# Username: hasan  |  Password: 1234
```

### 4. Run the server

```bash
poetry run python manage.py runserver
```

Open [http://127.0.0.1:8000](http://127.0.0.1:8000) in your browser.

Access the admin at [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin).

## Alternative: pip install

```bash
pip install django django-mptt
python manage.py makemigrations
python manage.py migrate
python manage.py runserver
```

## Project Structure

```
django-tree-data/
├── hierarchicaldata/   # Django app — MPTT models and views
├── files/              # Static files
├── manage.py
└── pyproject.toml      # Poetry dependencies
```
