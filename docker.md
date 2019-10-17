# Docker Commands

### 1. Create an image:

```bash
# Inside the folder with Dockerfile
docker build -t <image_name> .
```

### 2. Run an image:

- Regular:

  ```bash
  docker run <image_name>
  ```

- Binding a port at run time:

  ```bash
  docker run -p <container_port>:<host_port> <image_name>
  ```

- Setting a name for the container at run time:

  ```bash
  docker run --name <container name> <image name>
  ```

- Running a container in the background (detached):

  ```bash
  docker run -d <image_name>
  ```

### 3. List your images:

```bash
docker image ls
```

### 4. Delete a specific image:

```bash
docker image rm [image name]
```

### 5. Delete all existing images:

```bash
docker image rm $(docker images -a -q)
```

### 6. List all existing containers (running and not running):

```bash
docker ps -a
```

### 7. Stop a specific container:

```bash
docker stop [container name]
```

### 8. Stop all running containers:

```bash
docker stop $(docker ps -a -q)
```

### 9. Delete a specific container (only if stopped):

```bash
docker rm [container name]
```

### 10. Delete all containers (only if stopped):

```bash
docker rm $(docker ps -a -q)
```

### 11. Display logs of a container:

```bash
docker logs [container name]
```

### 12. Build using docker compose:

```bash
# In the repository with docker-compose.yml
docker-compose build
```

### 13. Starting containers using docker compose:

- Regular:

  ```bash
  # In the repository with docker-compose.yml
  docker-compose up
  ```

- Background (Detached mode):

  ```bash
  # In the repository with docker-compose.yml
  docker-compose up -d
  ```

### 14. Deleting all untagged(dangling) images:

```bash
docker rmi $(docker images -f “dangling=true” -q)
```
