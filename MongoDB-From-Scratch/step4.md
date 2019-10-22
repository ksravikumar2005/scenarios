In this step, we will play with the new MongoDB container that we created in the previous step.

Step 1: Check the logs to confirm the mongo process is up and running

docker logs myfirstmongo{{execute}}

Step 2: Check the logs on the docker host volume to confirm the volume mapping

ls -l /data/db{{execute}}

Step 3: Login to the container shell and execute mongo OR execute the below command to directly drop to mongo shell

docker exec -it myfirstmongo mongo{{execute}}

Step 4: Type "show databases" to view all the default databases, you should see the default databases like

	

Step 5: Type exit to quit the shell
