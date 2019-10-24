
`kubectl delete -f mongodb-pod-definition.yaml -f mongodb-datadb-pvc.yaml -f mongodb-datadb-pv.yaml`{{execute}}

To bring up the whole setup again, you can use the command

kubectl create  -f mongodb-pod-definition.yaml -f mongodb-datadb-pvc.yaml -f mongodb-datadb-pv.yaml

To confirm the cleanup

`kubectl get pods,pv,pvc`{{execute}}

