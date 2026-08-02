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
