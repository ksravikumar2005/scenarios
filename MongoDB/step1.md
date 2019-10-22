For the Impatient:

To quickly get a single instance of the MongoDB up and Running, follow the steps below.

Step 1: Create a directory on the Docker Host and Change the ownership to match the uid and gid of the mongodb user inside the container. This step is optional and is needed only to persist the mongodb data on the docker host.

`mkdir -p /data/db; chown -R 1000:1000 /data/db`{{execute}}

Step 2: Run a prebuilt docker image for mongodb from docker hub which uses the host volume created in step 1 and exposing the port 27017 on the host which maps to the port 27017 on the docker container.

`docker run -d -v /data/db:/data/db -p 27017:27017 --name=myfirstmongo ksravikumar2005/mongodb:latest`{{execute}}

Step 3: Check the status of the running container

`docker ps`{{execute}}

Step 4: Check the logs to confirm the mongo process is up and running

`docker logs myfirstmongo`{{execute}}

Step 5: Check the logs on the docker host volume to confirm the volume mapping

`ls -l /data/db`{{execute}}

Step 6: Login to the container shell and execute mongo OR execute the below command to directly drop to mongo shell

`docker exec -it myfirstmongo mongo`{{execute}}

Step 7: Type "show databases" to view all the default databases

Step 8: type "exit" to exit the mongo shell and the container

Step 9: Stop the container using the command

`docker stop myfirstmongo && docker rm myfirstmongo`{{execute}}

Step 10: You have successfully deployed MongoDB on Docker in less than 5 minutes!

See you in the next scenario! 
