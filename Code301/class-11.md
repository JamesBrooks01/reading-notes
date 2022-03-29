# Reading Assignment 11

## Mongo and Mongoose

---

### NoSQL vs SQL

---

- SQL vs NoSQL
  - SQL
    1. Relational Database
    2. Table-Based
    3. Pre-Defined Schema
    4. Vertically Scalable, or Scaled by increasing the power of the hardware
    5. More Designed Complex Queries
  - NoSQL
    1. Non=Relational or Distributed
    2. Document-Based Key-Value Pairs, Graphs or Wide-Column Stores
    3. Dynamic Schema
    4. Horizontally Scaleable, or Scaled by increasing the number of servers available to reduce the load
    5. More Designed for large data sets.
- What kind of data is a good fit for an SQL database?
  - An Intensive & Complex Query Enviroment
- Give a real world example.
  - Oracle
- What kind of data is a good fit a NoSQL database?
  - High-Volume, Hierarchy Based Data Storage
- Give a real world example.
  - MongoDB
- Which type of database is best for hierarchical data storage?
  - NoSQL
- Which type of database is best for scalability?
  - Both scale in different ways. SQL is scaled with the power of the individual server, while NoSQL is scaled with the number of servers.

### SQL vs NoSQL Video

---

- What does SQL stand for?
  - Structured Query Language
- What is a relational database?
  - A Database that uses SQL and is based on tables.
- What type of structure does a relational database work with?
  - Tables; otherwise called Logical Data Structures.
- What is a ‘schema’?
  - The structure that the Database follows.
- What is a NoSQL database?
  - A non-table based database that stores data in documents.
- How does it work?
  - By using collections of data with no set schema
- What is inside of a Mongo database?
  - Collections of data organized like JSON data with key-value pairs.
- Which is more flexible - SQL or MongoDB? and why.
  - MongoDB because while it's NoSQL basis has it's limitations, it allows for a greater amount of data and the ability to store it in a less restictive manner because it doensn't rely on relations for data.
- What is the disadvantage of a NoSQL database?
  - Without Schema, the layout of data can be inconsistent and without relations, there could be duplicate data within the database and if data is needed in multiple places, any update must manually be updated for each instance.
