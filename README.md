# 🚀 Flask Docker App

A simple Flask web application containerized using Docker. This project demonstrates how to build, package, and run a Python Flask application inside a Docker container.

---

## 📌 Project Overview

This project showcases the fundamentals of containerization using Docker. The application is built with Flask and packaged into a Docker image, making it portable and easy to deploy across different environments.

---

## 🛠️ Tech Stack

- Python 3
- Flask
- Docker
- Git
- GitHub
- Jenkins (CI/CD)

---

## 📁 Project Structure

```
flask-docker-app/
│── app.py
│── Dockerfile
│── requirements.txt
│── Jenkinsfile
│── README.md
```

---

## ⚙️ Prerequisites

- Docker
- Git
- Python 3.x (optional for local execution)

---

## 🐳 Build Docker Image

```bash
docker build -t flask-docker-app .
```

---

## ▶️ Run Docker Container

```bash
docker run -d -p 5000:5000 flask-docker-app
```

Open your browser:

```
http://localhost:5000
```

---

## 📋 Docker Commands

### List Images

```bash
docker images
```

### Running Containers

```bash
docker ps
```

### Stop Container

```bash
docker stop <container_id>
```

### Remove Container

```bash
docker rm <container_id>
```

---

## 🔄 CI/CD Pipeline

This project includes a Jenkins pipeline that:

- Pulls the latest code from GitHub
- Builds the Docker image
- Runs the Docker container
- Automates the deployment workflow

Pipeline Flow:

```
GitHub
   │
   ▼
 Jenkins
   │
   ▼
 Docker Build
   │
   ▼
 Docker Container
```

---

## 🎯 Learning Outcomes

- Docker Installation
- Docker Images
- Docker Containers
- Dockerfile
- Port Mapping
- Flask Application Deployment
- Jenkins Integration
- GitHub Integration

---

## 📸 Screenshots

Add screenshots of:

- Jenkins Pipeline Success
- Docker Images
- Running Container
- Flask Application in Browser

---

## 🚀 Future Improvements

- Docker Compose
- MySQL Integration
- Nginx Reverse Proxy
- Kubernetes Deployment
- AWS EC2 Deployment
- GitHub Actions CI/CD

---

## 👨‍💻 Author

**Amit Dorwekar**

Aspiring DevOps Engineer

AWS | Docker | Jenkins | Python | Linux

GitHub: https://github.com/amitd1299
