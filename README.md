# 🚀 DevSecOps CI/CD Pipeline on AWS using GitHub Actions, Jenkins & Kubernetes

A production-inspired DevSecOps project that automates the complete software delivery lifecycle—from code commit to Kubernetes deployment—using modern DevSecOps tools and security best practices.

![GitHub Actions](https://img.shields.io/badge/GitHub-Actions-2088FF?style=for-the-badge&logo=github-actions)
![Jenkins](https://img.shields.io/badge/Jenkins-CI%2FCD-D24939?style=for-the-badge&logo=jenkins)
![Docker](https://img.shields.io/badge/Docker-Containers-2496ED?style=for-the-badge&logo=docker)
![Kubernetes](https://img.shields.io/badge/Kubernetes-K3s-326CE5?style=for-the-badge&logo=kubernetes)
![AWS](https://img.shields.io/badge/AWS-EC2-FF9900?style=for-the-badge&logo=amazonaws)
![SonarCloud](https://img.shields.io/badge/SonarCloud-Code%20Quality-4E9BCD?style=for-the-badge&logo=sonarcloud)
![Trivy](https://img.shields.io/badge/Trivy-Container%20Security-1904DA?style=for-the-badge)

---

# 📖 Overview

This project demonstrates an end-to-end DevSecOps pipeline that automatically:

- Performs Static Application Security Testing (SAST)
- Builds a Docker image
- Scans the image for vulnerabilities
- Pushes the secure image to Docker Hub
- Deploys the application to a Kubernetes cluster hosted on AWS

Every push to the **main** branch triggers an automated workflow, ensuring code quality, container security, and continuous deployment.

---

# 🏗 Architecture

```text
Developer
     │
     ▼
 GitHub Repository
     │
     ▼
GitHub Actions
     │
     ├──────────────► SonarCloud
     │                 (Code Quality)
     │
     ├──────────────► Docker Build
     │
     ├──────────────► Trivy Scan
     │                 (Container Security)
     │
     ▼
 Docker Hub
     │
     ▼
 Jenkins
     │
     ▼
 Kubernetes (K3s)
     │
     ▼
 AWS EC2 Instance
     │
     ▼
 Live Node.js Web Application
```

---

# 🛠 Technologies Used

| Category | Technologies |
|----------|--------------|
| Cloud | AWS EC2 |
| Containerization | Docker |
| Container Registry | Docker Hub |
| CI | GitHub Actions |
| CD | Jenkins |
| Container Orchestration | Kubernetes (K3s) |
| Code Quality | SonarCloud |
| Vulnerability Scanning | Trivy |
| Backend | Node.js, Express.js |
| Version Control | Git & GitHub |

---

# ⚙ CI/CD Workflow

## Continuous Integration (GitHub Actions)

On every push to the **main** branch:

- Checkout source code
- Install dependencies
- Build Docker image
- Perform SonarCloud Static Code Analysis
- Scan Docker image using Trivy
- Push secure image to Docker Hub

---

## Continuous Deployment (Jenkins)

Jenkins automatically:

- Connects securely to the Kubernetes cluster
- Pulls the latest Docker image
- Creates or updates the Kubernetes Deployment
- Exposes the application using a Kubernetes Service
- Verifies deployment status

---

# 🔒 Security Features

- Static Application Security Testing (SonarCloud)
- Container Vulnerability Scanning (Trivy)
- Kubernetes Deployment Automation
- Docker Image Versioning
- Secure Jenkins Credentials Management
- AWS Security Group Configuration
- Kubernetes Cluster Isolation using K3s

---

# 📂 Project Structure

```text
DevSecOps_CI_CD_Pipeline/
│
├── .github/
│   └── workflows/
│       └── main.yml
│
├── k8s/
│   ├── deployment.yaml
│   └── service.yaml
│
├── app/
│   ├── server.js
│   └── package.json
│
├── Dockerfile
├── Jenkinsfile
└── README.md
```

---

# 🚀 Deployment Pipeline

## Step 1

Developer pushes code to GitHub.

↓

## Step 2

GitHub Actions starts automatically.

↓

## Step 3

SonarCloud performs code quality analysis.

↓

## Step 4

Docker image is built.

↓

## Step 5

Trivy scans the image for vulnerabilities.

↓

## Step 6

Image is pushed to Docker Hub.

↓

## Step 7

Jenkins deploys the latest image to Kubernetes.

↓

## Step 8

Application becomes available on the AWS EC2 Kubernetes cluster.


---

# ⚙ Installation

Clone the repository

```bash
git clone https://github.com/CloudwithGarv/DevSecOps_CI_CD_Pipeline.git

cd DevSecOps_CI_CD_Pipeline
```

---

# Run the application locally

```bash
npm install

npm start
```

---

# Build Docker Image

```bash
docker build -t devsecops-webapp .
```

---

# Run Docker Container

```bash
docker run -d -p 80:80 devsecops-webapp
```

---

# Deploy to Kubernetes

```bash
kubectl apply -f k8s/
```

---

# 📊 CI/CD Pipeline Components

| Tool | Purpose |
|------|---------|
| GitHub | Source Code Management |
| GitHub Actions | Continuous Integration |
| SonarCloud | Static Code Analysis |
| Docker | Application Containerization |
| Trivy | Vulnerability Scanning |
| Docker Hub | Image Registry |
| Jenkins | Continuous Deployment |
| Kubernetes (K3s) | Container Orchestration |
| AWS EC2 | Production Infrastructure |

---

# 📈 Skills Demonstrated

- DevSecOps
- CI/CD Pipeline Design
- Docker Containerization
- Kubernetes Deployment
- Jenkins Automation
- GitHub Actions
- SonarCloud Integration
- Trivy Security Scanning
- AWS EC2 Administration
- Linux System Administration
- YAML Pipeline Development
- Container Security
- Kubernetes Networking

---

# 🎯 Resume Highlights

- Designed and implemented a complete DevSecOps CI/CD pipeline using GitHub Actions, Jenkins, Docker, Kubernetes, and AWS.
- Automated code quality analysis with SonarCloud before deployment.
- Integrated Trivy for automated container vulnerability scanning.
- Built and published Docker images to Docker Hub.
- Automated Kubernetes deployments on an AWS-hosted K3s cluster using Jenkins.
- Implemented secure credential management for Kubernetes deployment.
- Troubleshot real-world networking, TLS, and Kubernetes deployment issues.

---

# 🔮 Future Improvements

- HTTPS using Let's Encrypt
- NGINX Ingress Controller
- Helm Charts
- Argo CD (GitOps)
- Prometheus & Grafana Monitoring
- Falco Runtime Security
- Terraform Infrastructure Provisioning
- Kubernetes Secrets Management
- Horizontal Pod Autoscaling
- Elastic IP & Domain Name Integration

---

# 👨‍💻 Author

**Garv Garg**

GitHub: https://github.com/CloudwithGarv

LinkedIn: https://www.linkedin.com/in/cloudwithgarv/

---

⭐ If you found this project useful, consider giving it a star!
