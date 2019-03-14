# Docker_Matomo_MySQL

Docker: 18.09.3, build 774a1f4

MySQL: 8.0

Matomo: 3.8.1

## Docker

https://github.com/Huioqy/Docker_Start_Up

* Common Ops
  
    docker ps -a
    
    docker stop $(docker ps -q) & docker rm $(docker ps -aq)
    
    docker rmi [OPTIONS] IMAGE [IMAGE...]
    
    docker run [OPTIONS] IMAGE [COMMAND] [ARG...] 
    
    [OPTIONS]: -d       Run container in background and print container ID
    
               -e       Set environment variables
               
               --name		Assign a name to the container
               
               --link		Add link to another container
               
               -p		    Publish a container’s port(s) to the host

## MySQL--Docker

https://hub.docker.com/_/mysql?tab=description

     docker run --name huioqy-mysql -e MYSQL_ROOT_PASSWORD=123456789 -d mysql:8 

## Matomo--Docker

https://github.com/matomo-org/docker

    docker run -d --link huioqy-mysql:db -p 4000:80 matomo:3.8.1
