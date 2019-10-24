# In this scenario, we will

1. List all the kubernetes nodes available for us in this environment
2. Create a PersistentVolumne on local file system for our MongoDB data files
3. Create a PersistentVolumeClaim that uses the PersistentVolume created earlier
4. View all the PersistentVolumes and PersistentVolumeClaims available for us
5. Launch a Pod with a MongoDB image that uses the PersistentVolumeClaim created earlier
6. View the logs of the Pod
7. Connect and list the default databases available
8. Cleanup

NOTE: This is a simple scenario to understnd how easily an instance of MongoDB can be stood up on Kubernetes. This scenario uses the "default" kubernetes namespace.
