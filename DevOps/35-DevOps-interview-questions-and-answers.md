# 35 DevOps interview questions and answers 

## 1. What is DevOps?

**Answer:**
DevOps is a practice that combines development and operations to automate building, testing, and deploying applications.

---

## 2. What is CI/CD?

**Answer:**

* **CI (Continuous Integration):** Automatically builds and tests code after every push.
* **Continuous Delivery:** Automatically builds, tests, and prepares the application for deployment. Deployment to production is usually a manual approval step.
* **Continuous Deployment:** Automatically deploys to production after all tests pass.

---

## 3. What is GitHub Actions?

**Answer:**
GitHub Actions is GitHub's CI/CD service that automatically runs workflows like testing, building, and deployment.

---

## 4. What triggers a GitHub Action?

**Answer:**
Events like:

* Push
* Pull Request
* Manual trigger
* Scheduled time (cron)

---

## 5. What is a GitHub Actions workflow?

**Answer:**
A YAML file inside `.github/workflows/` that defines automation steps.

---

## 6. What is Docker?

**Answer:**
Docker is a platform that packages applications and their dependencies into containers so they run the same everywhere.

---

## 7. What is a Docker Image?

**Answer:**
A Docker image is a blueprint or template used to create containers.

**Image → Container**

---

## 8. What is a Docker Container?

**Answer:**
A running instance of a Docker image.

Example:

```
Image: node:22
Container: Running Node.js application
```

---

## 9. Difference between Image and Container?

**Answer:**

| Image                      | Container           |
| -------------------------- | ------------------- |
| Blueprint                  | Running application |
| Read-only                  | Running process     |
| Can create many containers | Uses one image      |

---

## 10. What is a Dockerfile?

**Answer:**
A Dockerfile contains instructions to build a Docker image.

Example:

```dockerfile
FROM node:22

WORKDIR /app

COPY . .

RUN npm install

CMD ["npm", "start"]
```

---

## 11. What does `docker build` do?

**Answer:**
Creates a Docker image from a Dockerfile.

---

## 12. What does `docker run` do?

**Answer:**
Creates and starts a container from an image.

---

## 13. Why use Docker?

**Answer:**

* Same environment everywhere
* Easy deployment
* No dependency conflicts
* Lightweight compared to virtual machines

---

## 14. What is Docker Compose?

**Answer:**
Docker Compose runs multiple containers together using one configuration file.

Example:

* Backend
* Database
* Redis

All started with:

```
docker compose up
```

---

## 15. Why use Docker Compose?

**Answer:**
Instead of starting containers one by one, it starts all services together.

---

## 16. What is Nginx?

**Answer:**
Nginx is a web server and reverse proxy used to serve websites and forward requests to backend servers.

---

## 17. Why do we need Nginx?

**Answer:**
Because it can:

* Serve static files
* Reverse proxy requests
* Handle HTTPS
* Load balance traffic
* Improve performance

---

## 18. What is a Reverse Proxy?

**Answer:**
A reverse proxy receives client requests and forwards them to the appropriate backend server.

```
Client
   ↓
Nginx
   ↓
Node.js
```

---

## 19. Why not expose the Node.js server directly?

**Answer:**
Because Nginx is faster for handling static files, HTTPS, and multiple client connections.

---

## 20. What is a Docker Volume?

**Answer:**
A Docker volume stores data outside the container so it isn't lost when the container is removed.

Useful for databases.

---

## 21. What is a Port Mapping?

**Answer:**
Maps a container's port to the host machine.

Example:

```
-p 3000:3000
```

Host → Container

---

## 22. What is an Environment Variable?

**Answer:**
A variable used to store configuration like:

* Database URL
* API Keys
* JWT Secret

Instead of hardcoding them.

---

## 23. What happens in a typical deployment pipeline?

**Answer:**

1. Push code to GitHub
2. GitHub Actions runs tests
3. Build Docker image
4. Push image to a registry (e.g., Docker Hub)
5. Server pulls the image
6. Run the new container

---

## 24. What is Docker Hub?

**Answer:**
Docker Hub is an online registry where Docker images are stored and shared.

---

## 25. Explain your deployment process.

**Answer:**
"I push code to GitHub. GitHub Actions builds and tests the project. If successful, it builds a Docker image and pushes it to Docker Hub. My server then pulls the latest image and starts a new container using Docker Compose. Nginx sits in front of the application and forwards incoming requests to the backend."

---
This is a very solid beginner-to-intermediate DevOps interview sheet. I'd say it's about **90–95% complete** for a typical Full Stack Developer interview.

The only important topics I'd add are:

### 26. What is a Container Registry?

**Answer:**
A container registry stores Docker images. Developers push images to the registry, and servers pull them for deployment.

Examples:

* Docker Hub
* GitHub Container Registry (GHCR)
* Amazon ECR

---

### 27. What is the difference between a Virtual Machine and a Docker Container?

| Virtual Machine     | Docker Container    |
| ------------------- | ------------------- |
| Includes full OS    | Shares host OS      |
| Heavier             | Lightweight         |
| Slower startup      | Starts in seconds   |
| More resource usage | Less resource usage |

---

### 28. What is a Health Check?

**Answer:**
A health check verifies whether an application is running correctly. If it fails, Docker or an orchestrator can restart the container.

---

### 29. What is HTTPS?

**Answer:**
HTTPS is HTTP secured with SSL/TLS encryption. It protects data exchanged between the client and the server.

---

### 30. What is SSL/TLS?

**Answer:**
SSL/TLS encrypts communication between clients and servers, making data secure during transmission.

---

### 31. What is a `.env` file?

**Answer:**
A `.env` file stores environment variables such as database URLs, API keys, and secrets, keeping sensitive information out of the source code.

---

### 32. What is `docker exec`?

**Answer:**
Runs a command inside a running container.

Example:

```bash
docker exec -it my-container sh
```

---

### 33. What is `docker logs`?

**Answer:**
Displays logs from a running container, useful for debugging.

Example:

```bash
docker logs my-container
```

---

### 34. What is the difference between `EXPOSE` and `-p`?

**Answer:**

* `EXPOSE` documents which port the container listens on.
* `-p` actually maps the container port to the host.

---

### 35. What is Zero Downtime Deployment?

**Answer:**
A deployment strategy where users continue accessing the application while a new version is deployed, minimizing or eliminating service interruption.

---
--- 

### What is Docker Networking?

**Answer:**
Docker networking allows containers to communicate with each other over a virtual network.

Example:

```
Frontend
     │
     ▼
Backend
     │
     ▼
PostgreSQL
```

With Docker Compose, services can communicate using their **service names**.

Example:

```yaml
services:
  backend:
  postgres:
```

The backend connects using:

```
DATABASE_URL=postgres://user:password@postgres:5432/mydb
```

Here, `postgres` is the service name—not `localhost`.


---
--- 

# Bonus Commands

```bash
# Build image
docker build -t my-app .

# Run container
docker run -p 3000:3000 my-app

# List containers
docker ps

# Stop container
docker stop <container-id>

# Remove container
docker rm <container-id>

# List images
docker images

# Remove image
docker rmi <image-id>

# Start all compose services
docker compose up

# Stop compose services
docker compose down

# View logs
docker compose logs

# Rebuild and start
docker compose up --build
```
