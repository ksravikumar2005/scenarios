# Create a PersistentVolume Claim to use the previously created PersistentVolume

View the PersistentVolumeClaim definition and you will see that the previously created PersistentVolume is selected for this claim using the "selector"
`cat mongodb-datadb-pvc.yaml`{{execute}}

To create a PersistentVolumeClaim, use

`kubectl create -f mongodb-datadb-pvc.yaml`{{execute}}

To list the available PersistentVolumeClaims, use

`kubectl get pvc`{{execute}}

Here, you will see that the PersistentVolumeClaim is now using the PersistentVolume that was created previously.

For more detailed description of the PersistentVolumeClaim, use

`kubectl describe pvc/mongodb-datadb-pvc`{{execute}}
