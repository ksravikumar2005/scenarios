Now, its time for us to bring up the ops manager container

View the contents of the docker-stack-opsmanager.yml file and you will see a service opsmanager  defined.

`cat docker-stack-opsmanager.yml`{{execute HOST1}}

Deploy these services to the docker swarm using the command below

`docker stack deploy -c docker-stack-opsmanager.yml opsmanager`{{execute HOST1}}

To view the staus of the deployed services, use the command

`docker stack ps opsmanager`{{execute HOST1}}

Initiall, all the services will be seen in "Preparing.." state, Wait for a few seconds as the specified OpsManager image is being downloaded to the node.

Try again: 

`docker stack ps opsmanager`{{execute HOST1}}

This will display on which node each service is currently running.

To verify the mongo containers on each node, execute the below command.

`docker ps`{{execute HOST01}}
`docker ps`{{execute HOST02}}
