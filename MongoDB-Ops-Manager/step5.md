When everything is complete, you will be taken to "You don't have any deployments yet" page, indicating that ops Manager is ready.
On the default "Project 0", click on Agents, then on Downloads and Settings.
Under the "MongoDB Agent current: 10.2.7.5898" tab, Select your operating system, select the first option - RedHat / CentOS (7.X), SuSE 12, Amazon Linux2 - RPM
From the popup window, click on "+Generate Key" from step 2 and under the "Next, open the config file", copy the mmsGroupId, mmsApiKey and mmsBaseUrl as follows

Example Values:

mmsGroupId=5dafb6cca228fe0063898805
mmsApiKey=5dafba1ea228fe006389892d7c36c79977f2a7e211b8298e63c03d19
mmsBaseUrl=http://2886795283-18080-frugo01.environments.katacoda.com 

Using the above values, create a string like 

command: --mmsBaseUrl=http://2886795283-18080-frugo01.environments.katacoda.com --mmsGroupId=5dafb6cca228fe0063898805  --mmsApiKey=5dafba1ea228fe006389892d7c36c79977f    2a7e211b8298e63c03d19

Now, open the docker-stack-automationagent.yml and replace the prepopulated values in line 12 with the above values obtained from the ops manager and save the file.

Deploy the automation agent service to the current swarm using the command

`docker stack deploy -c docker-stack-automationagent.yml ospmanager`{{execute}}

