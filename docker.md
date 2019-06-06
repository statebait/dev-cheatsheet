# Docker Commands

### 1. List your images:

```bash
docker image ls
```

### 2. Delete a specific image:

```bash
docker image rm [image name]
```

### 3. Delete all existing images:

```bash
docker image rm $(docker images -a -q)
```

### 4. List all existing containers (running and not running):

```bash
docker ps -a
```

### 5. Change a container name at running time:

```bash
docker run --name [container name] [image name]
```

### 6. Stop a specific container:

```bash
docker stop [container name]
```

### 7. Stop all running containers:

```bash
docker stop $(docker ps -a -q)
```

### 8. Delete a specific container (only if stopped):

```bash
docker rm [container name]
```

### 9. Delete all containers (only if stopped):

```bash
docker rm $(docker ps -a -q)
```

### 10. Display logs of a container:

```bash
docker logs [container name]
```

### 11. Build using docker compose:

```bash
# In the repository with docker-compose.yml
docker-compose build
```

### 12. Starting containers using docker compose:

```bash
# In the repository with docker-compose.yml
docker-compose up
```
