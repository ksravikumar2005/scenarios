In this scenario, we will

    List all the kubernetes nodes available for us in this environment
    Create a PersistentVolumne on local file system for our MongoDB data files
    Create a PersistentVolumeClaim that uses the PersistentVolume created earlier
    View all the PersistentVolumes and PersistentVolumeClaims available for us to use
    Launch a Deployment with a MongoDB image (that we used in previous scenario) and PersistentVolumeClaim created in earlier step
    View the logs of the deployment
    View underlying pods
    Connect and list the default databases available
    Cleanup

NOTE: This is a simple scenario to understnd how easily an instance of MongoDB can be stood up on Kubernetes. This scenario uses the "default" kubernetes namespace.
