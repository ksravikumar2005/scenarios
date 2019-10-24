# Standing up your first MongoDB pod

With the necessary volume objects in place, we are now ready to bring up the first Mongodb. Take a few seconds to see the pod definition

`cat mongodb-pod-definition.yaml`{{execute}}

Launch the pod

`kubectl create -f mongodb-pod-definition.yaml`{{execute}}

To check the status of the newly created pod, use

`kubectl get pods`{{execute}}

To get a detailed description of the newly created pod, use 

`kubectl describe pod/mongodb`{{execute}}

To use the mongo client, execute

`kubectl exec -it pod/mongodb mongo`{{execute}}

At the mongo shell, execute the command "show databases" view the databases created.

To cleanup, execute

`kubectl delete -f mongodb-pod-definition.yaml -f mongodb-datadb-pvc.yaml -f mongodb-datadb-pv.yaml`{{execute}}

To bring up the whole setup again, you can use the command

kubectl create  -f mongodb-pod-definition.yaml -f mongodb-datadb-pvc.yaml -f mongodb-datadb-pv.yaml

To confirm the cleanup

`kubectl get pods,pv,pvc`{{execute}}


