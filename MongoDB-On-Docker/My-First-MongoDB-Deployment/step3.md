
With the necessary volumes in place, we are now ready to bring up the first Mongodb Deployment. Take a few seconds to see the pod definition

`cat mongodb-deployment.yaml`{{execute HOST1}}

Launch the pod

`kubectl create -f mongodb-deployment.yaml`{{execute HOST1}}
 
To check the status of the newly created deployment, use

`kubectl -n mongodb get deployments`{{execute HOST1}}

To check the status of the newly created pod, use

`kubectl -n mongodb get pods`{{execute HOST1}}


Initially, you will see that the pod status is not ready as Kubernetes is busy doing its background work needed to bring up the pod.

	NAME      			     READY   STATUS             RESTARTS   AGE

	mongodb-deployment-bd677f595-kwqhh   0/1     ContainerCreating   0          2m6s
	mongodb-deployment-bd677f595-q7wbc   0/1     ContainerCreating   0          2m6s
	mongodb-deployment-bd677f595-xntmp   0/1     ContainerCreating   0          2m6s

Once everything is ready, should see the status as

`kubectl -n mongodb get pods`{{execute}}

	NAME      			    READY    STATUS    RESTARTS   AGE

	mongodb-deployment-bd677f595-kwqhh   1/1     Running   0          4m22s
	mongodb-deployment-bd677f595-q7wbc   1/1     Running   0          4m22s
	mongodb-deployment-bd677f595-xntmp   1/1     Running   0          4m22s


To get a detailed description of the newly created deployment, use 

`kubectl -n mongodb describe deploy/mongodb-deployment`{{execute}}

