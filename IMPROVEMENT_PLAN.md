# Improvement Plan: hierarchical_data

## Overview
Django 3 + django-mptt hierarchical file/folder app. No REST API, no authentication, hardcoded admin credentials, and no containerization.

## Improvements

### Security (High Priority)
- Change the default admin credentials (`hasan`/`1234`) — never ship a project with hardcoded credentials
- Move `SECRET_KEY`, `DEBUG`, and DB credentials to environment variables via `django-environ`
- Add `ALLOWED_HOSTS` configuration and HTTPS-only settings for production

### API Layer
- Add Django REST Framework to expose a RESTful API for the tree structure (list children, move nodes, create/delete)
- Alternatively, add a GraphQL API using `graphene-django` — hierarchical data maps naturally to GraphQL queries

### Authentication & Authorization
- Add user authentication (Django's built-in auth or `django-allauth`)
- Add per-node permissions: users should only see/modify their own files/folders

### Frontend
- Add a simple React or Alpine.js frontend to render the tree interactively (expand/collapse nodes, drag-and-drop to rearrange)
- Currently the app is admin-only — a real frontend would make the demo usable

### Testing
- Add pytest + `pytest-django` tests for node creation, deletion, and tree traversal
- Add factory_boy fixtures for generating test trees

### DevOps
- Add a `Dockerfile` and `docker-compose.yml` (app + PostgreSQL)
- Switch from SQLite to PostgreSQL for production parity and better django-mptt performance
- Add GitHub Actions CI: lint + test
