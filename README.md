devOps-tasks/
│
├── Dockerfile
├── Jenkinsfile
├── index.html
├── README.md
└── screenshots/
    ├── jenkins-success.png
    └── browser-output.png

# DevOps CI/CD Pipeline using Jenkins & Docker

## Project Overview
This project demonstrates a complete **CI/CD pipeline** that automates the build,
push, and deployment of an HTML web application using **Jenkins** and **Docker**.

The pipeline pulls source code from GitHub, builds a Docker image, pushes it to
Docker Hub securely using access tokens, and deploys the container automatically.

---

## Technologies Used
- Jenkins (Declarative Pipeline)
- Docker & Docker Hub
- Git & GitHub
- HTML & Nginx
- Linux

---

## CI/CD Workflow
1. Source code checkout from GitHub
2. Docker image build using Dockerfile
3. Secure Docker Hub login via Jenkins credentials
4. Push image to Docker Hub
5. Run container and expose application on port `8070`

---

## 📂 Project Structure
