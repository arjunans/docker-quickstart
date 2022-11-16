## How to pull image from dockerhub and run it in the docker container
 - docker pull hello-world
 - docker run hello-world

## How to find all downloaded images
 - docker images

## How to find all running containers
 - docker ps

## How to find all running/stopped containers
 - docker ps -a

## How to run an image in a detached mode (Docker container runs in the background of your terminal)
 - docker run -d redis

## How to start container
- docker start <id-of-container>

## How to stop container
docker stop <id-of-container>

## How to do port mapping between host and container (d -detached mode, p - port)
- docker run -dp 3001:80 bootstrap-static-page

## How to remove container
- docker rm -f <name-of-container/containerid> [f- force delete](for example: docker rm -f mongo-db)

## How to create network 
- docker network create <network-name> (for exampleL docker network create db-network)

## How to delete network in docker container
- docker network rm <network-name> 

## How to delete all running containers in one command? (Note:- Be careful while using this command in development)
 - docker rm $(docker ps -aq) - This command may not run properly when you run it from cmd prompt. use powershell either in windows. No issues with linux.

## How to delete all downloaded images in one command? (Note:- Be careful while using this command in development)
docker rmi $(docker images -q) - This command may not run properly when you run it from cmd prompt. use powershell either in windows. No issues with linux

## How to stop all running containers in one command? (Note:- Be careful while using this command in development)
 - docker stop $(docker ps -aq) - This command may not run properly when you run it from cmd prompt. use powershell either in windows. No issues with linux