# Next Steps

With this, you now have a 3 mongodb nodes that are managed as part of a single deployment. The next step would be to create a 3 node replicaset with 1 primary (master) and 2 secondary (slaves) nodes.

To cleanup the deployment, pods, volumes, etc., 

`kubectl delete -f ./ `{{execute}}

To confirm the cleanup

`kubectl -n mongodb get pods,pv,pvc`{{execute}}

To bring up the whole setup again, you can use the command

kubectl create  -f ./
