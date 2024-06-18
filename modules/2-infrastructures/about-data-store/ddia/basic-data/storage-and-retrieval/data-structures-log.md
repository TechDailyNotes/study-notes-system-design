# Log Structured Storage Engine

## Definition

Store data in an append-only sequence of records.

## Complexity Optimization

1. Space Complexity
   1. Features: High (O(n))
   2. Causes: Logs are append-only, and old data is not deleted.
   3. Problems: Disk space reclaimation.
   4. Solutions
      1. Description: Compaction and merging.
      2. Procedures
         1. Divide the log into segments.
         2. Periodically compact and merge old segments into new segments and remove duplicate keys.
         3. Delete old segments.
         4. Route reads to the new segments.
      3. Influences on read and write
         1. Read/write from/to the newest segment first, then the second newest, and so on.
      4. Scenarios: Bitcask storage engine in Riak.
2. Time Complexity
   1. Features
      1. Read is slow: O(n)
      2. Write is fast: O(1)
   2. Solution: Hash index.

## Extension Optimization

1. File Format: Byte stream (length of string + byte representation of the string)
2. Record Deletion: Add a tombstone record.
3. Crash Recovery: Snapshots.
4. Partially Written Records: Append a checksum to the end of each record.
5. Concurrency Control: Single write thread. (read is concurrent-safe)

## Pros and Cons

1. Pros
   1. Sequential write is fast.
   2. Concurrency and crash recovery are simple.
2. Cons
   1. Hash index must fit in memory.
   2. Hash index doesn't support range queries.
