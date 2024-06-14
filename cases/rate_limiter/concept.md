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
   1. Scalability
      1. Startup or big company
      2. Distributed systems

## High Level Design

1. Location
   1. Modularizatio: Separate service
   2. Connection: Standalone middleware
2. Implementation
   1. [Algorithm](./high_level_design/implementation/algorithm.md)
3. System
   1. Scalability

## Detailed Design

## Wrap Up
