# Explore SQL with PostgreSQL

### Covered topics in Module 15

- What is Database?
  - A database is a structured collection of related data that represent some real world entities and are organized for efficiant retrival storage and management.
- What is Data?
  - Data is facts that can be recorded in the form of text, video, audio etc.
- What is information?
  - Information is processed and organized data that provides meaningfull context, insight or knowledge.
- What is DBMS and Why we use it?
  - DBMS is a software which help us to manage database.
- RDBMS instruct by SQL
- Types of Database
  - Relational --> MySQL, PostgreSQL, SQLLite, SQLServer
  - Document --> MongoDB, Amazon DynamoDB
  - Key Value --> Redis
  - Graph database
- Different types of Database model
  - Hierarchical
  - Network
  - Relational
  - Document
  - Key Value
- Anatomy of a Table/Relation
  - Table --> Relation/Entities
  - Column --> Column/Attribute
  - Collection of column --> Degree
  - Row --> Rows/Tuples/Records
  - Collection of row --> Cardinality
- What is Key?
  - A key in a relational database is a field or a combination of fields that uniquely identifies a records in a table.
- Types of key
  1. Super key
  2. Candidate key
  3. Alternate key
  4. Composite key
  5. Forign key
  6. Primary key
- In SDLC database is designed in system design phase.
- Relationship types in RDBMS
  - one-to-one (1:1)
  - one-to-many (1:N)
  - many-to-one (N:1)
  - many-to-many (N:N)
  - Optional one-to-one (0...1:0...1)
  - Optional one-to-many (0...1:N)
- Steps of database design
  1. Determining entities
  2. Determining attributes
  3. Relationship among entities or relationship cardinality
  4. Solving many to many

### Covered topics in Module 16

- Anomalies --> Anomalies in databases refer to inconsistencies or unexpected issues that can occur during data manipulation or retrieval.
- There are 3 main types of anomalies
  1. Update anomalies
  2. Delete anomalies
  3. Insert anomalies
- Normalization is a technique of database design
- Functional Dependency
- Normal Forms
- Types of Normal Forms
  1. 0NF
  2. 1NF
  3. 2NF
  4. 3NF
- Transitive Dependency
- Normalization can't remove the repetation of data, but can minimize the repetation of data
- Junction/Intermediate table -> This table use for resolve many-to-many relationship
- In remote server we can't use GUI software for DBMS, We need to use there terminal commands

  #### PostgreSQL commands

  - select version(); --> check postgres version
  - \l --> show database list
  - \c --> change database
  - \d --> show table in database
  - \dt --> By this command also we can check table
  - \d+ --> By this command we can get details information about table
  - create table table_name --> Use for create a new table
  - \dn --> For see database schema
  - Owner means a user who create the table
  - \q --> For quite from psql
