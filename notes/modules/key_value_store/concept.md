# Key-Value Store

## Single Server Key-Value Store

1. Optimization
   1. Data compression
   2. Store frequently accessed data in memory and infrequently accessed data in disk

## Distributed Key-Value Store

### Components

#### Consistency

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

#### Failure Handling

1. Failure Detection
   1. Method: Heartbeat
   2. Procedure
      1. Random Nodes: Randomly select a node and send a heartbeat message.
      2. Failure Dectection: If the node does not respond within a certain time, then the node is considered as failed.
      3. Failure Confirmation: Send a heartbeat message to the failed node from another node to confirm the failure.
      4. Failure Broadcasting: Broadcast the failure to all the nodes.
2. Failure Handling
   1. Temporate Failure
      1. Sloppy Quorum
         1. Ignore the failed node and continue the operation
            1. Use first W available nodes to write data
            2. Use first R available nodes to read data
      2. Traffic Redirection
         1. Redirect the traffic to other healthy nodes
   2. Permanent Failure
      1. Data Sync
         1. Method: Anti-Entropy Protocol
         2. Data Structure: Merkle Tree
         3. Algorithm: Hashing
         4. Time Complexity: `O(logn)`
   3. Data Center Outage
      1. Distribute data replicas to different data centers

### Configuration

### Composition
