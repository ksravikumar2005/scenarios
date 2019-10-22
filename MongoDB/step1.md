<<<<<<< HEAD
For the Impatient:

To quickly get a single instance of the MongoDB up and Running, follow the steps below.

Step 1: Create a directory on the Docker Host and Change the ownership to match the uid and gid of the mongodb user inside the container. This step is optional and is needed only to persist the mongodb data on the docker host.

mkdir -p /data/db; chown -R 1000:1000 /data/db

Step 2: Run a prebuilt docker image for mongodb from docker hub which uses the host volume created in step 1 and exposing the port 27017 on the host which maps to the port 27017 on the docker container.

docker run -d -v /data/db:/data/db -p 27017:27017 ksravikumar2005/mongodb:latest

=======
For the Impatient:

To quickly get a single instance of the MongoDB up and Running,  follow the steps below.

Step 1: Create a directory on the Docker Host and Change the ownership to match the uid and gid of the mongodb user inside the container. This step is optional and is needed only to persist the mongodb data on the docker host.

mkdir -p /data/db; chown -R 1000:1000 /data/db

Step 2: Run a prebuilt docker image for mongodb from docker hub which uses the host volume created in step 1 and exposing the port 27017 on the host which maps to the port 27017 on the docker container.

docker run -d -v /data/db:/data/db -p 27017:27017 ksravikumar2005/mongodb:latest

>>>>>>> 0f9ad92dee8b4235fecc10067e5574857a3c255e
