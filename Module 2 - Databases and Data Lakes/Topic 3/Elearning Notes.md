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

#### Consistency
Only valid data is saved.
Ensures that any transaction will bring the database from one valid state to another, maintaining all predefined rules, such as unique primary keys, foreign key constraints, and custom constraints.

#### Isolation
Transactions do not affect each other.

#### Durability
Written data will not be lost.
Durability guarantees that once a transaction has been committed, it will remain so, even in the event of a power loss, crashes, or errors

In one scenario, due to a system failure, the transaction was interrupted right after the money was deducted but before it was credited to the other account. Thanks to the atomicity and durability properties, the system was able to roll back the incomplete transaction once the system was restored, thus preventing potential financial discrepancies for the customer and the bank.
eg current lloyds example iclude begin try statements with deployments - making sure tasks are deployed together as a datasource etc


## Lession 5: Writing Nested CRUD SQL Queries

In database operations, mastering CRUD (Create, Read, Update, Delete) functionalities is essential for managing data effectively. When these operations involve complex data relationships or require the evaluation of conditions across multiple tables, nested SQL queries become invaluable. Nested queries, or subqueries, are queries placed within another SQL query, enhancing the flexibility and depth of data manipulation possible within a single statement. These queries are particularly useful in scenarios where the results of one query depend on the data retrieved by another.


While SQL doesn't directly support nested 'CREATE' statements, complex 'CREATE' operations can involve subqueries to define or populate new tables based on existing data. For example, creating a new table that aggregates existing customer data but only includes those who meet certain spending thresholds.

### Understanding Nested and Correlated Queries in SQL

Nested Queries :
Also known as subqueries, nested queries are executed within another query. The inner query runs first, providing results to the outer query.

Correlated Queries 
The inner query depends on the outer query and is executed repeatedly. eg WHERE EXISTS (SUBQUERY)

<b>Differences:</b><br>
Execution: Nested queries run once; correlated queries run for each outer row.
Performance: Correlated queries can be slower due to multiple executions. 
Dependency: Nested queries are independent; correlated queries rely on the outer query. 

<img width="758" height="342" alt="image" src="https://github.com/user-attachments/assets/aaec7643-8b8e-45f2-86e3-9a89ec03d6d5" />


- Correlated queries are resource-intensive and may be slower.
- Consider rewriting correlated queries as joins for efficiency.
- Use correlated queries for complex conditions involving row comparisons.
- Understanding and using these queries effectively can improve database query performance.

basically dont use correlated where possible as it performs the query by a row by row basis! 

## Lession 6 : Joins and Database Normalisation

oins allow for the combination of data from two or more tables based on a related column between them, enabling complex queries across a database. Database normalisation, on the other hand, is a systematic approach to reducing redundancy and dependency by organising fields and table relationships. It involves dividing large tables into smaller, less redundant tables and defining relationships between them to increase the coherence and efficiency of the data.


1NF: Ensures all columns hold atomic values and each record is unique.
2NF: Requires that all non-key attributes are fully functional dependent on the primary key.
3NF: Ensures that no transitive dependencies exist between non-key attributes and the primary key.


#### Key Concepts:
- Join : A SQL operation used to combine rows from two or more tables based on a related column between them.
- Normalsation : The process of organising data in a database to reduce redundancy and improve data integrity.
- Functional Dependancy : A relationship that exists when one attribute uniquely determines another attribute.
- Transitive Dependancy : A functional dependency in which one attribute indirectly determines another attribute through a third attribute.
  eg recurisve dependancies :)


## Lession 7 : GroupBy, Aggregation, and Windowing in SQL


GroupBy is commonly paired with functions like COUNT, MAX, MIN, SUM, and AVG to perform calculations on each group.
It is possible to group by more than one column, providing a more granular breakdown of data.
Aggregation functions are used to compute a single result from a set of input values. These functions are critical for summarising data, making them indispensable for generating reports and analytics that support business decisions.

#### Windowing Functions

SQL window functions allow performing calculations across a set of rows that are related to the current row, 
without collapsing the result into a single value. They are commonly used for tasks like aggregates, rankings and running totals.
The OVER clause defines the “window” of rows for the calculation. It can:
PARTITION BY: divide the data into groups.
ORDER BY: specify the order of rows within each group.
With this, functions such as SUM(), AVG(), ROW_NUMBER(), RANK() and DENSE_RANK() can be applied in a controlled way.

<img width="500" height="214" alt="image" src="https://github.com/user-attachments/assets/4e7a2c57-3138-4811-8bee-6e05d35c54f1" />
<br>
<br>

#### Over Clause:  
Specifies the partitioning and ordering of a data set before the window function is applied.
  
#### Frame Specification
Allows the window to be defined over a range of rows relative to the current row, providing flexible data analysis options.

Through effective use of GroupBy, aggregation, and windowing, complex datasets can be transformed into actionable insights, enabling businesses to make informed decisions based on comprehensive data analysis. These techniques are vital in leveraging data as a strategic asset within an organisation.

Lession 8 : 


