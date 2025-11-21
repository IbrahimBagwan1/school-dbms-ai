School DBMS + AI System
An AI-powered School Database Management System built with Django, FastAPI, PostgreSQL, PyTorch, HTMX, Celery, Redis & Docker
⭐ Overview 

This project is a modern, scalable School Management & AI System, combining:

Django (Web App + Admin + Templates)

FastAPI (Machine Learning inference service)

PostgreSQL (Primary Database)

Redis (Cache + Celery Broker)

PyTorch (AI models for similarity, NER, classification, analytics)

MLflow (Model tracking & registry)

HTMX (Dynamic UI without React)

Bootstrap (Clean UI)

Docker Compose (One-command full stack setup)

This system handles all core school operations plus integrated AI features.

🎯 Core Features
🏫 School DBMS

Student management

Teacher management

Classes, divisions, subjects

Attendance management

Exam management & marks entry

Report cards

Admin dashboards

Role-based authentication

Secure internal APIs

🤖 AI Features

Text similarity for complaint classification

NER for extracting important information

Predictive analytics modules

ML model versioning using MLflow

FastAPI inference endpoint

📢 Additional Modules

Online voting system using blockchain (optional extension)

Complaint registration & categorization

Automated report generation (Celery)

🏗 Tech Stack
Backend

Django

FastAPI

AI & ML

PyTorch

MLflow

Database & Cache

PostgreSQL

Redis

Frontend

Django Templates

HTMX

Bootstrap

Infrastructure

Docker

Docker Compose

Nginx

Gunicorn

Uvicorn

📂 Project Structure
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

🚀 Getting Started
1. Clone the repository
git clone https://github.com/your-username/school-dbms-ai.git
cd school-dbms-ai

2. Create your .env
cp .env.example .env

3. Run the entire system
docker-compose up --build

4. Access apps
Service	URL
Django Web App	http://localhost:8000/

FastAPI ML Service	http://localhost:8001/docs

Admin Panel	http://localhost:8000/admin/

Nginx (Prod Reverse Proxy)	http://localhost/
🧪 Testing

Run Django tests:

docker-compose exec web python manage.py test

🧠 MLflow Integration

Models are logged to local MLflow server.

Replace model in /ml/model/ to update inference.

All versions tracked automatically.

🛠 Development Tools

Black code formatter

Pre-commit hooks (optional)

GitHub Actions (CI for tests & builds)

🤝 Contributing

Contributions are welcome! Please follow the PR format:

Fork the repo

Create a new branch

Commit changes

Create a PR

📄 License

This project is currently under the MIT License (or change if preferred).

👤 Author

Ibrahim Rasulahmed Bagwan
Belgaum, Karnataka
YouTube: AI with Ibrahim

⭐ Support

If you like this project, consider giving the repository a ⭐ on GitHub!
