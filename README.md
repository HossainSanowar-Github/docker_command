# docker_command

https://hub.docker.com/r/docker/getting-started

# Create Docker Command: 
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


docker build -t <image_name>:<tagname> #build image; image name for docker must be lowercase
docker build -t ml_project .
docker images #to show the list of docker images
docker run -p 5000:80 -e PORT=5000 <image id> #run docker image
docker run -d -p 8000:8000 -e PORT=8000 52879125fe4b #running docker images and working
docker ps #check running container status
docker ps -a # all project running container status
docker stop container_id #stop container
docker stop 0cc6448810ee


# Docker Images
