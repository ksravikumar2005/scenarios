
With the necessary volume objects in place, we are now ready to bring up the first Mongodb. Take a few seconds to see the pod definition

`cat mongodb-pod-definition.yaml`{{execute}}

Launch the pod

`kubectl create -f mongodb-pod-definition.yaml`{{execute}}

To check the status of the newly created pod, use

`kubectl get pods`{{execute}}


Initially, you will see that the pod status is not ready as Kubernetes is busy doing its background work needed to bring up the pod.

	NAME      READY   STATUS             RESTARTS   AGE
	mongodb   0/1     ContainerCreating             2m33s

Once everything is ready, should see the status as

`kubectl get pods`{{execute}}

	NAME      READY   STATUS    RESTARTS   AGE
	mongodb   1/1     Running   0          2m33s


To get a detailed description of the newly created pod, use 

`kubectl describe pod/mongodb`{{execute}}

To use the mongo client, execute

`kubectl exec -it mongodb mongo`{{execute}}

NOTE: mongodb is the server process and mongo is the database client.

At the mongo shell, execute the command "show databases" view the databases created and type "exit" to exit the mongo shell.
