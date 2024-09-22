# Docker Commands

## Delete All Images
docker rmi $(docker images -q)

## Stop All Containers
docker stop $(docker ps -a -q)

## Run Docker Compose (detached)
docker-compose up -d

## Rebuild Docker Compose After Changing Files of Project (detached)
docker-compose up -d --build

## Stop and Remove All Compose Containers
docker-compose down

## Logs of Particular Container ID/Name
docker logs 94027a507567

## All Containers (Stopped and Active)
docker ps -a

## All Active Containers
docker ps

## Delete All Stopped Containers
docker container prune

## Invoke Process in Running Container (sh/bash/powershell) (Special - name of container)
docker exec -it Special sh

## Create and Run Container from Image `my-file-writer`
docker run -it --name Special my-file-writer

## Create Image (path: `.`)
docker build . -t my-file-writer

## Show All Images
docker images

## Run Container with Specific Name
docker run -it --name calendar5 my-calendar:2.0.0

## Run Docker Container with Port and Volume Remappings (or `${PWD}`)
docker run -d -v C:\New\docker\nginx:/usr/share/nginx/html -p 8181:80 --name M1 nginx

## Inspect Container
docker inspect M1

## Delete all unused Docker volumes
docker volume prune
