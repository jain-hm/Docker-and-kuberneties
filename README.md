# Docker-and-kuberneties
material for docker and kuberneties

systemctl status docker //get the status of docker engine service <br>  
docker build -t 1stday:v1 .  //build docker -t is tag to name and " . " is for the location where to find the files<br>  
docker images // gives images list  <br>
docker run -p 8081:80 1stday:v1  // run the container  <br>
docker ps  // live containers list  <br>
docker stop container name  //to stop the container  <br>
docker run -d -p 8081:80 1stday:v1  // run the container without having the logs on the terminal  <br>
docker exec -it container name sh  // will help you login in container and then access the shell  <br>
docker stop container name  // stop the container  <br>
docker rm container name   // remove the container  <br>