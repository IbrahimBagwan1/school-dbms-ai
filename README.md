# School DBMS + AI System

An AI-powered School Database Management System built with Django, FastAPI, PostgreSQL, PyTorch, HTMX, Celery, Redis & Docker.

A modern, scalable system combining a full-featured Django web app (admin + templates) with a FastAPI ML inference service and background workers.

---

## Quick overview

- Django: web app, admin, templates, role-based auth  
- FastAPI: ML inference endpoints (PyTorch models)  
- PostgreSQL: primary database  
- Redis: cache + Celery broker  
- Celery: background tasks (reports, async jobs)  
- MLflow: model tracking & registry  
- HTMX + Bootstrap: dynamic, lightweight UI  
- Docker Compose: one-command full stack

---

## Features

Core DBMS
- Student, teacher management
- Classes, divisions, subjects
- Attendance, exams, marks, report cards
- Admin dashboards, role-based auth, secure internal APIs

AI features
- Text similarity for complaint classification
- NER for information extraction
- Predictive analytics modules
- ML model versioning via MLflow
- FastAPI inference endpoint

Extras
- Complaint registration & categorization
- Automated report generation (Celery)
- Optional: online voting (blockchain extension)

---

## Tech stack

Backend
- Django, Gunicorn, Uvicorn

ML & AI
- PyTorch, MLflow, FastAPI

DB & Cache
- PostgreSQL, Redis

Frontend
- Django templates, HTMX, Bootstrap

Infra
- Docker, Docker Compose, nginx

---

## Project structure

school-dbms-ai/
│
├── web/                     # Django web application
│   ├── school/              # Django project settings
│   ├── apps/                # Students, Teachers, Attendance, etc.
│   ├── templates/           # Django + HTMX templates
│   ├── static/              # CSS/JS/Bootstrap
│   └── Dockerfile
│
├── ml/                      # FastAPI ML service
│   ├── model/               # PyTorch models
│   ├── main.py              # Inference API
│   └── Dockerfile
│
├── nginx/
│   └── nginx.conf
│
├── infra/
│   └── docker-compose.prod.yml
│
├── docker-compose.yml
├── .env.example
├── README.md
└── requirements.txt

---

## Getting started

1. Clone
```
git clone https://github.com/your-username/school-dbms-ai.git
cd school-dbms-ai
```

2. Create environment file
```
cp .env.example .env
# Edit .env as needed (DATABASE_URL, REDIS_URL, SECRET_KEY, etc.)
```

3. Build & start
```
docker-compose up --build
```

4. Services (default ports)
- Django Web App: http://localhost:8000/
- FastAPI ML Service (docs): http://localhost:8001/docs
- Admin Panel: http://localhost:8000/admin/
- Nginx (if enabled): http://localhost/

---

## Environment variables (example keys)

- SECRET_KEY
- DATABASE_URL (Postgres)
- REDIS_URL
- MLFLOW_TRACKING_URI
- DJANGO_ALLOWED_HOSTS
- EMAIL / SMTP settings (optional)

Refer to .env.example for full list.

---

## Development & testing

Run Django tests:
```
docker-compose exec web python manage.py test
```

Local ML model changes:
- Replace or update model files in /ml/model/
- Restart ml service or re-deploy container

CI & quality:
- Black formatter
- Pre-commit hooks (optional)
- GitHub Actions for CI (tests & builds)

---

## MLflow

- Models logged to configured MLflow server
- Use MLflow UI to browse model versions
- Inference service reads model files from /ml/model/ or from MLflow registry (configurable)

---

## Deployment

- Use docker-compose.prod.yml for production orchestration
- Use nginx as reverse proxy and SSL termination
- Ensure environment variables and secrets are set securely
- Use a managed Postgres or secure production Postgres instance

---

## Contributing

- Fork the repo
- Create a feature branch
- Commit changes with clear messages
- Open a PR and describe the changes
- Follow code style and run tests

---

## License

MIT License (change if preferred)

---

## Author

Ibrahim Rasulahmed Bagwan  
Belgaum, Karnataka  
YouTube: AI with Ibrahim

---

If this README is for a public repo, consider adding usage examples, endpoint docs (FastAPI), and sample screenshots for clarity.