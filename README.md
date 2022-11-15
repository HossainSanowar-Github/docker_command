# docker_command

https://dockerlabs.collabnix.com/docker/cheatsheet/

https://www.docker.com/

https://hub.docker.com/r/docker/getting-started

https://labs.play-with-docker.com/

##docker pull image
```
##Example 1:
docker pull docker/getting-started
docker images
docker run -d -p 80:80 docker/getting-started #here -d:ditach mode, -p: prefix, 80: local host port, 80: container port
docker ps #show the docker status
Example 2: 
docker pull redis
docker images
```
## Create Docker File
```
1. Create a Dockerfile
FROM
COPY
WORKDIR
RUN
CMD
2. Build the docker image; `.` means current directory
docker build -t <image-name> .
docker images
##run docker image; here -d: detach mode, -p: assign port, 5000: local host port, 8000: container port
docker run -d -p 5000:8000 welcome-app
```
```
#download python:3.7 from Docker Hub
#internally linux base image is downloaded
FROM python:3.7
##copy each and every from local folder, put inside the `docker app` folder; that means source is `.` and destination is `app`
COPY . /app
#get working directory
WORKDIR /app
#run all the required libraries
RUN pip install -r requirements.txt
#run python file like `python app.py`
CMD ["python","app.py"]
```
##remove docker images
```
docker ps
docker stop <image id>
docker images
docker rmi -f <image name>
```
## docker images push to docker Hub
```
docker build -t sanowarhossain/welcome-app .
docker push sanowarhossain/welcome:latest #here, latest: version
```


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
