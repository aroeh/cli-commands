# Docker
Additional details can be found on the Docker website at [Reference Documentation](https://docs.docker.com/reference/)

## Search

Searches for an image on the docker hub repository using the provided term

`docker search [options] <term>`

```
docker search redis
```


## Images

### List all images

List all images on the local workstation

`docker images`

```
docker images
```

### Build

Create a new image using inline cli parameters or a docker file

`docker build -t <name> -f <dockerfile> <context>`

```
docker build -t my_image -f Dockerfile .
```

> The context is key since that instructs the docker file and docker daemon on the source path for running commands
> A context using only a period "." represents the current directory


### Remove image

Deletes a single image

`docker rm <image>`

```
docker rm my_image
```

> Images can also be deleted by a specific tag

`docker rm <image>:<tag>`

```
docker rm my_image:latest
```

### Force Remove Multiple Images

Removes all images regardless of use in containers or dependencies.  This can be useful when just needing to delete everything

`docker rmi $(docker images -q) -f`

### Prune Images

Removes images that are not being used by any containers

`docker image prune [options]`

```
docker image prune -a
```

> -a on this command removes all dangling images


## Containers

### List containers

List running containers on the environment

`docker ps [options]`

```
docker ps
```

> To List all containers add the -a parameter

```
docker ps -a
```

### Create

Creates a new container using the specified image

`docker create --name <container-name> <image-name>`

```
docker create --name my_container my_image
```

### Start

Starts the container to run and consume resources

`docker start <container>`

```
docker start my_container
```

### Stop

Stops the container

`docker stop <container>`

```
docker stop my_container
```

### Delete

Delete a container and remove it

`docker rm [options] <container>`

```
docker rm my_container
```

> Containers that are running will not be deleted.  To forcefully delete a running container add -f

`docker rm -f <container>`

```
docker rm -f my_container
```

> All containers can be deleted in the same command

```
docker rm $(docker ps -a -q)
```

### Run

Builds and runs a container using provided parameters

`docker run [options] <image>`

```
docker run -d -p 5000:80 -e "ASPNETCORE_ENVIRONMENT=Development" --name my_container my_image
```

> -d runs the container in detached mode.  Good if you do not want to debug
> -p adds a port to the container for networking
> -e adds an environment variable to the container.  Multiple environment variables can be addded.  -e var1 -e var2
> --name sets the container name

### Logs

Retrieve logs from the container instance

`docker logs [options] [container]`

```
docker logs -f my_container
```

> If running on a network, the full service name should be used.

## Networking

## Exec

# Docker Compose