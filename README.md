# 🚀 Docker + Kubernetes Deployment using Minikube

This project demonstrates deploying a containerized Node.js application on a local Kubernetes cluster using **Docker**, **Kubernetes**, and **Minikube**.  
It is designed as a production-style DevOps project suitable for resumes and interviews.

---

## 📦 Project Overview

### What this project includes:
- Dockerized Node.js application  
- Kubernetes Deployment & Service (NodePort)
- Local Kubernetes cluster using Minikube  
- DockerHub image publishing  
- Accessing the app via browser  
- Real-world DevOps folder structure  
- Screenshots of the working setup  

---

## 📁 Folder Structure

docker-Kubernetes-deployment/
│
├── app/
│ ├── server.js
│ └── package.json
│
├── k8s/
│ ├── deployment.yaml
│ └── service.yaml
│
├── screenshots/
│ └── (runtime screenshots)
│
├── Dockerfile
└── README.md



yaml
---

## 🐳 Step 1 — Docker Build & Push

Build the Docker image:

```bash
docker build -t thrinadhprasadapu/k8s-app:latest .


Login to DockerHub (only once):

docker login


Push the image:

docker push thrinadhprasadapu/k8s-app:latest

☸️ Step 2 — Start Minikube
minikube start --driver=docker


Check cluster status:

kubectl get nodes

📦 Step 3 — Deploy to Kubernetes

Apply Deployment & Service:

kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml


Verify resources:

kubectl get pods
kubectl get svc

🌐 Step 4 — Access the Application

Open the Node.js app running on Kubernetes:

minikube service k8s-app-service


This exposes the app in your browser via a NodePort.

You should see:

Hello from Docker + Kubernetes + Minikube!

🛠️ Tech Stack

Docker

Kubernetes

Minikube

Node.js

DockerHub

kubectl

📌 Key Learnings 

Built and containerized application using Docker

Deployed microservice to Kubernetes using Deployment & Service

Managed local Kubernetes cluster with Minikube

Pushed container image to DockerHub

Exposed service using NodePort and accessed via browser

👤 Author

Thrinadh Prasadapu

DevOps • AWS • Terraform • Docker • Kubernetes


