# Designs

## Functional

1. What is this system about?
   1. Recommend posts to users based on their interests/queries.
2. What is the core business target/metric?
   1. Improve DAU, sessions, and user engagements.
3. How to measure the performance of the system?
   1. Positive signals: likings, comments, sharings, and followings.
   2. Negative signals: reportings, unfollowings, and blockings.

## Non-Functional

1. Properties
   1. Performance
      1. Scalability
      2. Availability
      3. Low latency
      4. High throughput
   2. Management
      1. Observability
      2. Visibility
      3. Maintainability
2. Distributed Systems
   1. Distributed servers
   2. Distributed data systems
   3. Distributed model training
      1. Data parallelism
      2. Tensor parallelism
      3. Pipeline parallelism
3. Tooling
   1. Logging
   2. Monitoring

## Estimation

1. DAU: 500 million users

## Data

1. Features
   1. Types
      1. Users
         1. Views
         2. Profile
         3. History behaviors
      2. Queries
      3. Items
         1. Text
         2. Audio
         3. Video
   2. Preprocessing
      1. Embeddings
         1. Purpose
            1. Quantify different types of data into vectors.
            2. Reveal the hidden patterns/semantics in the data.
         2. Source
            1. Pre-trained models (if we don't have embeddings from a working system).
            2. Embeddings from legacy systems or evolving systems.
      2. Fusion
2. Labels
   1. Types
      1. Likings
      2. Comments
      3. Sharings
      4. Followings
3. Example Data Pair
   1. (u, q, i, p, r)

## Model

1. Model Pipeline
   1. Retrieval
      1. Candidate Generation
         1. ANN (Approximate Nearest Neighbors)
      2. Filtering
         1. Bloom Filter
   2. Ranking
      1. Scoring
      2. Ordering

## Serving
