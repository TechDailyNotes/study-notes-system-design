# B-Tree

## Definition

1. B-Tree is a multi-way search tree that is designed to work well on disk storage.
2. Each block/page is 4KB in size.

## Complexity Optimization

1. Time complexity: O(logN)

## Extension Optimization

1. WAL (Write-Ahead Log) / redo log
   1. Functionality: Help with data recovery/operation recovery after unexpected system shutdown/hardware crashes.
2. Concurrency control
   1. Solutions
      1. Latches
      2. Snapshot Isolation
      3. Copy-on-Write
