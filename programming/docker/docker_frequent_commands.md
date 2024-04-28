#### image
- docker images - list all images
- docker build -t <image-name> <path-to-dockerfile> - build image
	- '-t' - output to terminal
- docker rmi <image-id> - remove image (note: no containers for this image should be running)
- docker rmi $(docker images -q) - remove all images
- docker tag <currentimage>:<tag> <repository-name>/<image-name>:<tag> - create tag
- docker push <repository-name>/<image-name>:<tag>
- docker commit <container-id> <repository-name>/<image-name>:<tag>
- docker pull <repository-name>/<image-name>:<tag>
#### container
- docker ps - list containers
	- '-a' - all
- docker run -itd --name <container-name> -p <host-port>:<port-in-container> <image-name:tag> - run the container from the image
	- '-d' - represents (detached mode), note that if you don't run this in detached mode, the life of the container will be the life of the terminal in which you are executing it.
	- '-p' -represents the host-port to container-port mapping, if you substitute it with '-P' you will get a random port allocated by docker
	- '--name' - represents the name of the container
- docker logs -ft <container-id/name> - container logs
	- '-f' - follow ( tail the logs)
- docker start <container-id/name> - start existing container
- docker stop <container-id/name> - stop existing container
- docker rm <container-id/name> - remove existing container
	- '-f' - force
- docker rm $(docker ps -a -q) - remove all containers
#### general
- docker inspect <image-id> | <container-id> - inspect image or container
- docker exec -it <container-id> /bin/bash  - execute bash in container