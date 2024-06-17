# Relational Model vs. Document Model vs. Graph Model

## Data Relationship

1. Graph model can handle high-interconnected data.
2. Relational model can handle normal many-to-many or many-to-one data.
3. Document model can handle one-to-many data.

## Data Schema

1. Relational model enforces a schema. (mandatory/strong schema)
   1. Categories
      1. SQL: strong schema validation.
   2. Features
      1. Schema-on-write (similar to static/compile-time type checking).
      2. Pros
         1. Safe data storage.
      3. Cons
         1. High downtime for schema changes.
   3. Scenarios
      1. Matured data model.
2. Document model has a flexible schema. (optional/weak schema)
   1. Categories
      1. JSON Schema: no schema validation.
      2. XML Schema: optional schema validation.
   2. Features
      1. Schema-on-read (similar to dynamic/run-time type checking).
      2. Pros
         1. Easy to change schema.
      3. Cons
         1. Unsafe data storage.
   3. Scenarios
      1. Rapidly changing data model.
      2. Uncontrolled data model, like user-generated content.

## Data Locality

1. Relational Model
   1. Data tends to be scattered across multiple tables.
   2. Pros
      1. Fetching smaller parts of data is faster.
   3. Cons
      1. Fetching all parts of data requires multiple queries/joins.
2. Document Model
   1. Data is stored altogether in a single large document.
   2. Pros
      1. Fetching all parts of data is faster (one query).
   3. Cons
      1. Fetching smaller parts of data is slower (load many redundant data).
