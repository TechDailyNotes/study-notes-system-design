# SSTable or LSM-Tree

SSTable: Sorted String Table
LSM-Tree: Log-Structured Merge-Tree

## Inherited Design Idea

1. Log storage engine.
   1. Sequential write is fast.
   2. Log segments help with compaction and merging.

## Problems to Solve

1. Log storage engine.
   1. Hash index takes up too much memory.

## Definition

1. Sort key-value pairs by the key when compacting and merging.
2. Take ${O(\sqrt{n})}$ time to read/write.
3. Hash index takes up ${O(\sqrt{n})}$ memory.

## Extension Optimization

1. Memtable
   1. Definition: A self-balancing binary search tree.
   2. Functionality: Keep in-memory key-value pairs sorted.
2. Bloom Filter
   1. Definition: An in-memory data structure.
   2. Functionality: Rapidly determine whether a key exists in the SSTable.
