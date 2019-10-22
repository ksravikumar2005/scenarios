# Create Swarm Cluster
## Initialize
`docker swarm init`{{execute}}

##Join

`token=$(ssh -o StrictHostKeyChecking=no 172.17.0.11 "docker swarm join-token -q worker") && echo $token`{{execute}}

On the worker node

`docker swarm join 172.17.0.11:2377 --token $token`{{execute}}

Create Overlay Network

`docker network create -d overlay mongodb`{{execute}}

