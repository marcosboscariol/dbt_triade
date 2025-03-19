# Chapter 3: SQL for Analytics

# SQL

- Used to store and analyze data
- Widely used on data environment
    - Readability of the code
    - Engines behind it have evolved a lot
    - Other tools use it as an interface, such as Spark, DuckDB
    - Have a strong data type rules
    - Tools like Window Function and CTE’s allows the users to make advanced analysis in a simple way

## Types of Databases

### Non-Relational Databases

- NoSQL
- Key-value, Graph, Column, Document
- Alternative for managing large volumes of unstructured and semi-structured data
- Do not rely on fixed schemas
- Prioritize high performance, horizontal scalability and  schema flexibility

### Relational Databases

- OLTP and OLAP
- Organized into tables of rows and columns
- Relationships are made by keys
- Strong data integrity
- Transactional reliability
- ACID properties
- On a relational databases, a table represents an entity, a column represents an attribute of this entity and a row is the data itself
- Using primary and foreign keys ensures consistency between relationships on the tables, and it’s made by the DBMSs, which serve as the software to enable efficient data storage, retrieval and management

### Database Management System

- Software that enables database creation, organization, management and manipulation, providing an interface and tools for the users, allowing data storage, retrieval, modification and deletion
- Primary Functions
    - Data definition
    - Data manipulation
    - Data security and integrity
    - Data concurrency and transaction management
    - Data recovery and backup
- DBMS types of language:
    - Data definition language (DDL)
    - Data manipulation language (DML)
    - Data control language (DCL)
    - Transaction control language (TCL)
- Most common DDL commands
    - `CREATE`
    - `DROP`
    - `ALTER`
    - `RENAME`
    - `TRUNCATE`
    - `CONSTRAINT`
    - `INDEX`
- Most common constraints
    - *Primary key*
    - *Foreign Key*
    - *Unique*
    - *Check*
    - *Not null*

### Common Table Expressions (CTE)

- Tool that act as a temporary result set, simplifying  complex queries and improve query maintainability
- CTEs allow us to tackle complex problems by breaking them into smaller, more manageable pieces, organizing and structuring our queries with more modularly and readably

```sql
WITH cte_name (column1, column2, ..., columnN) AS (
 -- Query definition goes here
)
SELECT column1, column2, ..., columnN
FROM cte_name
-- Additional query operations go here
```

### Window Function

- Tool that improves efficiency and reduces query complexity when analyzing partitions or windows of a dataset
- Avoid the use of complicated subqueries