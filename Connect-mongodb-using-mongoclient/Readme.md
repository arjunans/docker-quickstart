**Purpose of Network:** 
- Containers are by default isolated environment. when we run multiple containers for one application, how do containers communicate? That's where docker networking comes into picture.

# How to create a network in docker?
  - docker network create db-network

# How to create a Mongo db instance in a network?
 - docker run --net db-network --name mongo-dbserver -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=pass123 mongo

# How to create a mongo-express in a network
 - docker run --net db-network --name mongo-client -p9001:8081 -e ME_CONFIG_MONGODB_SERVER=mongo-dbserver -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=pass123 mongo-express

