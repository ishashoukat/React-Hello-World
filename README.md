# 🚀 React Hello World App (Docker + Kubernetes + CI/CD)

![Docker](https://img.shields.io/badge/Docker-Containerized-blue)
![Kubernetes](https://img.shields.io/badge/Kubernetes-Rancher%20Desktop-blueviolet)
![CI](https://img.shields.io/badge/CI-GitHub%20Actions-green)

---

## 📌 Overview

This project is a **Dockerized React application** deployed on **Kubernetes (Rancher Desktop)** with **CI/CD using GitHub Actions (self-hosted runner)**.

---

## 🛠️ Tech Stack

* ⚛️ React
* 🐳 Docker
* ☸️ Kubernetes (Rancher Desktop)
* 🔁 GitHub Actions (Self-hosted Runner)

---

## 📁 Project Structure

```bash
react-hello-world/
│── public/
│── src/
│── Dockerfile
│── package.json
│── package-lock.json
│── reacthelloworld.yaml
│── .github/workflows/
│── README.md
```

---

## 🐳 Docker Setup

### 🔧 Build Image

```bash
docker build -t react-hello-app:v1 .
```

---

### ▶️ Run Container

```bash
docker run -d -p 3000:3000 --name react-container react-hello-app:v1
```

---

### 🌐 Access App

Open in browser:

```
http://localhost:3000
```

---

## 📤 Push Image to Docker Hub

```bash
docker login
docker tag react-hello-app:v1 <your-dockerhub-username>/react-hello-app:v1
docker push <your-dockerhub-username>/react-hello-app:v1
```

---

## ☸️ Kubernetes Deployment (Rancher Desktop)

### 🔧 Apply Deployment

```bash
kubectl apply -f reacthelloworld.yaml
```

---

### 🔍 Check Pods

```bash
kubectl get pods
```

---

### 🌐 Check Services

```bash
kubectl get services
```

---

## 🔁 CI/CD Pipeline (GitHub Actions)

This project uses a **self-hosted GitHub runner**.

### ✅ Pipeline Steps

* Build Docker Image
* Tag Image (`v1`)
* Push to Docker Hub
* Deploy to Kubernetes

---

## 🖼️ Screenshots

> Add your screenshots inside a `screenshots/` folder

### 🐳 Docker Build

![Docker Build](screenshots/docker-build.png)

### ▶️ Running Container

![Container](screenshots/container-running.png)

### ☸️ Kubernetes Pods

![Pods](screenshots/k8s-pods.png)

---

## 🧠 Key Concepts

* Docker Image vs Container
* Port Mapping
* Kubernetes Deployment & Service
* CI/CD Automation

---

## 🧹 Cleanup

```bash
docker rm -f react-container
kubectl delete -f reacthelloworld.yaml
```

---

## 👩‍💻 Author

Your Name

---

## ⭐ Learning Outcome

* Dockerize a React App
* Push image to Docker Hub
* Deploy on Kubernetes (Rancher Desktop)
* Automate using GitHub Actions
