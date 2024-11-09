# Master Database (Primary): Responsible for all write operation. Insert, delete, update.

like all user transaction -> add to cart, payment in e-commerce

# slave database (Replica): Improve read performance, high availity, load balancing, data redundancy

ensure data will not loss. like browse products, searching

# Master-Slave challenges or Disadvantages:

1. Single Point of Failure for Writes

Solution: 

i. Sharding or Partitioning
ii. Master-Master replication: Multiple nodes use for write and read operation.
iii. Automatic Failover with Master Election: automatically select master from slaves a node using
    database tools like Zookeepe, etcd, consul
   
2.  Replication Lag: In asynchronous replication, there is a time delay before updates on the master 
reach the replicas, creating a risk that replicas may serve outdated data.

Solution:

i. keep close the replica to the master. same data center.
ii. Optimize Network Latency
iii. Use batching for write operations, which can improve throughput by reducing the number of individual write transactions.