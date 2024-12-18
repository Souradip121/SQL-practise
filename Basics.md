# Basics of DBMS and SQL

## Table of Contents
1. [Introduction to Databases](#introduction-to-databases)
2. [Database Management Systems](#dbms)
3. [Types of Databases](#database-types)
4. [SQL Fundamentals](#sql-fundamentals)
5. [Database Design](#database-design)

## Introduction to Databases

<details>
<summary>What is a Database?</summary>

A database is an organized collection of data stored electronically. Think of it like a digital filing cabinet.

**Real-world analogies:**
- Library catalog 📚
- Phone contacts list 📱
- School records system 🎓

**Key characteristics:**
- Structured data storage
- Easy retrieval
- Data integrity
- Concurrent access
- Data security
</details>

<details>
<summary>Why Use Databases?</summary>

Instead of using spreadsheets or files, databases offer:

1. **Data Independence:** Applications don't need to know how data is stored
2. **Data Integrity:** Rules ensure data accuracy
3. **Concurrent Access:** Multiple users can access simultaneously
4. **Data Security:** Control who can see or modify data
5. **Data Recovery:** Backup and restore capabilities
</details>

## DBMS

<details>
<summary>Database Management Systems Explained</summary>

A DBMS is like a supervisor that manages all database operations.

**Core Functions:**
- Data storage and retrieval
- Security and authorization
- Backup and recovery
- Transaction management

**Popular DBMS Software:**
```
Relational:          NoSQL:
- MySQL             - MongoDB
- PostgreSQL        - Redis
- Oracle            - Cassandra
- SQL Server        - CouchDB
```
</details>

## Database Types

<details>
<summary>Types of Databases</summary>

### 1. Relational Databases (RDBMS)
```sql
-- Example table structure
CREATE TABLE Students (
    StudentID INT PRIMARY KEY,
    Name VARCHAR(50),
    Age INT
);
```

### 2. NoSQL Databases
```json
// Document store example (MongoDB)
{
    "studentId": 1,
    "name": "John Doe",
    "age": 20,
    "courses": ["Math", "Physics"]
}
```

### 3. Graph Databases
Used for connected data like social networks

### 4. Time-Series Databases
Perfect for IoT and monitoring systems
</details>

## SQL Fundamentals

<details>
<summary>Basic SQL Commands with Examples</summary>

### SELECT Statement
```sql
-- Basic query
SELECT * FROM Students;

-- With conditions
SELECT name, age 
FROM Students 
WHERE age > 18;

-- With sorting
SELECT name, grade 
FROM Students 
ORDER BY grade DESC;
```

### INSERT Statement
```sql
INSERT INTO Students (name, age)
VALUES ('John Doe', 20);
```

### UPDATE Statement
```sql
UPDATE Students 
SET age = 21 
WHERE name = 'John Doe';
```

### DELETE Statement
```sql
DELETE FROM Students 
WHERE age < 18;
```
</details>

## Database Design

<details>
<summary>Database Design Principles</summary>

### 1. Entity Relationship Diagrams
```
[Students] 1---* [Enrollments] *---1 [Courses]
     |                                  |
     |                                  |
     *                                  *
[Addresses]                        [Professors]
```

### 2. Normalization Rules
- **First Normal Form (1NF)**
  - No repeating groups
  - Atomic values

- **Second Normal Form (2NF)**
  - Must be in 1NF
  - No partial dependencies

- **Third Normal Form (3NF)**
  - Must be in 2NF
  - No transitive dependencies

### 3. Keys and Relationships
- Primary Keys
- Foreign Keys
- Composite Keys
- Candidate Keys
</details>

<details>
<summary>Best Practices</summary>

1. **Naming Conventions**
   - Use meaningful table and column names
   - Be consistent with capitalization
   - Avoid reserved words

2. **Data Integrity**
   - Use appropriate data types
   - Implement constraints
   - Define relationships properly

3. **Performance**
   - Index frequently searched columns
   - Optimize queries
   - Regular maintenance
</details>

## Practice Exercises

<details>
<summary>Basic Database Operations</summary>

1. Create a simple students database
2. Add student records
3. Query student information
4. Update student details
5. Delete student records

```sql
-- Example Exercise
CREATE TABLE Students (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    email VARCHAR(100)
);

-- Practice inserting data
INSERT INTO Students VALUES (1, 'John', 'john@email.com');

-- Practice querying
SELECT * FROM Students WHERE id = 1;
```
</details>

## Additional Resources
- 📚 Books: "Database System Concepts" by Silberschatz
- 🎥 Video Tutorials: [SQL Tutorial - Full Database Course for Beginners](https://www.youtube.com/watch?v=HXV3zeQKqGY)
- 💻 Practice: [SQLZoo](https://sqlzoo.net/), [HackerRank SQL](https://www.hackerrank.com/domains/sql)
- 🔗 Documentation: [MySQL Docs](https://dev.mysql.com/doc/), [PostgreSQL Docs](https://www.postgresql.org/docs/)
