# Algorithm

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

## Sliding Window Counter
