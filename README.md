# Sample CI Docker

## 1) Add repository secrets
Create repository secrets:
- DOCKERHUB_USERNAME = your Docker Hub username
- DOCKERHUB_TOKEN = a Docker Hub access token (not the password)

GitHub UI path: Settings → Secrets and variables → Actions → New repository secret. [Docs] [web:29]

## 2) Push to main
Commit the repository and push to main to trigger the workflow. [Docs] [web:27]

## 3) Pull and run
After the workflow completes, pull and run:

docker pull DOCKERHUB_USERNAME/sample-ci-app:latest
docker run -p 8000:8000 DOCKERHUB_USERNAME/sample-ci-app:latest
curl http://localhost:8000
