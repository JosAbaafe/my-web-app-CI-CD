# Docker, GitHub & DevSecOps Beginner Hands-On Lab

![Docker](https://img.shields.io/badge/Docker-Containerization-blue?logo=docker)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-CI%2FCD-black?logo=githubactions)
![Python](https://img.shields.io/badge/Python-3.11-yellow?logo=python)
![Flask](https://img.shields.io/badge/Flask-Web%20Framework-lightgrey?logo=flask)
![DevSecOps](https://img.shields.io/badge/DevSecOps-Security%20Automation-red)

---

# Overview

This repository contains a beginner-friendly DevSecOps hands-on lab focused on containerization, CI/CD automation, and security integration using Docker, Flask, Docker Hub, GitHub Actions, and Trivy.

The project demonstrates how to:

- Build and containerize a Flask web application
- Create a secure Docker image using best practices
- Push and pull images from Docker Hub
- Automate CI/CD workflows with GitHub Actions
- Scan container images for vulnerabilities using Trivy
- Perform automated smoke testing
- Apply DevSecOps principles in a practical workflow

---

# Technologies Used

- Docker
- Docker Hub
- Python 3.12
- Flask
- Git & GitHub
- GitHub Actions
- Trivy Vulnerability Scanner

---

# Project Structure

```bash
your-project/
├── app.py
├── templates/
│   └── index.html
├── requirements.txt
├── Dockerfile
├── .dockerignore
└── .github/
    └── workflows/
        └── docker-build-push.yml
```

---

# Flask Application

The application includes:

- A homepage endpoint (`/`)
- A health-check endpoint (`/health`)

---

# Docker Features Implemented

## Secure Dockerfile Practices

- Lightweight base image (`python:3.12-slim`)
- Layer caching optimization
- Health checks
- Reduced attack surface
- `.dockerignore` implementation

---

# CI/CD Pipeline Features

The GitHub Actions workflow performs the following:

1. Checks out source code
2. Logs into Docker Hub securely using GitHub Secrets
3. Builds the Docker image
4. Scans the image with Trivy
5. Pushes images only if scans pass
6. Runs smoke tests automatically
7. Cleans up test containers

---

# Screenshots

## 1. Running Flask Application

![Flask App Screenshot](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/0433e40082fffbebd1d9efac7f736d9197326cbd/images/3.png)

---

## 2. Health Endpoint Response

![Health Endpoint](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/0433e40082fffbebd1d9efac7f736d9197326cbd/images/4.png)

---

## 3. Docker Image Build

![Docker Build](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/0433e40082fffbebd1d9efac7f736d9197326cbd/images/Screenshot%202026-05-08%20223149.png)

---

## 4. Running Docker Container

![Docker Run](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/ff185d433f75ab37ec60559b6e981c6c208f6295/images/2.png)

---

## 5. Docker Hub Repository

![Docker Hub](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/ff185d433f75ab37ec60559b6e981c6c208f6295/images/6.png)

---

## 6. GitHub Actions Workflow Success

![GitHub Actions](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/ff185d433f75ab37ec60559b6e981c6c208f6295/images/7.png)
![GitHub Actions](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/ff185d433f75ab37ec60559b6e981c6c208f6295/images/8.png)
---

## 7. Trivy Vulnerability Scan

![Trivy Scan](https://github.com/JosAbaafe/my-web-app-CI-CD/blob/94110dea0cf0cdb62d01fd52c6894b8017e78f67/images/trivy.png)

---

# Setup Instructions

## Clone Repository

```bash
git clone https://github.com/JosAbaafe/my-web-app-CI-CD.git
cd cloned-Repo
```

---

## Build Docker Image

```bash
docker build -t my-web-app .
```

---

## Run Docker Container

```bash
docker run -d -p 5000:5000 --name webapp-test my-web-app
```

---

## Access Application

Home Page:

```bash
http://localhost:5000
```

Health Endpoint:

```bash
http://localhost:5000/health
```

---

# GitHub Actions Workflow

Workflow file location:

```bash
.github/workflows/docker-build-push.yml
```

The workflow automatically:

- Builds the image
- Performs vulnerability scanning
- Pushes secure images to Docker Hub
- Executes smoke tests

---

# Docker Hub Image

```bash
docker pull emmanuel321/my-web-app:tagname
```

---

# Example Workflow Commands

## Build Image

```bash
docker build -t my-web-app .
```

## Run Container

```bash
docker run -d -p 5000:5000 my-web-app
```

## Push Image

```bash
docker push emmanuel321/my-web-app:tagname
```

---

# Learning Outcomes

Through this lab, I gained practical experience in:

- Docker containerization
- Secure Docker image creation
- CI/CD automation
- GitHub Actions workflows
- DevSecOps practices
- Vulnerability management
- Container security best practices
- Image lifecycle management

---

# Author

**Emmanuel Awonate Abaafe**

- GitHub: https://github.com/JosAbaafe
- LinkedIn: www.linkedin.com/in/emmanuel-abaafe-524101177

---

