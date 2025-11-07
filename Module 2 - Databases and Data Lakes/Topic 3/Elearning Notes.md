# TOPIC 3 : Advanced SQL


## Lession 2: Impacts of upstream data modelling on downstream experience

5 things to ask before pushing schema change to production

1. Is a change management process embedded into your data engineering workflow?
2. What is the structure of your data organisation?
3. What impact up and downstream will the schema change have?
4. How will you communicate schema changes with the broader data team?
5. Are you measuring the impact of change management on your organisation?

For instance, if the database schema is modified to split employee benefits into multiple categories, existing SQL queries in downstream applications might no longer return correct results unless they are also updated to reflect these changes. This scenario underscores the necessity of employing advanced SQL features like views and stored procedures to ensure seamless transitions and uninterrupted service delivery.


Views in a Database Management System (DBMS) are virtual tables that do not store data physically; instead, they are defined by a query that pulls data from one or more underlying tables. They are essentially saved SQL queries that appear as virtual tables within a database. Views can be used for various purposes, such as simplifying complex queries, providing a layer of security, or presenting data in a different format from the actual table structure.


A stored procedure is a prepared SQL code that you can save, so the code can be reused over and over again. So if you have an SQL query that you write over and over again, save it as a stored procedure, and then just call it to execute it.

A view can contain all or some of the rows and columns of the base tables, depending on the query that defines the view. A view can also have additional columns that are computed from the base table columns.

What is a Stored Procedure? 
Also known as a stored proc, or a sproc, a stored procedure is a prepared SQL code. It is a user-created code snippet that Data Engineers upload to a database to  make it automatically perform a set of SQL queries and logical operations. The procedure is stored in the database. It saves you time as the code can be reused over and over again. 
Remember that most SQL operations in stored procedures are so-called CRUD operations. 

Additionally, triggers can be set up to automatically update audit logs whenever changes are made to sensitive employee data, thus supporting compliance with data protection regulations.


## Lession 3 : The importance of good data modelling

Data modelling is the process of creating a visual representation of a system or database, where data objects are defined and relationships between these objects are established. It involves the careful design of data structures and schema to ensure data integrity, efficiency in data handling, and alignment with business requirements. 
This process helps in organising data as well as promoting a clear understanding of the data flow across systems, which is crucial for effective database and application design.

### Conceptual Data Model
This model provides a high-level overview of the database without delving into technical details. It focuses on the broad structure of the database and the relationships between major entities in the system. It is often used for initial planning and agreement between stakeholders on the major entities and relationships in the system.

### Logical Data Model
This model describes the data in more detail but without concern for how they will be physically implemented in the database. It includes all entities, their attributes, and relationships, along with key constraints that should apply. It is used to translate the conceptual model into a more technical blueprint that database designers can understand and use

### Physical Data Model
This model outlines how the database will be physically realised on the storage system. It details the complete structure of the database, including tables, columns, data types, constraints, indexes, and how they are physically stored on disk. This model is used to build the actual database according to the specified performance, security, and storage requirements.

##### Database triggers:
Database triggers are procedures that automatically execute in response to specific events on a particular table or view in a database.
They are used to maintain the integrity of the data across complex business rules and relationships.

##### Views:
Views are virtual tables based on SQL queries. They allow users to structure data in a way that that the user reqires, implementating business requires while  hiding the complexity of the database schema.

##### Stored procedures:
SQL code that you can save, so the code can be reused over and over again. They can perform complex operations, from data validation to batch processing with conditional logic, and can reduce traffic between an application and the database server by bundling commands.

##### Normalisation:
Normalisation is a systematic approach of decomposing tables to eliminate data redundancy (repetition) and undesirable characteristics like Insertion, Update, and Deletion Anomalies. It is a multi-step process that puts data into tabular form by removing duplicated data from the relational tables. Normalisation helps to reduce redundancy and dependency by organising fields and table of a database.

##### Redundancy:
In the context of database management, redundancy occurs when the same piece of data is stored in two or more separate places, either within the same database or across multiple databases. Redundancy can lead to inconsistencies during data updates, increased storage requirements, and unnecessary complexity in data handling. While sometimes used intentionally for improving data retrieval performance and ensuring data availability, redundancy often requires careful management to avoid data integrity issues.


##### Comprehensive Data Types:
These are specific kinds of data attributes that define the kind of data a column can hold in a database. They help in accurately describing the data characteristics, such as integers, decimals, dates, or strings, ensuring that data inputs are processed and stored correctly.

##### Redundancy:
Constraints in a database ensure the accuracy and reliability of the data in the database. They enforce rules on the data fields, such as primary keys, foreign keys, unique, not null, and check constraints, to maintain data integrity and enforce business rules.

##### Indexing Strategies:
These are plans or methods implemented to improve database performance. Indexing strategies involve creating indexes on tables to speed up the retrieval of rows at the cost of additional writes and storage space to maintain the index data structures.

##### Indexing:
Indexes are special lookup tables that the database search engine can use to speed up data retrieval. Simply put, an index in a database is similar to an index in the back of a book.

##### Database Business Requirements:
These are specifications derived from business needs that outline what the business intends to achieve with the database. These requirements focus on what data needs to be stored and how it will be used to support business processes.

##### Database User Requirements:
These are detailed requirements that describe what the end-users need the database to do, from how data should be input, to how it should be manipulated, accessed, and presented. These are more focused on the usability and functionality of the database from the user's perspective.


## Lession 4: ACID and the Importance of Transactions

The ACID properties (Atomicity, Consistency, Isolation, Durability) provide a foundation for reliable database transactions, ensuring that all operations within a transaction are completed successfully or not at all. 

This framework is essential in environments where data accuracy and reliability are paramount, such as financial systems, e-commerce platforms, and other business-critical applications.

#### Atomicity
Transactions are all or nothing.
Atomicity guarantees that each transaction is treated as a single unit, which either succeeds completely or fails completely.
eample includes begin/ rollback 


