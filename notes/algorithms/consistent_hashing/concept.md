# Consistent Hashing

## Problems of Traditional Hashing Algorithm

1. Rehashing affects almost all the data.
   1. Not suitable for scenarios where rehashing is frequent.
   2. Not suitable if data amount is huge.
      1. It takes too long to rehash.
      2. It makes all the data unavailable.

## Application Scenarios

1. Distributed Storage Engine
   1. Distributed Database
   2. Distributed Cache
   3. Content Delivery Network
2. Load Balancer

## Virtual Nodes

1. Each actual storage server has multiple nodes in the hash ring.

## Find Affected Keys

1. All keys starting from the removed/added server anti-clockwise to the nearest server are affected.
