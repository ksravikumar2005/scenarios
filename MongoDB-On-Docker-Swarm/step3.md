# Let`s simulate a failure  by shutting down the docker service on Host02

`systemctl stop docker`{{execute HOST02}}

Verify the docker service is stopped 

`docker ps`{{execute HOST02}}

Now, let`s verify the status of our mongo services

`docker stack ps mongodb`{{execute HOST1}}

Give it a few seconds and verify again

`sleep 15; docker stack ps mongodb`{{execute HOST1}}
