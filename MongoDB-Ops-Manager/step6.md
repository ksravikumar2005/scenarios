After a couple of minutes, you should see your first "node01" in Project 0 >> Servers section.
Navigate back to Process tab and you should be able to create your first MongoDB Deployment as 

New Shared Cluster
New Replica Set Or 
New Standalone

For this scenario, select the "New Standalone" and provide the values below.

Hostname : default
Port : specify a port which is used for the mongodb deployment inside the automation agent container
Version : Version of MongoDB to be used in automation agent container
Data Directory:  /data/db
Log File : leave default

Use "Advanced Configuration Options" to provide all options that the mongodb deployment needs to use and click on "Create Standalone"
After this, you will be taken to the "Deployment" Page and you should see "Review & Deploy" button on the top, Click it and click Confirm & Deploy to create your first MongoDB deployment that you can manage from the ops manager.

Now, navigate to the servers tab and in node01 box, click on the "..." activate Monitoring and Active Backup, and click Confirm & Deploy

Once it is complete, you should be able to go back to Processes tab to view your deployment, its stats, etc.
The servers tab should show all processes inside your automation-agent container.
Click on "Data" to see all databases deployed in this section.

