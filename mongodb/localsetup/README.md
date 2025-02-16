# MongoDB setup in local

Better way to setup in local is using docker or any other container platform such as podman.

I tried to do it using docker. And specifically using docker compose as I wanted to use mongo-express - an UI tool to access MongoDB and work on it (create/update/delete documents)


## Connecting to MongoDB through CLI

After starting the MongoDB as docker container, login to mongodb container and execute 'mongosh' command to connect to the local instance and start shell.
But if we have any username or password, we need to connect using those credentials.

Below command to connect to my local instance (running within the docker container) 

docker exec -it <mongodo_containerId> /bin/bash

mongosh "mongodb://localhost:27017" --username admin --password password --authenticationDatabase admin

These above commands helped me to login to MongoDB container, and also start a MongoShell and connect to the MongoDB running in local. Set to do hand-on practice with the Mongo queries.


