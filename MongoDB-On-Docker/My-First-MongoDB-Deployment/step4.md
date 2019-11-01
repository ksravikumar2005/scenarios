To cleanup the deployment, pods, volumes, etc., 

`kubectl delete ./ `{{execute}}

To confirm the cleanup

`kubectl get pods,pv,pvc`{{execute}}

To bring up the whole setup again, you can use the command

kubectl create  -f ./
