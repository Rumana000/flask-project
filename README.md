# DevOps Project – Flask App Deployment using GitHub Actions & Minikube

## Overview

This project demonstrates:

- A simple Flask application containerized using Docker.
- Automated CI/CD pipeline using GitHub Actions.
- Image pushed to DockerHub.
- Deployed the application on Kubernetes (Minikube).

## Project Structure

```
flask-project/
├── app.py
├── Dockerfile
├── requirements.txt
├── k8s/
│   ├── deployment.yaml
│   └── service.yaml
└── .github/
    └── workflows/
        └── docker-build.yml
```

## Deployment Steps

1. Push code to GitHub – triggers GitHub Actions.
2. Docker image builds and pushes to DockerHub.
3. Deploy to Minikube using:

```bash
kubectl apply -f k8s/
kubectl rollout restart deployment flask-app-deployment
minikube service flask-app-service --url
```

## Author

Shaik Umayrumaniya

## License

This project is licensed under the MIT License.



