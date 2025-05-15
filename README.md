
# 🚀 CI/CD for Kubernetes using GitHub Actions

This project demonstrates setting up a CI/CD pipeline using GitHub Actions to build a Docker image, push it to DockerHub, and deploy it to an AKS Kubernetes cluster.

---

## 🎯 Objectives

- Automate Docker build and push using GitHub Actions
- Deploy Kubernetes manifests to AKS
- Securely manage secrets (DockerHub credentials, K8s configs)

---

## 🧰 Tools Used

- GitHub Actions
- Docker & DockerHub
- Kubernetes (AKS or any K8s cluster)
- `kubectl`

---

## 📂 Project Structure

```
k8s-ci-githubactions/
├── .github/
│   └── workflows/
│       └── ci-cd.yml
├── k8s/
│   └── deployment.yaml
├── Dockerfile
├── README.md
└── images/
    └── architecture-diagram.png
```

---

## 🔄 Workflow

1. Push to `main` branch
2. GitHub Actions builds & pushes Docker image
3. Applies `k8s/deployment.yaml` to your cluster via `kubectl`

---

## 🔐 Secrets Required

- `DOCKER_USERNAME`
- `DOCKER_PASSWORD`

Add these in your GitHub repo under **Settings > Secrets and variables > Actions**.

---

## 🖼️ Architecture

![architecture](images/architecture-diagram.png)

---

## 📌 Notes

- This is a real deployable GitHub Actions pipeline, replace placeholders with your actual DockerHub username.
- Can be extended to support Helm, Canary deployments, Slack notifications, etc.

---

👤 **Author:** [Rukesh Dasari](https://github.com/rukesh24)
