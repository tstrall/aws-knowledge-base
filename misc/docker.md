# Docker

**What it is:**
- A platform for building, packaging, and running applications in containers
- Containers provide isolated environments that are lightweight and portable

---

## Core Concepts

| Concept         | Description |
|------------------|-------------|
| **Image**        | Blueprint for a container (includes app code + dependencies) |
| **Container**    | Running instance of an image |
| **Dockerfile**   | Text file with instructions to build an image |
| **Volume**       | Mount external storage into a container (for persistence) |
| **Network**      | Bridge, host, or custom networking between containers |
| **Registry**     | Storage for Docker images (Docker Hub, ECR, etc.) |

---

## Dockerfile Example
```dockerfile
FROM python:3.11-slim
WORKDIR /app
COPY requirements.txt ./
RUN pip install -r requirements.txt
COPY . .
CMD ["python", "main.py"]
```

---

## Common Commands
```bash
# Build image from Dockerfile
docker build -t my-app .

# Run container
docker run -d -p 8080:80 my-app

# List running containers
docker ps

# View logs
docker logs <container-id>

# Stop and remove container
docker stop <id> && docker rm <id>
```

---

## Volumes and Mounts
```bash
# Mount a host directory into the container
-v /host/path:/container/path
```
Use cases:
- Persist logs, config, or databases across container restarts

---

## Multi-Stage Builds (Best Practice)
```dockerfile
FROM node:20 as builder
WORKDIR /app
COPY . .
RUN npm run build

FROM nginx:alpine
COPY --from=builder /app/dist /usr/share/nginx/html
```

---

## Docker Compose
Useful for running multi-container apps
```yaml
version: '3'
services:
  web:
    build: .
    ports:
      - "5000:5000"
  redis:
    image: redis:alpine
```
```bash
docker-compose up -d
```

---

## Interview Tips
- Be ready to explain difference between image vs container
- Know how to reduce image size (slim base images, multi-stage builds)
- Understand networking and ports, especially `-p` vs `EXPOSE`
- Practice debugging with `docker logs`, `exec`, and inspecting files inside a container
