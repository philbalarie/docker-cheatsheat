# Doc for Docker

## Containers

### Start docker container based on an image
```console
$ docker container run --rm --publish 80:80 --detach --name webhost --network network_name nginx
```
Opened port 80 on the host IP
Routes that traffic to the container IP, port 80

### List all containers

```console
$ docker container ls
```

### Stop container
```console
$ docker container stop ID/NAME
```

### Get log from container
```console
$ docker logs ID/NAME
```

### Get process inside a container
```console
$ docker container top ID/NAME
```

### Remove containers
```console
$ docker container rm ID/NAME
```
### Start a new container interactively
```console
$ docker container run -it ID/NAME bash
```

### Run additional command in additional container
```console
$ docker container exec -it 
```

### Start existing container (before with run command)
```console
$ docker container start -ai ID/NAME 
```

### Show ports of container
```console
$ docker container port ID/NAME
```

### Inspect container
```console
$ docker container inspect ID/NAME --format '{{ .NetworkSettings.IPAddress }}' ID/NAME
```

## Images

### List docker images on system
```console
$ docker image ls
```

### Get image history
```console
$ docker history NAME
```

### Build image
```console
$ docker image build -t custom_nginx .
```

## Network

### List docker networks
```console
$ docker network ls
```

### Inspect a network
```console
$ docker network inspect ID/NAME
```

### Create a network
```console
$ docker network create NAME
```

### Attach a network to container
```console
$ docker network connect
```

### Detach a network from container
```console
$ docker network disconnect
```

## Prune

### Clean up just "dangling" images
```console
$ docker image prune
```

### Remove all images you're not using
```console
$ docker image prune -a
```

### Clean up everyting
```console
$ docker system prune
```