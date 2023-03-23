# Docker Compose

Docker compose enables working with multiple containers using a compose file.  This helps define a platform or ecosystem as code.  Full reference of commands see [Compose](https://docs.docker.com/compose/reference/)

## Build

Builds all services listed in the compose file

`docker-compose build`

```
docker-compose build
```

> To build a single service in the compose add the service name

```
docker-compose build my_service
```

## Up

Runs all services in the compose file

`docker-compose up`

```
docker-compose up
```

> To run the containers in detached mode add d to the command.  This helpful for performance and when you don't need or want to debug

```
docker-compose up -d
```


## Down

Stops all services in the compose file

`docker-compose down`

```
docker-compose down
```

> Sometimes you may also want to remove all containers and images.

```
docker-compose down --rmi 'all'
```
