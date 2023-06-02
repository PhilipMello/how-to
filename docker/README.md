# HOW-TO DOCKER

### Login in Docker CLI

```
docker login
```

### Download Docker images

```
docker pull "name-of-image"

Example: docker pull ubuntu
```

### Show Docker images

```
docker image ls
```

### Remove one or more images

```
docker image rm "name-of-image"

Example: docker image rm ubuntu
```

### Remove unused images (WARNING, THIS COMMAND WILL REMOVE ALL DOCKER IMAGES ON COMPUTER)

```
docker image prune
```

### Upload Docker image to DockerHub

```
docker push "name-of-image"

Example: docker push ubuntu
```

### Inspect Docker image

```
docker image inspect "name-of-image"

Exemple: docker image inspect ubuntu

```
