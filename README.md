# 🚀 Kubernetes Node.js Deployment

Deploying a containerized Node.js application on Kubernetes using Deployments and Services.

---

## 📌 Project Overview

This project demonstrates how to deploy a Dockerized Node.js application on a Kubernetes cluster using declarative YAML manifests.

The application is containerized with Docker, pushed to Docker Hub, and deployed to Kubernetes using a Deployment and exposed through a Service.

This project helped me understand how Kubernetes manages Pods, Deployments, ReplicaSets, Services, self-healing, and application scaling.

---

## 🏗️ Architecture

```
               +--------------------+
               |    Developer       |
               +---------+----------+
                         |
                         |
                  Docker Build
                         |
                         ▼
               +------------------+
               | Docker Image     |
               +------------------+
                         |
                  Push to Docker Hub
                         |
                         ▼
                Kubernetes Cluster
                         |
          +--------------+--------------+
          |                             |
    Deployment                  ReplicaSet
          |                             |
          +--------------+--------------+
                         |
                     Multiple Pods
                         |
                     Kubernetes Service
                         |
                         ▼
                    End Users
```

---

## 🛠️ Tech Stack

- Node.js
- Docker
- Kubernetes
- Docker Hub
- kubectl
- YAML

---

## 📂 Project Structure

```
.
├── app.js
├── Dockerfile
├── deployment.yaml
├── service.yaml
└── README.md
```

---

## ⚙️ Features

- Containerized Node.js application
- Docker image creation
- Kubernetes Deployment
- Kubernetes Service
- Automatic Pod recreation
- Scalable architecture
- Declarative Infrastructure using YAML

---

## 📦 Docker Image

Build Docker Image

```bash
docker build -t myapp .
```

Run Container

```bash
docker run -d -p 3000:3000 myapp
```

Push Image

```bash
docker tag myapp sufyaan04/myapp:latest

docker push sufyaan04/myapp:latest
```

---

## ☸️ Kubernetes Deployment

Apply Deployment

```bash
kubectl apply -f deployment.yaml
```

Apply Service

```bash
kubectl apply -f service.yaml
```

---

## 🔍 Useful Kubernetes Commands

Check Pods

```bash
kubectl get pods
```

Check Deployments

```bash
kubectl get deployments
```

Check Services

```bash
kubectl get svc
```

Describe Pod

```bash
kubectl describe pod <pod-name>
```

View Logs

```bash
kubectl logs <pod-name>
```

Delete Pods

```bash
kubectl delete pods --all
```

---

## 🌐 Output

After deployment, the application is exposed using a Kubernetes Service.

Example Output

```
Hello from Kubernetes 🚀
```

---

## 🧠 Concepts Learned

- Containers vs Pods
- Docker Images
- Kubernetes Deployments
- ReplicaSets
- Services
- Cluster Networking
- Self-Healing
- Rolling Updates
- Scaling Applications
- Docker Hub Integration

---

## 🐞 Challenges Faced

During development I encountered several real-world issues, including:

- ImagePullBackOff
- CrashLoopBackOff
- Incorrect Docker image names
- Docker Hub authentication issues
- YAML configuration mistakes
- Port mapping issues
- Kubernetes Service configuration errors

Each issue was diagnosed using:

```bash
kubectl describe pod
```

```bash
kubectl logs
```

```bash
kubectl get events
```

This project significantly improved my debugging and troubleshooting skills.

---

## 📈 Future Improvements

- Horizontal Pod Autoscaler (HPA)
- Ingress Controller
- Helm Charts
- Monitoring with Prometheus & Grafana
- CI/CD using Jenkins
- Kubernetes Secrets & ConfigMaps
- Deployment on AWS EKS

---

## 🎯 Resume Highlights

- Deployed a containerized Node.js application on Kubernetes using Deployments and Services.
- Configured Docker Hub integration for automated image deployment.
- Diagnosed and resolved ImagePullBackOff and CrashLoopBackOff issues using Kubernetes debugging tools.
- Implemented declarative infrastructure with Kubernetes YAML manifests.
- Demonstrated container orchestration, self-healing, and scalable application deployment.

---

## 📸 Project Demo

### Kubernetes Deployment

![Deployment](images/kubernetes-deployment.png)

### Application Output

![Output](images/output.png)

## 👨‍💻 Author

**Mohammad Sufyaan**

Computer Science Student | Full Stack Developer | DevOps Enthusiast

GitHub: https://github.com/Sufyaan04
