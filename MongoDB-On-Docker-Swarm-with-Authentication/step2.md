# Running Mongo as a service:
With Docker Swarm, the mongodb can be deployed as a service and having multiple nodes will ensure the service availability has minimal impact. This demo is only meant to highlight the features of Docker swarm to maintain service availability.

Download the required stack files for running the docker swarm by cloning

`git clone https://github.com/ksravikumar2005/mongodb.git`{{execute HOST1}}

`cd mongodb`{{execute HOST1}}

View the contents of the mongo-stack.yml file and you will see 2 services (mongodb1 and mongodb2) defined.

`cat mongo-stack-with-auth.yml`{{execute HOST1}}

Deploy these services to the docker swarm using the command below

`docker stack deploy -c mongo-stack-with-auth.yml mongodb`{{execute HOST1}}

To view the staus of the deployed services, use the command

`docker stack ps mongodb`{{execute HOST1}}

Initiall, all the services will be seen in "Preparing.." state, Wait for a few seconds as the specified MongoDB image is being downloaded to each node.

Try again: 

`docker stack ps mongodb`{{execute HOST1}}

This will display on which node each service is currently running.

To verify the mongo containers on each node, execute the below command.

`docker ps`{{execute HOST01}}
`docker ps`{{execute HOST02}}
