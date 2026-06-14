# 🚀 MERN Stack Deployment using Kubernetes (Minikube + AWS EKS + Helm)
---

## 📌 Project Overview

This project demonstrates the complete deployment of a **MERN Stack Application (MongoDB, Express, React, Node.js)** using modern DevOps tools:

- Docker (containerization)
- Kubernetes (orchestration)
- Minikube (local deployment)
- AWS EKS (cloud deployment)
- Helm (package manager for Kubernetes)

---

## 🏗️ Application Architecture

The application consists of three main components:

- 🎨 Frontend → React.js (served via Nginx)
- ⚙️ Backend → Node.js + Express API
- 🗄️ Database → MongoDB

---

## 📁 Project Structure
# 🚀 MERN Stack Deployment using Kubernetes (Minikube + AWS EKS + Helm)


## 📌 Project Overview

This project demonstrates the complete deployment of a **MERN Stack Application (MongoDB, Express, React, Node.js)** using modern DevOps tools:

- Docker (containerization)
- Kubernetes (orchestration)
- Minikube (local deployment)
- AWS EKS (cloud deployment)
- Helm (package manager for Kubernetes)

---

## 🏗️ Application Architecture

The application consists of three main components:

- 🎨 Frontend → React.js (served via Nginx)
- ⚙️ Backend → Node.js + Express API
- 🗄️ Database → MongoDB

---

## 📁 Project Structure
# 🚀 MERN Stack Deployment using Kubernetes (Minikube + AWS EKS + Helm)

---

## 📌 Project Overview

This project demonstrates the complete deployment of a **MERN Stack Application (MongoDB, Express, React, Node.js)** using modern DevOps tools:

- Docker (containerization)
- Kubernetes (orchestration)
- Minikube (local deployment)
- AWS EKS (cloud deployment)
- Helm (package manager for Kubernetes)

---

## 🏗️ Application Architecture

The application consists of three main components:

- 🎨 Frontend → React.js (served via Nginx)
- ⚙️ Backend → Node.js + Express API
- 🗄️ Database → MongoDB

---

## 📁 Project Structure
├── client/ # React frontend
├── server/ # Node.js backend
├── k8s/ # Kubernetes manifests
│ ├── frontend-deployment.yaml
│ ├── backend-deployment.yaml
│ ├── mongo-deployment.yaml
│ ├── frontend-service.yaml
│ ├── backend-service.yaml
│ └── mongo-service.yaml
├── blog-app/ # Helm Chart
│ ├── templates/
│ ├── values.yaml
│ ├── Chart.yaml
├── docker-compose.yaml
└── README.md

---

## 🐳 Docker Images

The application uses pre-built Docker images:

- Frontend: `arshen00r/blog-client:v1`
- Backend: `arshen00r/blog-server:v1`
- Database: `mongo:latest`

---

## ☸️ Kubernetes Deployment (Minikube / EKS)

### 🔹 Deploy application

```bash
kubectl apply -f k8s/

Check running resources
kubectl get pods
kubectl get services
kubectl get nodes
```
## 🌐 Access Application

Frontend is exposed using NodePort service:

http://<NODE-IP>:30090

To get node IP:

kubectl get nodes -o wide
⛵ Helm Deployment
Install Helm Chart
helm install blog-release ./blog-app
Upgrade Release
helm upgrade blog-release ./blog-app
Uninstall Release
helm uninstall blog-release
## ☁️ AWS EKS Deployment
Step 1: Create Cluster
eksctl create cluster \
  --name blog-eks-cluster \
  --region us-east-1 \
  --nodes 2 \
  --node-type t3.small
Step 2: Configure kubectl
aws eks update-kubeconfig \
  --region us-east-1 \
  --name blog-eks-cluster
Step 3: Deploy Application
kubectl apply -f k8s/
## 📊 Verification Commands
kubectl get pods -o wide
kubectl get services
kubectl get nodes
## 📸 Screenshots

Include screenshots of:

Pods running successfully
Services (NodePort / ClusterIP)
EKS nodes
Application running in browser
## 🎯 Key Learnings
Docker containerization of full-stack application
Kubernetes deployments & services
Helm chart creation and management
AWS EKS cluster provisioning
Multi-node Kubernetes scheduling
Real-world DevOps workflow implementation
## 🏁 Conclusion

This project demonstrates a complete CI/CD-style deployment workflow:

👉 Build → Containerize → Deploy Locally → Deploy on Cloud → Manage via Helm

## ✅ Status

✔ Dockerized
✔ Kubernetes deployed
✔ Helm chart created
✔ AWS EKS cluster configured
✔ Application running successfully

## 👨‍💻 Author
Arshenoor