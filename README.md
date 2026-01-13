## 🚀 Quick start

```sh
# Copy the example environment file, on the root level
cp .env.example .env

# Copy the example environment file, for each service
cd services/<SERVICE_NAME>
cp .env.example .env

# First, build the custom Node.js 22 Docker image
docker build -t custom-node:22 ./docker/node-base # custom-node:22

# Then, start the application with Docker Compose
docker compose up --build
```

## 🛠️ Architecture

### Ports binding

| Service         | Port |
| --------------- | ---- |
| Service A       | 3001 |
| Service B       | 3002 |
