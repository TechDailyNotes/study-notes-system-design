# Algorithms

## Token Bucket

1. Description: A container with pre-defined capacity.
2. Work Flow
   1. Refill tokens in the bucket at preset rates periodically.
   2. Check if there are enough tokens when a request arrives.
3. Parameters
   1. Bucket Size
   2. Refill Rate
4. Return Values
5. Miscellaneous
   1. Configure different buckets for different APIs.
   2. Configure different buckets for different IPs.
   3. Configure a global bucket to control the total requests.
6. Pros
   1. Memory efficient.
   2. Can handle a burst of traffic.
7. Cons

## Leaking Bucket

1. Description: A queue with pre-defined capacity and preset outflow rates.
2. Work Flow
   1. Check if the queue is full when a request arrives.
   2. Process requests in the queue at the preset rate periodically.
3. Parameters
   1. Bucket Size
   2. Outflow Rate
4. Return Values
5. Miscellaneous
6. Pros
   1. Memory efficient.
   2. Can handle a burst of traffic.
7. Cons

## Fixed Window Counter

1. Description
2. Work Flow
   1. Divide a timeline into time windows.
   2. Assign request counters to time windows.
3. Parameters
4. Return Values
5. Miscellaneous
6. Pros
7. Cons
   1. Spike in traffic at window edges will cause more requests than allowed quota to go through.

## Sliding Window Log

1. Description: A queue (or sorted set) storing timestamps.
2. Work Flow
   1. When a request arrives, remove all the outdates timestamps.
   2. Check if the number of requests exceeds the pre-defined rate limit.
3. Parameters
   1. Timestamps
4. Return Values
5. Miscellaneous
6. Pros
   1. This rate limiting is very accurate, because in any rolling window, the number of requests will not exceed the rate limit.
7. Cons
   1. Memory inefficient because timestamp logs will use additional memory.

## Sliding Window Counter

1. Description: It divides a timeline into time windows.
2. Work Flow
   1. When a request arrives, it computes the percentage of overlaps between the current window and the preceding window.
   2. Total number of requests is the sum of the current window's request number and the previous window's request number multiplied by the overlap percentage.
3. Parameters
4. Return Values
5. Miscellaneous
6. Pros
   1. Memory efficient.
   2. Smooth out spikes in traffic.
   3. Work in most of the scenarios.
7. Cons
   1. Assume a even distribution in requests.
