# Jenkins CI/CD Demo Project

> **End-to-End CI/CD pipeline using Jenkins, Docker, Kubernetes, and Helm**

---

## 📌 Project Overview
This project demonstrates a complete CI/CD pipeline using Jenkins, integrated with Docker for containerization and Kubernetes for orchestration. Helm is used for Kubernetes deployment.

![](diagram.png) <!-- Optional: Replace with actual architecture diagram -->

---

## ⚙️ Tech Stack
- **CI/CD**: Jenkins
- **Containerization**: Docker
- **Orchestration**: Kubernetes
- **Package Manager**: Helm
- **Infrastructure as Code**: Terraform (for infra, not used directly in this demo)
- **Monitoring & Logging**: Prometheus, Grafana, ELK, CloudWatch (can be added later)
- **Language**: Python (Flask)

---

## 🚀 Features
- Simple Flask app
- Dockerized build
- Jenkins pipeline for CI/CD
- Helm chart for Kubernetes deployment
- Easily customizable for real-world microservices

---

## 🧾 Folder Structure
```
jenkins-ci-cd-demo/
├── app/                  # Python Flask application
│   └── app.py
├── Dockerfile            # Docker build file
├── Jenkinsfile           # Jenkins pipeline
├── helm-chart/           # Helm chart for Kubernetes deployment
│   ├── Chart.yaml
│   ├── templates/
│   │   └── deployment.yaml
│   │   └── service.yaml
│   └── values.yaml
├── README.md             # Project documentation
└── diagram.png           # (Optional) Architecture diagram
```

---

## 🔁 Jenkins Pipeline Overview
1. **Checkout code from GitHub**
2. **Build Docker image**
3. **Push Docker image to DockerHub**
4. **Deploy to Kubernetes using Helm**

---

## 🛠️ Setup Instructions

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/jenkins-ci-cd-demo.git
cd jenkins-ci-cd-demo
```

### 2. Jenkins Setup
- Install required plugins: Docker, Kubernetes CLI, Helm
- Create Jenkins credentials:
  - `dockerhub-pass`: DockerHub token (secret text)
- Add `Jenkinsfile` to a multibranch pipeline job

### 3. DockerHub Setup
- Replace `DOCKER_USERNAME` in `Jenkinsfile` and `values.yaml`

### 4. Kubernetes Cluster
- Use Minikube, EKS, or GKE
- Ensure `kubectl` and `helm` access

---

## 📦 Build & Deploy (Manual Option)

### Build Docker Image
```bash
docker build -t your-username/jenkins-flask-demo:latest .
docker push your-username/jenkins-flask-demo:latest
```

### Deploy with Helm
```bash
cd helm-chart
helm install jenkins-demo .
```

---

## 👤 Author
**Omkar Patil**  
[GitHub](https://github.com/devopsomkarpatil)

---

## 📄 License
MIT
