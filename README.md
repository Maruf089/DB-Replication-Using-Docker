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



**MySql Replication**

MySQL InnoDB cluster provides a complete high availability solution for MySQL. MySQL Shell includes AdminAPI which enables you to easily configure and administer a group of at least three MySQL server instances to function as an InnoDB cluster. Each MySQL server instance runs MySQL Group Replication, which provides the mechanism to replicate data within InnoDB clusters, with built-in failover.

![1_tVjbEGafBiYEfqfAgf0DYQ](https://github.com/user-attachments/assets/4aa93b30-6aa3-472b-9857-565f026a7f21)

