# 🚀 Jenkins CI/CD Pipeline for Node.js App

This project demonstrates how to automate the build and deployment of a simple Node.js application using Jenkins and Docker.

---

## 📁 Project Structure

- `index.js` – Basic Node.js web server
- `package.json` – Project metadata and dependencies
- `Dockerfile` – Container setup instructions
- `Jenkinsfile` – Jenkins pipeline configuration

---

## 🔧 Technologies Used

- **Jenkins** – Automation server for CI/CD
- **Docker** – Containerization platform
- **GitHub** – Code hosting and version control
- **Node.js** – JavaScript runtime environment

---

## 📌 Jenkins Pipeline Stages

1. **Build Docker Image**  
   Builds the Docker image using the Dockerfile and tags it as `siri1419/jenkins-demo-app`.

2. **Run App**  
   Runs the Docker container on port 3000.

---

## ▶️ How to Run Jenkins with Docker (Locally)

```bash
docker run -d \
  --name jenkins-docker \
  -p 8080:8080 -p 50000:50000 \
  -v jenkins_home:/var/jenkins_home \
  -v /var/run/docker.sock:/var/run/docker.sock \
  jenkins/jenkins:lts
