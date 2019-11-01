To cleanup the deployment, pods, volumes, etc., 

`kubectl delete -k ./ `{{execute}}

To confirm the cleanup

`kubectl get pods,pv,pvc`{{execute}}

To bring up the whole setup again, you can use the command

kubectl create  -f mongodb-pod-definition.yaml -f mongodb-datadb-pvc.yaml -f mongodb-datadb-pv.yaml
