Now, its time for us to bring up the ops manager container

View the contents of the docker-stack-opsmanager.yml file and you will see a service opsmanager  defined.

`cat docker-stack-opsmanager.yml`{{execute HOST1}}

Deploy these services to the docker swarm using the command below

`docker stack deploy -c docker-stack-opsmanager.yml opsmanager`{{execute HOST1}}

Check the status of the OPS Manager service using the below command

`docker service logs --follow opsmanager_opsmanager`{{execute}

The output should look like this - this might take about 5 - 8 minutes depending on the internet bandwidth, etc.,

opsmanager_opsmanager.1.0pufq92d2bm2@host01    | tput: No value for $TERM and no -T specified
opsmanager_opsmanager.1.0pufq92d2bm2@host01    | Starting pre-flight checks
opsmanager_opsmanager.1.0pufq92d2bm2@host01    | Successfully finished pre-flight checks
opsmanager_opsmanager.1.0pufq92d2bm2@host01    |
opsmanager_opsmanager.1.0pufq92d2bm2@host01    | Migrate Ops Manager data
opsmanager_opsmanager.1.0pufq92d2bm2@host01    |    Running migrations...[  OK  ]
opsmanager_opsmanager.1.0pufq92d2bm2@host01    | Starting Ops Manager server
opsmanager_opsmanager.1.0pufq92d2bm2@host01    |    Instance 0 starting.................[  OK  ]
opsmanager_opsmanager.1.0pufq92d2bm2@host01    | tput: No value for $TERM and no -T specified
opsmanager_opsmanager.1.0pufq92d2bm2@host01    | Starting pre-flight checks
opsmanager_opsmanager.1.0pufq92d2bm2@host01    | Successfully finished pre-flight checks
opsmanager_opsmanager.1.0pufq92d2bm2@host01    |
opsmanager_opsmanager.1.0pufq92d2bm2@host01    | Start Backup Daemon...[  OK  ]
opsmanager_opsmanager.1.0pufq92d2bm2@host01    | MongoDB Ops Manager is running. Check the logs folder for logs.

Once you see the last line that says - "MongoDB Ops Manager is running. Check the logs folder for logs.", press Ctrl+C to exit the log tail mode.

To view the staus of the deployed services, use the command

`docker stack ps opsmanager`{{execute HOST1}}

This will display on which node each service is currently running.

To verify the mongo containers on each node, execute the below command.

`docker ps`{{execute HOST01}}
`docker ps`{{execute HOST02}}
