# In this scenario, we will be 

1. Set up new docker swarm with one master and one worker
2. Prepare a stack file with 2 MongoDB services and see the environment variables that are set to enable the inital admin authentication.
3. Deploy the stack on the swarm
4. verify the services and confirm we have one service running on each node
5. Shutdown the docker service on Host02
6. Verify the services again and see if the service from the failed node came up on Host01
7. Verify Docker volumes on each node.

NOTE: This scenario shows the swarm functionality to maintain the availability of the services as mandated in the stack file. 
