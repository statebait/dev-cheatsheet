# Docker Commands

### 1. Create an image:

```bash
# Inside the folder with Dockerfile
docker build -t <image_name> .
```

### 2. List your images:

```bash
docker image ls
```

### 3. Delete a specific image:

```bash
docker image rm [image name]
```

### 4. Delete all existing images:

```bash
docker image rm $(docker images -a -q)
```

### 5. List all existing containers (running and not running):

```bash
docker ps -a
```

### 6. Change a container name at running time:

```bash
docker run --name [container name] [image name]
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

```bash
# In the repository with docker-compose.yml
docker-compose up
```

### 14. Deleting all untagged(dangling) images:

```bash
docker rmi $(docker images -f “dangling=true” -q)
```
