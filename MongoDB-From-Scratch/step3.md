In this step, we will be running the image we built in the previous step.

Step 1: Create a directory on the Docker Host and Change the ownership to match the uid and gid of the mongodb user inside the container. This step is optional and is needed only to persist the mongodb data on the docker host.

`mkdir -p /data/db; chown -R 1000:1000 /data/db`{{execute}}

Step 2: Run a prebuilt docker image for mongodb from docker hub which uses the host volume created in step 1 and exposing the port 27017 on the host which maps to the port 27017 on the docker container.

`docker run -d -v /data/db:/data/db -p 27017:27017 --name=myfirstmongo mongodb:latest`{{execute}}

Step 3: Check the status of the running container

`docker ps`{{execute}}
