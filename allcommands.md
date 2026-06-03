# 🐳 Docker Essential Commands (Simple Cheat Sheet)

## Check Docker

```bash
docker --version
```

→ Shows installed Docker version.

```bash
docker info
```

→ Shows Docker system details.

---

# Images (App Templates)

```bash
docker images
```

→ Show all downloaded images.

```bash
docker pull nginx
```

→ Download an image.

```bash
docker rmi IMAGE_NAME
```

→ Delete an image.

Example:

```bash
docker rmi nginx
```

---

# Containers (Running Apps)

```bash
docker run nginx
```

→ Create and start a container.

```bash
docker run -d nginx
```

→ Run in background.

```bash
docker run -p 3000:3000 nginx
```

→ Connect container port to your PC.

Format:

```text
HOST:CONTAINER
```

```bash
docker run --name myapp nginx
```

→ Give container a custom name.

---

# View Containers

```bash
docker ps
```

→ Show running containers.

```bash
docker ps -a
```

→ Show all containers.

---

# Control Containers

```bash
docker stop CONTAINER
```

→ Stop container.

Example:

```bash
docker stop myapp
```

```bash
docker start CONTAINER
```

→ Start stopped container.

```bash
docker restart CONTAINER
```

→ Restart container.

```bash
docker rm CONTAINER
```

→ Delete container.

---

# Logs & Debugging

```bash
docker logs CONTAINER
```

→ Show logs/output.

```bash
docker logs -f CONTAINER
```

→ Watch logs live.

```bash
docker exec -it CONTAINER bash
```

→ Open terminal inside container.

Example:

```bash
docker exec -it myapp bash
```

---

# Build Your App

```bash
docker build -t app-name .
```

→ Build image from Dockerfile.

Example:

```bash
docker build -t backend .
```

---

# Docker Compose

```bash
docker compose up
```

→ Start all services.

```bash
docker compose up -d
```

→ Start in background.

```bash
docker compose down
```

→ Stop all services.

```bash
docker compose logs
```

→ Show compose logs.

---

# Storage (Volumes)

```bash
docker volume ls
```

→ List storage volumes.

```bash
docker volume create data
```

→ Create volume.

---

# Networks

```bash
docker network ls
```

→ Show networks.

```bash
docker network create app-net
```

→ Create network.

---

# Cleanup

```bash
docker container prune
```

→ Delete stopped containers.

```bash
docker image prune
```

→ Delete unused images.

```bash
docker system prune -a
```

→ Delete everything unused.

---

# Daily Workflow

```bash
docker build -t app .
docker run -p 3000:3000 app
docker ps
docker logs container
docker stop container
docker rm container
```

---

# Memory Trick

```text
Pull → Run → View → Debug → Stop → Remove
```
