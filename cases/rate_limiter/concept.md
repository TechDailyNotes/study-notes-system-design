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
   1. [Algorithm](./high_level_design/implementation/algorithm.md)
   2. Modules
      1. Components
         1. Redis cache: efficient storage and fetching.

## Detailed Design

1. Implementation
   1. Modules:
      1. Configuration: Rate limiter middleware needs rate limiting rules config.
      2. Work Flow
         1. A worker constantly fetch updated limiting rules from disks to cache.
         2. When a request arrives, the middleware fetches the rule from cache and the latest count/timestamps from Redis.
            1. If passed the rule, the request is routed to the server.
            2. If not, the rate limiter sends a 429 too many requests error response back to the user.
               1. One option is to drop the request.
               2. One option is to store the request in a message queue.
2. System

## Wrap Up
