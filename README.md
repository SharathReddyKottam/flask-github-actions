# Flask API with GitHub Actions CI/CD on AWS EC2

A Flask REST API automatically tested and deployed to AWS EC2 using GitHub Actions CI/CD pipeline.

## Project Overview
Every push to main branch automatically:
- Runs tests
- Builds Docker image
- Pushes to Docker Hub
- Deploys to AWS EC2

## Tech Stack
- Python 3.11
- Flask
- pytest
- Docker
- Docker Hub
- GitHub Actions
- AWS EC2

## Project Structure
```
flask-github-actions/
├── app.py              # Flask API
├── test_app.py         # automated tests
├── requirements.txt    # dependencies
├── Dockerfile          # container config
└── .github/
    └── workflows/
        └── ci.yml      # GitHub Actions pipeline
```

## API Endpoints
| Endpoint | Response |
|---|---|
| `/` | `{"message": "Hello from Flask!", "status": "running"}` |
| `/health` | `{"status": "healthy"}` |

## CI/CD Pipeline
1. **Test** - Run pytest automatically
2. **Build** - Build Docker image
3. **Push** - Push image to Docker Hub
4. **Deploy** - Pull and run on AWS EC2

## Live URL
```
http://44.204.180.11:5000
```