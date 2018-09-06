# Docker cheatsheet
Docker installation and common commands
---

Build a Docker image from a docker file 
```
cd /Desktop/docker1

c..\Desktop\docker1>  docker build -t hello-world .

  -t followed by *imagename*
  . is location of Dockerfile

```


Create and run a container based on the image you created 
```
c..\Desktop\docker1>  docker run -p 80:80 hello-world

  host port : container port
  
http://localhost

```


List running docker containers 
```
docker ps -a

  -a = all
  -l = latest
  -s = by size
```

View docker logs -- especially useful if a container will not start and has a status of Exit(1)
``` 
docker logs *container ID or name*
```

Stop a docker container
```
docker stop *container ID or name*
```

Remove a docker container
```
docker rm *container ID or name*
```

List docker images
```
docker images -a
  -a = all
```

Remove docker images
```
# removes a single image
docker rmi *image id or name*

# removes all images
docker rmi $(docker images -a -q)  
```
