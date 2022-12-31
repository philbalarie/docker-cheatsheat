# Doc for Docker

## Containers

### Start docker container based on an image
```console
$ docker container run --publish 80:80 --detach --name webhost nginx
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
$ docker container inspect --format '{{ .NetworkSettings.IPAddress }}' ID/NAME
```

## Images

### List docker images on system
```console
$ docker image ls
```

## Network

### List docker networks
```console
$ docker network ls
```

### Inspect a network
```console
$ docker network inspect
```

### Create a network
```console
$ docker network create --driver
```

### Attach a network to container
```console
$ docker network connect
```

### Detach a network from container
```console
$ docker network disconnect
```