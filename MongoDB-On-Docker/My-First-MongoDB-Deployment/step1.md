
View the Kubernetes Nodes available for us to use.

NOTE: It might take a minute or two for the kubernetes cluster to get ready to use. 

`kubectl get nodes`{{execute HOST1}}

Clone the git repo that has files to get started.

`git clone https://github.com/ksravikumar2005/mongodb-k8s.git`{{execute HOST1}}

`cd mongodb-k8s/deployment`{{execute HOST1}}

Create a directory on local file system to persist the mongodb data files and change the ownership to 1000:1000 as the mongodb userid:groupid used in the image is 1000:1000

On host1:

`mkdir -p /data/mongodb0`{{execute HOST1}}

`mkdir -p /data/mongodb2`{{execute HOST1}}
`chown -R 1000:1000 /data/mongodb*`{{execute HOST1}}

On host2

`mkdir -p /data/mongodb1`{{execute HOST2}}

`chown -R 1000:1000 /data/mongodb*`{{execute HOST2}}

Since we have same type of volumes used on all nodes, it makes sense to create a Storage Class. To view the yaml file for storage class, use

`cat mongodb-sc.yaml`{{execute HOST1}}

To create a storage class use

`kubectl create -f mongodb-sc.yaml`{{execute HOST1}}

To view the storage class 

`kubectl get sc`{{execute HOST1}}

Create Kubernetes PersistentVolume(s) using the folders that were created previously and using the mongodb-datadb-pv.yaml

`kubectl create -f mongodb-pv.yaml`{{execute}}

For more details on the newly created PersistentVolume

`kubectl get pv`{{execute HOST1}}

To view the physical locations mapped to each PersistenVolume, use

`kubectl describe pv/mongodb-pv0`{{execute HOST1}}

`kubectl describe pv/mongodb-pv1`{{execute HOST1}}

`kubectl describe pv/mongodb-pv2`{{execute HOST1}}




