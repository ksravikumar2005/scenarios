
View the PersistentVolumeClaim definition and you will see that the previously created PersistentVolume is selected for this claim using the "selector"

`cat mongodb-pvc.yaml`{{execute HOST1}}

To create a PersistentVolumeClaim, use

`kubectl create -f mongodb-pvc.yaml`{{execute HOST1}}

To list the available PersistentVolumeClaims, use

`kubectl -n mongodb get pvc`{{execute HOST1}}

Here, you will see that the PersistentVolumeClaim is now using the PersistentVolume that was created previously.

For more detailed description of the PersistentVolumeClaim, use

`kubectl -n mongodb describe persistentvolumeclaim/mongodb-data-0`{{execute HOST1}}
