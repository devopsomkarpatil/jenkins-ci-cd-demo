# Jenkins CI/CD Demo

This project showcases a complete CI/CD pipeline using Jenkins, Docker, Kubernetes, and Helm.

## 🔧 Stack
- Jenkins
- Docker
- Kubernetes (minikube or GKE)
- Helm
- Python (Flask app)

## 🚀 Pipeline Overview
1. Jenkins clones the repo
2. Builds and pushes Docker image to Docker Hub
3. Deploys app to Kubernetes using Helm

## 📦 How to Run
```bash
# Build & run locally
docker build -t jenkins-demo .
docker run -p 5000:5000 jenkins-demo

# Run Helm deploy manually
helm upgrade --install jenkins-demo helm-chart
```

## 📊 Architecture Diagram
![diagram](diagram.png)

## 📎 Notes
- Store DockerHub password in Jenkins credentials
- Make sure `kubectl` and `helm` are configured on Jenkins agent
