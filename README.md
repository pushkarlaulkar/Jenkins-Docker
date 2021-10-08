# Jenkins-Docker
Jenkins Docker images of different OS

This repository contains Jenkins image of different OS.

To run the image with volume mounting enter below command

Alpine OS
-------

docker run -d --name [name of the container] -v jenkins-data:/var/lib/jenkins -p 8080:8080 --restart always jenkins:alpine.

This will create a docker volume "jenkins-data" which will store all the Jenkins data of the container, and port 8080 on the host is mapped to port 8080 on the container. Also adding the always restart policy to make sure the container restarts automatically if there is an issue with docker daemon.

Once the container is up and running enter below URL to start using Jenkins

ip-address-of-the-host:8080
