# CAP Theory

## Definition

CAP theorem states that it is impossible for a distributed data store to simultaneously provide more than two out of the following three guarantees: Consistency, Availability, and Partition Tolerance.

## Categories

1. CP: Consistency and Partition Tolerance
   1. If a partition occurs, the system will stop  responding until the partition is resolved.
   2. Strong consistency
2. AP: Availability and Partition Tolerance
   1. If a partition occurs, the system will continue to respond.
   2. Eventual consistency
3. CA: Consistency and Availability
