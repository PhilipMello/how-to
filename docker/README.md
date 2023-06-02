# HOW-TO DOCKER

## Docker Images

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
or
docker images
```

### Remove one or more images

```
docker image rm "name-of-image"

Example: docker image rm ubuntu

or
docker rmi "name-of-image"

Example: docker rmi ubuntu
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

### Build Docker image

```
docker image build "name-of-image"

Example: docker image build ubuntu
```

## Docker Container

### List all Docker containers running

```
docker container ps
or
docker ps
```

### List all Docker containers running

```
docker container ps -a
or
docker ps -a
or
docker ps -all
```

### Stop Docker contaienr

```
docker container stop "id-of-container"
or
docker container stop "name-of-container"
or

docker stop "id-of-container"
or
docker stop "name-of-container"
```

### Copy files to Docker container

```
docker container cp

Example: docker container cp file.txt abcdocker889938:/usr/share
```
