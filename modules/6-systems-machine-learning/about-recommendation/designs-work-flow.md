# Work Flow

## Procedures

1. Query Processing (QP)
2. Recall
3. Retrieval
4. Ranking

## Modules

### Query Processing

1. Query Processing Model

### Recall

### Retrieval

1. Retrieval Model
2. Document Embedding Model
3. Inverted Index

### Ranking

1. Ranking Model
2. Forward Index

## Examples

### DoorDash Search System

![DoorDash Search System](./diagrams/work-flow-doordash.png)

#### Core Procedures

1. Recall
   1. Spell Check
   2. Query Understanding (Query Processing) - QP Model
   3. Query Expansion (Retrieval) - Retrieval Model
2. Precision
   1. Ranking - Ranking Model
   2. Decorate

#### Full Procedures

1. User Query
2. Recall
3. Precision
4. Online Evaluation

#### Offline Tasks

1. Model Training
   1. Trained Data
   2. Model
   3. Offline Evaluation
2. Data Preprocessing
   1. Embeddings Data
      1. Database: Pinecone, Aroma
   2. Graph Data
      1. Database: Neo4j
   3. Document Data
      1. Database: Elasticsearch
   4. Attributes Data
      1. Database: MySQL, noSQL
