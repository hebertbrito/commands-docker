# COMMANDS DOCKER
## *Here are some commands that are useful in your day using docker, you can also replace the word "docker" with "docker-compose" some commands may work*

LINE COMMAND | ACTIONS
------------ | -------------
docker ps | list he containers 
docker ps --all	 | lists containers that have been executed and are no longer active at this time.
docker run -it **[image] [comando]** | execute the image and execute the command informing inside the container
docker start **[image]** | starting image
ocker run -it --rm **[image] [comando]** | every time the image is executed and at the end the image is deleted from the machine/cache
docker run -p 8080:80 nginx | local access from my machine from port 8080 to nginx port 80
docker run -d -p 8080:80 | the -d command lets you run an image that maintains the process and exit inside the container without terminating it
docker stop **[idimage]** | stopping execution images
docker rm **[idimage]** or -f | remove the containers and using the -f force the request.
docker exec **[nameimage] [comando]** | execute a command inside the container that is already in process
docker system prune | clear all docker space
docker build -t **[dockerhubname]/[yournameimage:tag]** . or **[path]** | builds an image based on naming to upload to the docker hub
docker rm $(docker ps -a -q) -f | removes all downloaded images based on ids
docker run -d --name nginx -p 8080:80 --mount tipe=bind,source=[path]/target=[path] | share files with container and local machine
**http://host.docker.internal:[port]** | accesses a local port of the user's machine and not of the container, this inside an application inside another container/process

## NOMENCLATURES

> LINE COMMAND | DESCRIPTION
------------ | -------------
-i | iterative mode
-t or tty| allows typing commands
--name | allow name the image of your choice
-mount | allow to pass a bind into the container

## COMMANDS UBUNTU
    apt-get update     -> updates the apt-get
    vim                -> apt-get install vim  -> install an editor on OS or VM
    $(pwd)             -> path of current directory that you are



## VIM
    i                 -> allow to edit the open file
    :+w               -> save modification
    :q                -> exit vim


## ENTRYPOINT vs CMD
> **Entrypoint is a fixed value that cannot be changed at runtime, it is a dynamic command that can be changed in the image execution process.**