In this step, lets see how to build a docker image 

Step 1: Note that at the minimum, the docker image tags should have and imagename:tag. 

An image tag like this: ksravikumar2005/mongodb:latest is an example of an image in hub.docker.com, Build your first image using the command below.

  `docker build -t mongodb:latest .`{{execute}}

This might take a few minutes as the Docker build process will download all CentOS base image and other dependencies listed in the Dockerfile.

Step 2: Verify built image using the command
  
   `docker image ls`{{execute}}

NOTE: This image is available locally and is not pushed to any Docker image repository. To push this image to a specific image repository, please follow the tag and push instructions specific to that repository.


