# Next Steps

With this, you now have a 3 mongodb nodes that are managed as part of a single deployment. The next step would be to create a 3 node replicaset with 1 primary (master) and 2 secondary (slaves) nodes.

To access individual MongoDB Deployments, you may access them via MongoDB pods. To list all available pods on this name space, use

`kubectl -n mongodb get pods`{{execute HOST1}}

To access mongodb shell from a speific pod, use the command

kubectl -n mongodb exec -it pod/"name of your pod" --mongo

To quit, just type exit on the shell

Irrespective of the pod or container restarts, you should still be able to see the contents persist as we have mapped the MongoDB data directory to a physical volume.

To cleanup the deployment, pods, volumes, etc., 

`kubectl delete -f ./ `{{execute}}

To confirm the cleanup

`kubectl -n mongodb get pods,pv,pvc`{{execute}}

To bring up the whole setup again, you can use the command

kubectl create  -f ./
