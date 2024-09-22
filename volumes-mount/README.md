# Volumes

- Volumes are easier to back up or migrate than bind mounts.
- You can manage volumes using Docker CLI commands or the Docker API.
- Volumes work on both Linux and Windows containers.
- Volumes can be more safely shared among multiple containers.
- Volume drivers let you store volumes on remote hosts or cloud providers, encrypt the contents of volumes, - or add other functionality.
- New volumes can have their content pre-populated by a container.
- Volumes on Docker Desktop have much higher performance than bind mounts from Mac and Windows hosts.


```
#Create a volume:
docker volume create my-vol
```


```
#List volumes:
docker volume ls
```

```
#Start a container with a volume
docker run -d \
  --name devtest \
  --mount source=myvol2,target=/app \
  nginx:latest
```