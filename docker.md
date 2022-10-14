# Docker 

#### Docker is a software platform that allows you to build, test, and deploy applications quickly. Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime. Using Docker, you can quickly deploy and scale applications into any environment and know your code will run.

- Official website - [https://www.docker.com/](https://www.docker.com/)

- Documentation - [https://docs.docker.com/](https://docs.docker.com/)

## Build
Building an image from Dockerfile 
```sh
docker build -t app_name:1.0 .
```
List all images
```sh
docker images
```


## Run
Run docker image
```sh
docker run -p 8001:8001 -it  app_name:1.0
```

List all running containers
```sh
docker ps
```

Kill a running container

```sh
docker kill container_name/ container_id 
```

## Prune
```sh
docker system prune     # prune all docker resources
docker system prune -f  # prune all resources with force (without prompt)
```

## Attributes

- https://aws.amazon.com/docker/


