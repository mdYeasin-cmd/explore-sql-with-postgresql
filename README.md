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
  - \conninfo --> Use for check current session user
  - \du --> By this command we can check databse user list

### Covered topics in Module 17

- "-u" by this flag we say the username for database server
- Template database means blue print of create a new database
- Postgres is not case-sensitive
- By connection limit we can set, how many user can connect with a database
- Attribute is collection of privileges
- Best practice, we should give database access to user as less as possible
- "\*" -> wild card, by this mean that select all
- In postgres we can control user permission from granular level
- We can add a user as a role of another user
- PostgreSQL data types
  1. Boolean
  2. Number
  3. Binary
  4. Date/Time
  5. Json
  6. Character
  7. UUID
  8. Array
  9. XML
- Constraints - Constraint use for add extra validation on column

  1.  Primary validation of a column is set data type for that column
  2.  And then we can add more validation by using constraint

- NOT NULL
- UNIQUE
- PRIMARY KEY
- FORIGN KEY (REFERENCES)
- DEFAULT
- CHECK
- Due to indexing query is faster then regular columns

#### SQL commands

##### User elements

- create user user_name login encrypted password 'user_password';
- create role role_name;
- set role user_name;
- select current_user, session_user;
- grant all privileges on table_name to user_name;
- grant select on table_name to user_name;
- revoke select on table_name from user_name;

##### Database elements

- create database db_name;
- create table table_name(
  column1, datatype, constraint,
  column2, datatype, constraint,
  column3, datatype, constraint
  );

##### Insert data

Single row insert

- insert into table_name(column1, column2, column3) values(value1, value2, value3);

Multi row insert

- insert into table_name(column1, column2, column3)
  values(value1, value2, value3), (value1, value2, value3), (value1, value2, value3);

Without define columns

- insert into table_name values(value1, value2, value3);
- insert into table_name
  values(value1, value2, value3), (value1, value2, value3), (value1, value2, value3);

##### Select data

- select \* from table_name;

### Covered topics in Module 18

- ALTER --> use for modify existing column structure
- Actions of ALTER keyword are -->
  1. Rename table
  2. Modify data type of a column
  3. Add/Drop column
  4. Setting default value of a column
  5. Rename a column
  6. Add/Drop constraint for a column
- NOT NULL and DEFAULT VALUE works for indivisual column
- UNIQUE, PRIMARY KEY, FORIGN KEY --> Here we can pass multiple column
- Some SELECT related methods are -->
  1. SELECT
  2. FROM
  3. WHERE
  4. ORDER
  5. GROUP
  6. HAVING
  7. JOIN
  8. DISTINCT
  9. LIMIT
  10. OFFSET
  11. IN
  12. LIKE --> case sensitive during perform operation
  13. ILIKE --> non case sensitive during perform operation
- "" --> Double quotation for column and '' --> Single quotation for row
- Postgres funtion type
  1. Scalar --> Perform operation on each row data
  2. Aggregate --> Perform operation accross multiple rows, often with the GROUP BY clause
- For complex query NOT keyword is useful
- NULL is special in postgres. What operation we perform with NULL that doesn't matter, it always return NULL
- COALESCE --> Return the first non-null value in a list
- During database design we need to handle NULL value smartly.
- Some special keyword
  - n% --> Need to match from start
  - %n --> Need to match from end
  - \_\_\_n --> Need to match first three character
  - \_\_n% --> Need to match first threed character and all last character doesn't matter
- UPDATE, DELETE and DROP --> We should careful during run mentioned 3 commands
