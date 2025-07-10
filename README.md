# 🚀 NestJS Dockerization Project

Welcome! This project demonstrates how to **dockerize a NestJS application** for easy deployment and management. Below you'll find step-by-step instructions and essential Docker commands to get started.

---

## 📦 Prerequisites

- [Docker](https://www.docker.com/) installed on your machine
- Basic knowledge of NestJS

---

## 🛠️ Docker Commands

### 1. Build the Docker Image
```bash
docker build -t my-nest-js-app:v1 .
```

### 2. List Docker Images
```bash
docker image ls
```

### 3. Create a Docker Network
```bash
docker network create --driver bridge my-nest-js-app-network
```

### 4. List Docker Networks
```bash
docker network ls
```

### 5. Create a Docker Volume
```bash
docker volume create my-nest-js-app-volume
```

### 6. List Docker Volumes
```bash
docker volume ls
```

### 7. Run the Container
```bash
docker run -d \
  --name app \
  -p 3000:3000 \
  --network my-nest-js-app-network \
  --volume my-nest-js-app-volume:/usr/src/app \
  my-nest-js-app:v1
```

### 8. Test the Application
```bash
curl http://localhost:3000
```

---
