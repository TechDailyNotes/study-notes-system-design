# Scalability

The system scales easily.

## Metrics

### Throughput

1. Definition: The number of requests a server can handle per second.

### Response Time

1. Definition: Total time taken to serve a request (between the client sends a request and receives a response).
2. Comparison
   1. Latency: The time a request waits to be handled.
3. Measurement
   1. Metrics
      1. Median
      2. High percentiles/Tail latencies (e.g. p95, p99, p999)
   2. Calculation
      1. Rolling Window + Sorting
4. SLO/SLA
   1. Service Level Objective/Agreement
   2. Definition: The percentage of requests that should be served within a certain time.
   3. Standards
      1. 50% of requests should be served within 200ms.
      2. 99% of requests should be served within 1s.
5. Tests
   1. Test client should keep sending requests independently of the response time.
6. Problems
   1. Tail latency amplification: It takes only one slow request to make the entire end-user request slow.
