# Create Swarm Cluster
NOTE: The terminal on the top from host01 and the at the bottom is host02 
Verify the hostnames with the following commands:

`hostname`{{execute HOST1}}
`hostname`{{execute HOST2}}

## Run this command to initialize swarm, this command would run on host1


`docker swarm init`{{execute HOST1}}

Verify the swarm status with the command below

`docker node ls`{{ execute HOST1}}

You will see that our swarm has only one node and that is the leader. To join nodes, we will need eth join-token that you can run on any Docker node to make it a worker

`docker swarm join-token worker`{{execute}}

## This command runs on host02

Use this command to fetche the join-token from the host01 and uses it on the host02 to join it as a worker node


`token=$(ssh -o StrictHostKeyChecking=no 172.17.0.11 "docker swarm join-token -q worker") && echo $token`{{execute HOST2}}

On the worker node

`docker swarm join 172.17.0.11:2377 --token $token`{{execute HOST2}}

Create Overlay Network

`docker network create -d overlay mongodb`{{execute}}

