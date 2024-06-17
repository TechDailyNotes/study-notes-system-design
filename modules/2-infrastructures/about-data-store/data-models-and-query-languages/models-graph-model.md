# Graph Model

## Components

1. Vertices
2. Edges

## Applications

1. Social Graph
2. Web Graph
3. Road Graph

## Categories

### Property Graph

1. Query Language: Cypher
2. Components
   1. Vertices
      1. UID (Unique Identifier)
      2. Incoming Edges
      3. Outgoing Edges
      4. Type of Vertex
      5. Properties (Key-Value Pairs)
   2. Edges
      1. UID (Unique Identifier)
      2. Source Vertex
      3. Destination Vertex
      4. Type of Edge
      5. Properties (Key-Value Pairs)

### Triple-Store Graph

1. Query Language: SPARQL
2. Components
   1. Subject
   2. Predicate
   3. Object
3. Scenarios
   1. If object is a primitive datatype, then the `predicate-object` pair is equivalent to the property of a vertex.
   2. If object is another vertex, then the `predicate-object` pair is equivalent to the edge between two vertices.

## Foundation

Datalog: Cascalog is the Datalog implementation on top of Hadoop.
