
# 🟢 3. README — branch3 (CI with GitHub Actions)

# ⚙️ Step 3: CI using GitHub Actions

## 📌 Objective

Automate build and push Docker image to DockerHub.

## 🧠 What This Step Covers

* GitHub Actions CI
* Docker build & push
* Secrets management

## 🔐 Required Secrets

Add in GitHub:

* DOCKERHUB_USERNAME
* DOCKERHUB_TOKEN

## 🔁 Workflow

```
Git Push → GitHub Actions → Build → Push to DockerHub
```

## ✅ Output

* Docker image pushed automatically
* Tagged using GitHub run ID

## 🔚 Next Step

👉 Move to **main branch** for full CI/CD with Helm + ArgoCD.
