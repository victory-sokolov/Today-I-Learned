# Stop/Remove all containers

```
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
```

```ps``` - lists containers

```-a``` - all

```-q``` - Only display numeric IDs