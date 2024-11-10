# Sharding: 

Sharding is a database architecture pattern used to split large databases into smaller, 
more manageable pieces, called shards, that are distributed across multiple servers.

# How sharding works:

i. Data Partitioning by Shard Key
ii. Routing Queries to the Right Shard
iii. Replication and Redundancy

# Benefitis of sharding: 

i. scalability
ii. improve performance
iii. fault Tolerance

# Challenges

i. Complexity: Sharding adds complexity to database architecture, especially with data routing and
 ensuring ACID compliance across shards.

  # Solution
   i. Use middleware for query routing. Vitess for MySQL, Citus for PostgreSQL, or ProxySQL for MySQL.
   ii. Choose an Effective Shard Key

ii. Rebalancing: If a shard becomes too large, it might need to be split again or rebalanced, 
which can be operationally challenging.
   
   # Solution
    i. Automated Rebalancing Tools and Platforms: Use databases and platforms with built-in rebalancing capabilities, such as MongoDB, Azure Cosmos DB, Amazon DynamoDB, and Google Spanner
    ii. Manual Rebalancing with Shard Key Redistribution: Adjust the shard key ranges for overloaded shards and manually migrate data from overloaded shards to new or underutilized shards

iii. Cross-Shard Queries: Queries that require data from multiple shards can be complex and resource-intensive to execute.

   # Solution
    i. Choose a shard key that logically groups related data, so most queries access only one shard.
    ii. Use a distributed SQL database that natively supports cross-shard queries, like Google Spanner, CockroachDB, or Vitess.
    