-DELETE ALL IMAGES
docker rmi $(docker images -q) 

-STOP ALL CONTAINERS
docker stop $(docker ps -a -q)

-RUN DOCKER COMPOSE (detached)
docker-compose up -d

-REBUILD DOCKER COMPOSE AFTER CHANGE FILES OF PROJECT (detached)
docker-compose up -d --build

-STOP AND REMOVE ALL COMPOSE CONTAINERS
docker-compose down

-LOGS OF PARTICULAR CONTAINER ID/NAME
docker logs 94027a507567

-ALL CONTAINERS SOPPED AND ACTIVE
docker ps -a

-ALL ACTIVE CONTAINERS
docker ps

-DELETE ALL STOPPED CONTAINERS
docker container prune

-INVOKE PROCESS IN RUNNING CONTAINER (sh/bash/powershell) (Special - name of container)
docker exec -it Special sh

-CREATE AND RUN CONTAINER FROM IMAGE my-file-writer
docker run -it --name Special  my-file-writer

-CREATE IMAGE (. - path) 
docker build . -t my-file-writer

-SHOW ALL IMAGES
docker images

-RUN CONTAINER WITH SPECIFIC NAME
docker run -it  --name calendar5  my-calendar:2.0.0

-RUN DOCKER CONTAINER WITH PORT AND VOLUME REMAPPINGS ( or ${PWD} )
docker run -d -v C:\New\docker\nginx:/usr/share/nginx/html  -p 8181:80 --name M1 nginx

-INSPECT CONTAINER
docker inspect M1
