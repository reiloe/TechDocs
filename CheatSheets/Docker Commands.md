# Docker Commands

### **Table of Contents**

1. [Docker Hub Commands](#docker-hub-commands)
2. [Image Operations](#image-operations)
3. [Container Operations](#container-operations)

### Docker Hub Commands

Docker Hub is a service provided by Docker for finding and sharing container images.

Login to Docker Hub

```bash
docker login -u <username>
```

Search Docker Hub for an image

```bash
docker search <image_name>
```

Pull an image from Docker Hub

```bash
docker pull <image_name>
```

Publish an image to Docker Hub

```bash
docker push <username>/<image_name>
```


### Image Operations

List local images

```bash
docker images
```

Build an Image (from a Dockerfile)

```bash
docker build .
```

*The . (dot) points to the location of the Dockerfile (in this case, current directory)*

or

```bash
docker build -t <image_name> .
```
*The -t  parameter is used to tag (name) the image*


Build an Image (from a Dockerfile) without the Cache

```bash
docker build -t <image_name> . -no-cache
```

Delete an Image

```bash
docker rmi <image_name>
```

Remove all unused images

```bash
docker image prune
```


### Container Operations

Show all running container

```bash
docker ps
```

Show all container (running and stopped)

```bash
docker ps -a
```

Run a container (in foreground)

```bash
docker run <image_name>
```

Run a container (in background)

```bash
docker run -d <image_name>
```

Run a container with a custom name

```bash 
docker run --name myCustomContainerName <image_name>
```

Run a container and publish a container port to the host

```bash
docker run -p <host_port>:<container_port> <image_name>
```

Start/Stop an existing container

```bash
docker start <container_name> (or <container_id>)

docker stop <container_name> (or <container_id>)
```

Open a shell inside a running container

```bash
docker exec -it <container_name> sh
```

Fetch and follow the logs of a container

```bash
docker logs -f <container_name> (or <container_id>)
```

Inspect a running container

```bash
docker inspect <container_name> (or <container_id>)
```

