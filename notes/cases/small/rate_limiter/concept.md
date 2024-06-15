# Rate Limiter

## Design Scope Questions

1. Definition
   1. Rate limiter limits the number of client requests allowed to be sent over a specific period.
2. Connection
   1. Modularization: Is it a separate service or should it be implemeted in application codes?
   2. Location
      1. Where to put the rate limiter with regard to other modules?
      2. Is it a client-side or server-side rate limiter?
3. Performance
4. Implementation
   1. Input: Do we throttle API based on IP, user ID or other properties?
   2. Output: Do we need to inform throttled users?
