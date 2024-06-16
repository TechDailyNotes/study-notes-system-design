# Modules

## Redis Cache

1. Component
   1. Redis cache: efficient storage and fetching.
2. Configuration: Rate limiter middleware needs rate limiting rules config.
3. Composition
   1. A worker constantly fetch updated limiting rules from disks to cache.
   2. When a request arrives, the middleware fetches the rule from cache and the latest count/timestamps from Redis.
      1. If passed the rule, the request is routed to the server.
      2. If not, the rate limiter sends a 429 too many requests error response back to the user.
         1. One option is to drop the request.
         2. One option is to store the request in a message queue.
4. Pros
5. Cons
