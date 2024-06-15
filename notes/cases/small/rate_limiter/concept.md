# Rate Limiter

## Definition

Rate limiter limits the number of client requests allowed to be sent over a specific period.

## Design Scope Questions

1. Location
   1. Modularization: Is it a separate service or should it be implemeted in application codes?
   2. Connection
      1. Where to put the rate limiter with regard to other modules?
      2. Is it a client-side or server-side rate limiter?
2. Implementation
   1. Input: Do we throttle API based on IP, user ID or other properties?
   2. Output: Do we need to inform throttled users?
3. System
   1. Distributed systems

## High Level Design

1. Location
   1. Modularizatio: Separate service
   2. Connection: Standalone middleware
2. Implementation
   1. [Algorithms](./high_level_design/implementation/algorithms.md)
   2. [Modules](./detailed_design/implementation/modules.md)

## Detailed Design

1. Implementation
   1. [Modules](./detailed_design/implementation/modules.md)
2. System
   1. Race Condition
   2. Synchronization
