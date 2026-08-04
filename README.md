# Docker-and-kuberneties
Author: Hasmukh<br>
These are my notes taken during the learning session, may contain info but unable recollect what it was. Please google it if details are forgotten.

## Short notes for docker and kuberneties

[ systemctl status docker ] - get the status of docker engine service

[ docker build -t 1stday:v1 . ] - build docker -t is tag to name and " . " is for the location where to find the files

[ docker images ] - gives images list

[ docker run -p 8081:80 1stday:v1 ] - create and run the container

[ docker ps ] - live containers list

[ docker stop container name ] - to stop the container

[ docker run -d -p 8081:80 1stday:v1 ] - run the container without having the logs on the terminal

[ docker exec -it container name sh ] - will help you login in container and then access the shell

[ docker stop container name ]  - stop the container

[ docker rm container name ]  - remove the container

[ curl -s http://169.254.169.254/latest/meta-data/instance-type ] - Details of EC2 instance

[ docker tag day2:v1 hmjain/docker_day2:v1 ] - Rename the image in docker

[ docker push hmjain/docker_day2:v1 ] - push the image to docker hub

[ docker pull hmjain/docker_day2:v1 ] - pull docker image from docker repo. you should have credentials to push

[ docker system prune ] - clears cached data or images unused, same can be done with volume too.

[ docker system prune -f ] - Forceful prune

[ docker run -it --name test-container ubuntu bash ] - login in to container

[ docket run -it --rm -v my-docker-volume:/data ubuntu bash] - this will create a volume in local my-dokcer-volume and data from "data" folder of the docker will be copied to new volume. --rm is used to kill the container after exit. Volumes are of two types Named volume and Unnamed volume. Named volumes are created by user with meaningful name.<br>* When prune is done this data will stay but unnamed volume will be cleared.

[ docker volume ls ] - gives list of volume

[ docket run -it --rm -v my-docker-v /data -v /temp ubuntu bash ] - this will create unnamed volumes

[ docker inspect volume_name ] - gives details of volume, same can be done using container image name

[ docker run -it --tmpfs /app:rw,size=500M busybox sh ] - Launches a “busybox” container with 500Mb memory ( reserved in RAM, to be used on demand, not immediately). tmpfs doesn't consume RAM until you write to it. No additional volume created for tmpfs storage. Temporary volume we can check inside container using “df -h” command.

[ docker compose up -d ] - runs all the images, default docker-compose.yml/compose.yml and deploy it on current folder name

[ docker compose -p hasmukh_project_prod up -d ] - default docker-compose.yml and deploy it in custom project

[ docker compose -f docker-compose_prod.yml -p hasmukh_project_prod up -d ] - deploy custom docker-compose.yml and deploy it on custom project

[ docker compose down ] - shutdown all the images

[ docker compose down -v ] - shutdown all the images and clean the volume

[ docker compose -p project-name down -v ] - shutdown the specific project and clean the volume

1# docker compose up -d  : Default docker-compose.yml/compose.yml and deploy it in current-folder-name project<br>

NAME                     STATUS              CONFIG FILES<br>
labuser                  running(2)          /home/labuser/docker-compose.yml<br>
 
2# docker compose -p saurabh_project_prod up -d  : Default docker-compose.yml/compose.yml and deploy it in custom project<br>

NAME                     STATUS              CONFIG FILES<br>
saurabh_project_prod_2   running(1)          /home/labuser/docker-compose.yml<br>
 
3# docker compose -f  docker-compose_prod.yml  -p saurabh_project_prod up -d : Deploy custom docker-compose-file and deploy it in custom project <br>

NAME                     STATUS              CONFIG FILES<br>
saurabh_project_prod     running(1)          /home/labuser/docker-compose_prod.yml<br>

[ docker service create --name nginx-app --replicas 2 -p 8081:80 nginx:latest ] - this will create multiple nodes in a container

[ docker service ls ] - live docker services

[ docker service ps ] - list of tasks

[ docker service scale ngnix-app=1oo ] - this will create 100 replicas, in the system

[ docker ps | wc -1 ] - this will say total running services details

[ docker node ls ] - list of nodes

[ docker stack deploy -c stack.yml mystack ] - will create and run stack

[ docker stack ps mystack ] - gives list fo the containers in the stack

[ docker run -dit --name host_nginx --network host nginx ]
