# Algorithms for Unique ID Generator

## Multi-Master Replication

1. Description: Each master auto-increments its ID by `k` where `k` is the number of masters.
2. Work Flow
3. Parameters
4. Return Values
5. Miscellaneous
6. Pros
7. Cons
   1. Unique IDs are not sorted by time.
   2. Hard to scale up/down the number of masters.

## Universally Unique Identifier (UUID)

1. Description: Generate a 128-bit number.
2. Work Flow
3. Parameters
4. Return Values
5. Miscellaneous
6. Pros
   1. Simple to generate in each server so that no need to communicate with other servers.
   2. Each server can generate unique IDs without any coordination so that it is easy to scale up/down the number of servers.
7. Cons
   1. The IDs are not sorted by time.
   2. The IDs are not numeric values.
   3. The IDs are not 64-bit values.

## Ticket Server

1. Description: A server generates a unique ID and returns it to the client.
2. Work Flow
3. Parameters
4. Return Values
5. Miscellaneous
6. Pros
   1. The IDs are sorted by time.
   2. The IDs are numeric values.
7. Cons
   1. The server is a single point of failure.

## Twitter Snowflake Approach

1. Description: Generate a compound number consisting of a timestamp, a datacenter ID, a machine ID, and a sequence number.
2. Work Flow
   1. Single bit: 0 (positive number)
   2. Timestamp: 41 bits (milliseconds since a custom epoch)
   3. Datacenter ID: 5 bits
   4. Machine ID: 5 bits
   5. Sequence number: 12 bits
3. Parameters
4. Return Values
5. Miscellaneous
6. Pros
   1. The IDs are sorted by time.
   2. The IDs are numeric values.
   3. The IDs are 64-bit values.
7. Cons
