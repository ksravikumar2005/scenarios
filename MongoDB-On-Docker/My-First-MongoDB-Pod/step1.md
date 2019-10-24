
View the Kubernetes Nodes available for us to use.

`kubectl get nodes`{{execute}

Clone the git repo that has files to get started.

`git clone https://github.com/ksravikumar2005/mongodb-k8s.git`{{execute}}
`cd mongodb-k8s/`{{execute}}

Create a directory on local file system to persist the mongodb data files and change the ownership to 1000:1000 as the mongodb userid:groupid used in the image is 1000:1000

`mkdir -p /tmp/uservolumes/mongo-datadb`{{execute}}
`chown -R 1000:1000 /tmp/uservolumes/mongo-datadb`{{execute}}

Create a Kubernetes PersistentVolume using the mongodb-datadb-pv.yaml

`kubectl create -f mongodb-datadb-pv.yaml`{{execute}}

For more details on the newly created PersistentVolume

`kubectl get pv`{{execute}}
`kubectl describe persistentvolume/mongodb-datadb-pv`{{execute}}


