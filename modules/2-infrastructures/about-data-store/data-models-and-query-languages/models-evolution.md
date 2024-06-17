# Evolution of Data Models

## Hierarchical Data Model

1. Features: Uses a tree-like structure to store data. Each record has a single parent record and can have multiple children.
2. Pros
   1. Efficient computation.
   2. Efficient query.
3. Cons
   1. Inefficient storage
      1. Duplicate records, especially in a many-to-one or many-to-many relationship.

## Network Data Model

1. Features: Uses a graph-like structure to store data. Each record can have multiple parent and child records.
2. Pros
   1. Efficient computation.
   2. Efficient storage.
3. Cons
   1. Inefficient query, especially in many-to-many relationships.

## Relational Data Model

1. Features: Uses tables to store data. Each table has rows and columns. Each row (relation) is simply a unordered collection of attributes (tuple/columns).
2. Pros
   1. Efficient query.
   2. Efficient storage.
3. Cons
   1. Inefficient computation, because each data record requires multiple joins/queries.

## Object-Oriented Data Model

## Document Data Model

1. Features: Uses a document-like structure to store data. Each document is a collection of key-value pairs.
2. Pros
   1. Efficient computation, no need for multiple joins/queries, especially in the one-to-many relationship.
   2. Efficient storage, because it applies the document reference to reduce duplicate records.
   3. Efficient query.

## Graph Data Model
