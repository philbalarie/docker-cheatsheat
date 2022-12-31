# Doc for Docker

## Start docker container based on an image
```console
$ docker container run --publish 80:80 --detach nginx
```
Opened port 80 on the host IP
Routes that traffic to the container IP, port 80

### List all containers

```console
$ docker container ls
```

### Stop container
```console
$ docker container stop ID
```
