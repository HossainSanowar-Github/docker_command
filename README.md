# docker_command
Create Docker Command 
1. docker -v
2. docker --version
3. docker images #show the number of image; but show after stop
4. docker ps #show the status; don't show it after stop; find the container ID
5. docker ps -a
6. docker stop <container_ID>
7. docker image rm -f <image_id> # remove image 

* First need to stop container id and then remove image

Create docker image like docker/getting-started
1. docker run -d -p 80:80 docker/getting-started
2. http://127.0.0.1/tutorial/ #show in localhost

notice a few flags being used. Here's some more info on them:

-d - run the container in detached mode (in the background)
-p 80:80 - map port 80 of the host to port 80 in the container
docker/getting-started - the image to use
