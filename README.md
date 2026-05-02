
# 🟢 3. README — branch3 (CI with GitHub Actions)

# ⚙️ Step 3: CI using GitHub Actions


# 🟡 5. GitHub Actions — branch3 (CI)

Use this:

```yaml
name: CI Pipeline

on:
  push:
    branches:
      - branch3

jobs:
  build-and-push:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout
      uses: actions/checkout@v4

    - name: Set up Go
      uses: actions/setup-go@v4
      with:
        go-version: 1.22

    - name: Build App
      run: go build -o app

    - name: Run Tests
      run: go test ./...

    - name: Login to DockerHub
      uses: docker/login-action@v3
      with:
        username: ${{ secrets.DOCKERHUB_USERNAME }}
        password: ${{ secrets.DOCKERHUB_TOKEN }}

    - name: Build & Push
      uses: docker/build-push-action@v6
      with:
        context: .
        push: true
        tags: ${{ secrets.DOCKERHUB_USERNAME }}/go-web-app:${{ github.run_id }}
```

---

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
