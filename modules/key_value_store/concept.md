# Key-Value Store

## Single Server Key-Value Store

1. Optimization
   1. Data compression
   2. Store frequently accessed data in memory and infrequently accessed data in disk

## Distributed Key-Value Store

### Components

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
         1. Higher consistency comes with higher latency
      3. Applications
         1. Dynamo, Cassandra, and normal key-value stores adopt eventual consistency
   5. Inconsistency Solution: Versioning
      1. Features: Vector Clock
      2. Representation: `[server: version]` pairs
      3. Patterns
         1. Ancestor-Descendant: If all the versions of data X is smaller than their correspondants of data Y, then we claim that X is the ancestor of Y.
         2. Sibling: If data X has some versions larger than their correspondants of data Y, and data Y has some versions larger than that of data X, then we claim X and Y are siblings.

### Configuration

### Composition
