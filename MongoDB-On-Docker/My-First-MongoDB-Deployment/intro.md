# In this scenario, we will

  1. List all the kubernetes nodes available for us in this environment
  2. Create a PersistentVolumne on local file system for our MongoDB data files
  3. Create a PersistentVolumeClaim that uses the PersistentVolume created earlier
  4. View all the PersistentVolumes and PersistentVolumeClaims available for us to use
  5. Launch a Deployment with a MongoDB image (that we used in previous scenario) and PersistentVolumeClaim created in earlier step
  6. View the logs of the deployment and underlying pods
  7. Cleanup

NOTE: This is a simple scenario to understnd how easily an instance of MongoDB can be stood up on Kubernetes. This scenario uses the "default" kubernetes namespace.
