# Key-Value Store

## Single Server Key-Value Store

1. Optimization
   1. Data compression
   2. Store frequently accessed data in memory and infrequently accessed data in disk

## Distributed Key-Value Store

1. Consistency
   1. Data Partitioning
      1. Method: Consistent Hashing (Hash Ring)
      2. Pros
         1. Autoscaling
         2. Heterogeneity
   2. Data Replication
      1. Select N nearest distinct virtual nodes in distinct data centers clockwisely from the hash ring
   3. Consistency
      1. Quorum Consensus
      2. Strong Consistency: R + W > N
   4. Consistency Model
      1. Categories
         1. Strong Consistency
         2. Weak Consistency
         3. Eventual Consistency
      2. Performance
         1. Higher consistency brings about higher latency
      3. Applications
         1. Dynamo, Cassandra, and normal key-value stores adopt eventual consistency
   5. Inconsistency Solution: Versioning
