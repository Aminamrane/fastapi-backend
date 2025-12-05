# FastAPI Backend

Backend application built with FastAPI.

## Structure

```
fastapi-backend/
├── app/
│   ├── api/
│   ├── core/
│   ├── alembic/
│   └── tests/
├── scripts/
├── Dockerfile
└── pyproject.toml
```

## Docker

Build:
```bash
docker build -t aminamr/fastapi-backend .
```

Run:
```bash
docker run -p 8000:8000 aminamr/fastapi-backend
```

## CI/CD

Pipeline located in: `cicd-jenkins-pipelines/jenkins/Jenkinsfile.backend`

Pipeline stages:
1. Checkout code
2. Build Docker image
3. Push to Docker Hub
4. Trigger Helm deployment (backend only)

## API

- Docs: http://localhost:8000/docs
- Health: http://localhost:8000/health
