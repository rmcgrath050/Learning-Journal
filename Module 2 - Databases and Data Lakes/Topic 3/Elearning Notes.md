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


