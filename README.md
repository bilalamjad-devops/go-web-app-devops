
# Containzer the Application


In branch 1, we ran our application locally. In this branch 2, we contianzer our application. 

build:
```docker
docker build -t my-image .
```

run:
```docker
docker run -itd -p 8080:8080 my-image
```

Open port:
- 5000
- You can check logs: docker logs container_id

Delete container:





# 🟢 2. README — branch2 (Docker)

# 🐳 Step 2: Containerize Application using Docker

## 📌 Objective

Package the Go application into a Docker container.

## 🧠 What This Step Covers

* Writing Dockerfile
* Multi-stage builds
* Running containers

## 🏗️ Build Image

```bash
docker build -t go-web-app .
```

## ▶️ Run Container

```bash
docker run -d -p 8080:8080 go-web-app
```

## 🌐 Access App

```
http://localhost:8080
```

## ✅ Output

Application runs inside container.

## 🔚 Next Step

👉 Move to **branch3** to automate build & push using GitHub Actions.
