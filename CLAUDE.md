# Hierarchical Data

Django 3 application demonstrating a Dropbox-style hierarchical file/folder structure using `django-mptt` for nested set tree storage.

## Tech Stack
- Python 3
- Django 3
- django-mptt (Modified Preorder Tree Traversal)
- Poetry (dependency management)

## Project Structure
```
hierarchicaldata/
├── files/
│   ├── models.py       # MPTTModel for file/folder nodes
│   └── views.py
├── manage.py
└── pyproject.toml
```

## Development
```bash
# Install dependencies
poetry install

# Apply migrations
poetry run python manage.py migrate

# Run development server
poetry run python manage.py runserver
```

## Key Notes
- Default admin credentials: `hasan` / `1234`.
- `django-mptt` must be installed and `mptt` must be in `INSTALLED_APPS`.
