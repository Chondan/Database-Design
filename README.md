# Database Design

## What is database?

- something that store data
- Spread sheet vs. Database
	- flexibility
	- accessibility

---

## Relational Database

- Relation -> connection between datas
- Terms
	- entity -> What we store data about?
		- 1 row (tuple) in a table represent an entity
	- attribute -> What we store?
	- attribute type -> table (store the same type of entities)

---

## RDBMS

- What is DBMS? -> a tool helping us working with data easily e.g. do a query to get a set of data
- view machanism -> get different views of the data (security feature)

---

## SQL

- SQL
	- DDL -> Define the structure of database e.g. table structure, relationship between tables
	- DML -> Manipulate data within the database

---

## Naming Convention

> Pattern that people do to keep things consistent

- use uppercase for SQL command e.g. "SELECT col1 FROM table"
- use lowercase for other e.g. "user" table, "user_id" attribute

---

## Database Design

- How to measure wheter database is good or bad?
	- Data Integrity -> all of your data is correct, up to date and there is no disconnect data.
- Schemas -> tell the way data is constructed
	- Conceptual Schema -> how data is related?
		- e.g. 'user' <---- 'sale' (sale depends on user)
	- Logical Schema -> relationship between data
		- e.g. 'user' can have multiple 'sale' and 'sale' can only have one 'user' (user 1 ---> m sale)
	- Physical Schema -> start implementing into the database

---

## Data Integrity

- We want a correct data in the database
	- we don't want 'repeating' value
	- we don't want 'incorrect' value
	- we don't want 'broken relationship' between tables
- Entity integrity -> unique entity
	- add more column to make each row in the table uniqueness e.g. 'id'
- Referential integrity -> relationship
- Domain integrity -> the exceptable value for column (the range of data accepting to store)
	- e.g. 'phone' column must be stored with 10 digits
	- Data Type
		- e.g. 'char(20)' -> "I like pizza"

---

## Database Terms

- Data
- Database
- Relational Database -> store in a table
- Database Management System (DBMS) -> control database
- RDBMS
- Null -> there is no data in a spcific field
- Anomalies -> errors within datas in data integrity
- Integrity
	- Entity -> uniqueness among the table 
	- Referential -> keep the connection across multiple table
	- Domain -> a column within a table has all of the expected value
- Entity -> anything we store data about
- Attributes -> thing we store about entity
- Relation -> a connection between set of data (table)
- Tuple -> a row in the table
- Table (File)
	- Rows (Record, Entry)
	- Columns (Field)
	- value -> data we put into the specific column
- Database Design -> the process to design a database in oder to remove anomalies and have data integrity
- Schema -> structure of a database
- Normalization -> a bunch of steps that we are going to follow to help us get the best database design
- Naming Convention
- Keys -> something to make everything unique within a table

---

## More Databaes Terms

- SQL (Structure Query Language)
	- DDL (Data Definition Language)
	- DML (Data Manipulation Language)
	- SQL Keywords -> e.g. SELECT, UPDATE, etc.
- Frontend -> what the users see
- Backend -> what going on behind the scene
- Client Side
- Server Side
- Server Side Scripting Language
- Views -> take datas in the database and illustrating in the different ways
- Joins -> connect data from multiple table to create a new table

---

## Atomic Value

> Everything we store in a database should be 1 thing. The smallest individual thing to store.

- Example
	- "Firstname Lastname" -> should split these 2 value into "Firstname" and "Lastname"
	- "address" column should be broken into multiple columns instead of storing all of information in only one column

---

## Relationships

- 1 to 1 (1 -> 1)
- 1 to many (1 -> m)
- many to many (m -> n)
	- Design -> create an intermediatly table and then break the relationship to "1 to many" on one side and "many to 1" on the other side

---

## Parent Tables and Child Tables

- Parent -> PK
- Child -> FK and point back to the parent

---

## Look up Table

A lookup table is normally a table that acts as a "master list" for something and you use it to look up a business key value.

---

## Keys

- Primary key
	- Unique
	- Never changing
	- Never null
- Super key
- Candidate key
- Alternate key -> candidate keys that not use as the main key of the table
- Foreign key
- Surrogate key -> no real world value or no real world meaning e.g. userID, songID, and etc.
- Natural key
- Simple 
- Composite (multiple column keys)
- Compound (multiple column keys and all of them are candidate keys)

---

## Cardinality



---

## Normalization

- 1NF
	- Primary key (no duplicate tuples)
	- No repeating groups
	- Atomic columns (cells have single value)
- 2NF
	- Be in 1NF
	- No partial functional dependencies of non-prime attributes on candidate keys
- 3NF
	- Be in 2NF
	- No transitive functional dependencies of non-prime attributes on candidate keys

---

## Indexes (Clustered, Non-clustered, Composite Index)

- Clustered Index
	- A type of index which sorts the data rows in the table on their key value.
	- There in only one clustered index per table.
- Non-clustered Index
	- A Non-clustered index stores the data at one location and indices at another location.
	- A single table can have many non-clustered indexes as an index in the non-clustered index is stored in different places.
- Composite Index
	- The columns used in composite indices are concatenated together, and those concatenated keys are stored in sorted oder using a B+ Tree.

---

## Data Types

- 3 main data types
	- string
	- numeric
	- date 

---

## Joins

- Inner Join
- Outer Join
	- Left Join
	- Right Join
- Self Join

---