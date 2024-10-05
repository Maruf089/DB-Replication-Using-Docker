# DB-Replication-Using-Docker

**Mongo Replication**

A MongoDB replica set is a group of interconnected separate instances of MongoDB that work together as one to provide high availability and fault tolerance. In a replica set, one node is elected as the primary to handle write operations while the rest serve as secondaries and replicate its data. In case of a primary node failure, a secondary node steps up to take over as the new primary, guaranteeing high availability.

![Three Nodes](https://github.com/user-attachments/assets/02d8d5d9-2358-4c94-8ac8-719f307df64b)

Step 1: cd MongoDb
Step 2: docker compose up
go to container of mongo1 using -> docker exec -it mongo1 bash
then rung mongod/mongosh  depends on version

Finally set replica using 

 rs.initiate(
  {
    _id: "rs0",
    version: 1,
    members: [
      { _id: 0, host: "mongo1:27017" },
      { _id: 1, host: "mongo2:27018" },
      { _id: 2, host: "mongo3:27019" }
    ]
  }
)
