# Docker-and-kuberneties
material for docker and kuberneties

systemctl status docker //get the status of docker engine service
docker build -t 1stday:v1 .  //build docker -t is tag to name and " . " is for the location where to find the files
docker images // gives images list
docker run -p 8081:80 1stday:v1  // run the container
docker ps  // live containers list
docker stop <container name>  //to stop the container
docker run -d -p 8081:80 1stday:v1  // run the container without having the logs on the terminal
docker exec -it <container name> sh  // will help you login in container and then access the shell
docker stop <container name>  // stop the container
docker rm <container name>   // remove the container