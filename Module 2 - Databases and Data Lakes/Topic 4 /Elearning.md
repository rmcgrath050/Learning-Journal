14/11/25 2 hours completed 

# Topic 4 - Database Administration and Optimisation


## Choosing the right Database Management System (DBMS)

- Scalibility : Scalability refers to the ability to handle increasing data volumes and user loads
- Performance : Performance focuses on efficient query processing and response times
- Data Consistancy : ensures data integrity and consistency across the database
- Transaction : support handles concurrent transactions and maintains data consistency

Also inportant to consider:
- data structure and relationships
- Expected data volume and growth
- Query patterns and performance expectations
- Consistency and availability trade-offs.

Designing for scalability and performance involves considering:
- Data volume and growth rate,
- Query patterns and performance,
- Partitioning and sharding,
- Caching mechanisms,
- Monitoring and performance tuning

Estimating current data volume and expected growth helps in planning for storage capacity and scalability, 
while considering data archival and retention strategies. 

Analysing common query patterns and their frequency, identifying performance-critical queries, 
and optimising queries through indexing, normalisation, and query rewriting are crucial for ensuring optimal performance.


### Performance Metrics
- Poorly formatted or overly general queries can introduce slowdowns
- user/query conflicts : Slowdowns can occur when multiple users are accessing the database.
- Business transactions : Look at end-user experience of real-time performance
- Capicity : Consider CPUs, disk performance, memory, configurations and network connections.
- Configuration : Be sure to change default settings for elements like buffer and query caches.


### 6 Tips to Increase Database Performance
- Optimise Queries
- Improve Indexes
- Defragment Data
- Increase Memory
- Strengthen CPU
- Review Access


Partitioning and sharding techniques distribute data across multiple nodes or servers, 
either through horizontal partitioning (sharding) based on a key or range or vertical partitioning based on columns or data types.


 Caching mechanisms, such as implementing caching layers (e.g., Redis, Memcached) 
 and storing frequently accessed data in memory, reduce database load and improve response times.
 
 Regular monitoring of database metrics, identifying performance bottlenecks and slow queries, 
 tuning database parameters and configurations, and analysing and optimising query execution plans 
 are essential for maintaining optimal performance!!

 ## Secuirty 

 Access controls and authentication mechanisms, such as setting up user accounts and roles, 
 implementing strong authentication, and restricting access based on the principle of least privilege, 
 help in securing the database. 
 
 <b>Role-based access control </b>(RBAC) allows defining user roles and permissions, 
 granting access based on user roles and responsibilities, and regularly reviewing and updating role assignments.

 <b>Data encryption</b>, using strong encryption algorithms and key management, protects sensitive data at rest and in transit, 
 mitigating the risk of unauthorized access and data breaches. 

 <b> Data Integrity Verfication </b>
 Implementing regular data backups, testing backup integrity and restore procedures, 
 establishing a disaster recovery plan, and ensuring data availability and minimising downtime are essential 
 for data protection and business continuity. 



 <img width="708" height="624" alt="image" src="https://github.com/user-attachments/assets/39d85921-dfd6-4e07-8954-cdc88828d44e" />

<br>
<br>


## Lession 3: SQL and NoSQL Databases

SQL databases are like buses, providing a structured and reliable way to transport data, 
while NoSQL databases are like off-road vehicles, offering flexibility and adaptability for handling diverse and unstructured data.

SQL databases are based on the relational model, where data is organized into tables with predefined schemas. 
Tables consist of rows (records) and columns (fields), with each column having a specific data type. 

SQL databases enforce <i>ACID </i> properties ensuring:
- Atomicity : Transactions are treated as a single unit of work
- Consistancy : Database remains in a consistent state before and after transactions
- Isolation : Concurrent transactions are isolated from each other
- Durability : Committed transactions are permanently stored


### SQL in a nutshell 


<img width="558" height="284" alt="image" src="https://github.com/user-attachments/assets/3069979c-4a81-4c9c-bdd0-53d2eadfe33e" />

### No SQL in a nutsell

- key thing here is that Offer a flexible schema, allowing for dynamic and evolving data structures. They follow a schema-less or schema-on-read approach
  <br>
  <br>



<img width="660" height="390" alt="image" src="https://github.com/user-attachments/assets/567faaa1-0038-47df-afd4-95c717fc87bb" />



## Database Changes: Impacts and Costs 

- Data Stream: Changes in upstream database systems can impact downstream applications and data consumers.
- Schema : Schema changes, such as adding or modifying columns in SQL databases, may require updates to downstream applications, whereas NoSQL databases have more flexibility to accommodate schema changes.
- Data format changes, such as introducing new data types or changing data representations, may impact data processing pipelines, requiring data engineers to assess the impact and coordinate necessary adaptations
- Performance optimisations, like indexing or partitioning changes, can affect query performance and resource utilisation

- Processing and Storage costs:
Processing and storage costs vary between SQL and NoSQL databases. SQL databases typically have lower storage costs due to efficient storage of structured data but can have higher processing costs for complex queries involving joins and aggregations. NoSQL databases may have higher storage costs due to the overhead of storing unstructured or semi-structured data but often have lower processing costs for simple queries and high-volume data ingestion. Factors affecting costs include data volume and growth rate, query complexity and frequency, indexing and partitioning strategies, hardware and infrastructure requirements, and licensing and support costs.


## Lession 4: Monitoring and Optimising Database Performance

Monitoring key data access metrics is crucial for ensuring database performance and identifying potential bottlenecks.

### Monitoring Techniques for Data Engineering: 

<b>Query response time</b><br>
Measures the time taken to execute and return the results of a query, 
helping identify slow-running queries that may impact overall performance and optimize query execution and indexing strategies.

<b>Throughput</b><br>
Tracks the number of queries or transactions processed per unit of time,
measuring the system's capacity to handle a certain workload and identifying performance bottlenecks and scaling requirements.

<b>Concurrency</b><br>
Monitors the number of concurrent users/ connections accessing the database,
ensuring the database can handle the expected level of concurrency (handle mutiple tasks at 1 time)
and identifying contention issues and optimising resource allocation.

<b>Resource Utilisation </b><br>
include CPU usage, which monitors the utilisation of CPU resources by the database processes, memory usage, which tracks the memory consumption of the database and its components, 
and disk I/O, which measures the read and write operations performed on the storage disks. 
These metrics help in identifying resource-intensive queries and optimising system resources

<b>Indexing </b><br>
Indexing effectiveness analyses the usage and performance of indexes, identifies missing or inefficient indexes that
impact query performance, and helps optimise indexing strategies based on query patterns.


## Monitoring tools 

Various monitoring tools and techniques are available for database performance monitoring. 
Most database management systems provide built-in monitoring and profiling tools, such as Oracle Enterprise Manager, SQL Server Management
Studio, and MySQL Workbench, offering insights into database performance, query execution, and resource utilisation. 
Third-party monitoring solutions also offer comprehensive monitoring, alerting, and reporting capabilities.

<b>In your learning journal, research the third-party database monitoring solutions that your company uses.</b>


#### Query profiling
Query logging and analysis, also known as query profiling,  involves examining executed queries from users and their 
performance metrics, analysing query logs to identify slow queries, inefficient patterns of usage, and opportunities for improving things 
such as rewriting queries or reshaping tables.
Regular performance reviews are conducted to assess database health, identify improvement areas, analyse trends, identify bottlenecks, 
make data-driven optimization decisions, 
and collaborate with stakeholders to align performance goals with business requirements.

#### Indexing strategies
Database performance optimisation techniques also include indexing strategies, database configuration tuning, horizontal scaling (sharding), and vertical scaling (adding more computing resources). Indexing strategies focus on creating appropriate indexes on frequently queried columns, choosing the right index types based on data characteristics and query patterns, and monitoring index usage and performance to identify redundant or underutilised indexes.

#### Database configuration
Database configuration tuning involves adjusting database configuration parameters to optimize performance, such as memory allocation, buffer sizes, caching mechanisms, and parallelism settings, based on workload characteristics and hardware resources.
Horizontal scaling (sharding) distributes data across multiple database instances or servers, partitioning data based on a key or range to distribute the workload and enable parallel processing and improved scalability for large datasets.

#### Collaboration
Collaboration between data engineers and database administrators (DBAs) is essential for smooth integration and optimization of databases within the data ecosystem.  Data engineers focus on data pipelines, data integration, and overall data architecture, while DBAs specialize in database management, performance tuning, and security. 
Effective communication, regular discussions on database requirements, performance goals, and optimization strategies, and collaboration on database design, schema changes, and migration plans are crucial.
Knowledge sharing, conducting joint performance reviews and analysis sessions, and continuously learning from each other's expertise help improve overall database management.


## How to optimise your database 

### Indexes

When you index your data, it helps reduce the amount of I/O required to retrieve information from your tables.It also improves performance by reducing the number of disks required to read disk data.

But it is recommended that you create an index for tables containing lots of columns, those most commonly used, and those with high cardinality. (An example of a data table column with high-cardinality would be a USERS table with a column named USER_ID. This column would contain unique values of 1-n)

Indexes are different ways to speed up searches in a table.
Different indexes help with different kinds of searches.
If two indexes are the same, you only need one.
Use whichever index performs best.



### Database Size

If you do not plan to add any new data to your database, then it is recommended that you do not increase the size of your database. Increasing the size of your database will cause additional I/O operations which can affect performance.

I/O operations means Input/Output operations — basically any time your database has to read data from storage or write data to storage.
<br>
Think of it like this:
Reading from the database = input
Writing to the database = output
<br>
These actions take time because the storage device (like an SSD or hard drive) has to do the work.

When it comes to keeping a smaller database size, the other important reason is that it is recommended that you reduce the fragmentation. You should also ensure that performance is maintained by avoiding index fragmentation and file fragmentation.

Index fragmentation – this happens when the index (your search shortcut) becomes messy and unorganized.
File fragmentation – this happens when the actual database file gets stored in pieces across the disk.
<br>

Index fragmentation occurs when all the rows in an index become fragmented into different pages due to their sizes. For example, if there are two columns in an index, one column has 100 rows while another has 50 rows.

File fragmentation occurs when the files are filled with different pages due to the large data size. For example if a database file grows too big to fit in one continuous space on the disk, the operating system stores its pages in multiple separate locations, causing the file to become scattered across the disk.

### Mutiple Tables

Do not create too many small tables when they represent the same type of data.
If you split related data into too many tables, you'll need separate indexes for each one, which hurts performance and complicates your design

Your goal is to reduce operational expenses by reducing your cluster resources (CPUs, memory, disk space), changing your instance configuration (RAM, CPU cores, disk size), or reducing storage requirements (disk space).

Your “cluster” is the group of servers running your database.
You can save money by using smaller or fewer servers:
- CPUs → the processing power (like the brain of the computer)
- Memory (RAM) → short-term storage used to run tasks quickly
- Disk space → long-term storage where your data/files live

Reduce storage requirements (disk space)
This means:
- Storing less data
- Cleaning old logs
- Compressing data
- Deleting unused backups
- Using more efficient storage formats

### Truncate Table

Don’t split a single record into many tiny rows just because you have many columns. In other words: <br>
❌ Don’t store what should be one row as many separate rows <br>
✔️ Keep related data in one row if they belong together <br>

### Reduce Table Size

If you have been using the same table for a long time, then it is recommended that you should consider reducing the size of your table. Reducing the size of your table will cause fewer I/O operations and fewer disk seeks to retrieve data from the disk.

### Use Auto-Increment Columns

If there are several columns in a single table, it is recommended that each of these columns have an auto-incrementing ID. Thus, it would be unique.
This would help improve performance by eliminating duplicate IDs when rows are inserted into a table

### Enable Statistics

When a new query or statement is executed against a database, then statistics are calculated and stored in memory by default. This helps improve performance by reducing I/O operations.

Statistics are calculated
The database collects some information about your data, like:
1. How many rows are in a table
2. How many distinct values are in a column
3. How data is distributed (e.g., 90% of customers live in one city)
<br>
These are called statistics.
<br>
- Stored in memory
- The database keeps these statistics in RAM (fast memory) instead of constantly reading from disk.
- Improves performance / reduces I/O operations
- If the database already knows statistics, it doesn’t have to scan the entire table from the disk every time.
Fewer disk reads = faster queries.

<br>
Use statistics most of the time, especially when:
- Your tables are large
- Your queries involve filters, joins, or sorting
- You want the database to automatically choose the fastest query plan

<br>
Reasons for disabling statistics:
- Tables are very small → scanning the whole table is already fast
- Memory is very limited, and keeping statistics in RAM could use valuable resources
- doing high-frequency bulk inserts/updates and statistics are constantly changing, which could slow down operations!

<br>
Example:<br>
1. A logging table that just keeps growing with new entries and is rarely queried by complex filters.
2. You don’t need statistics because queries just read the newest rows sequentially.


### Scenario of real life example:
1. slow query response times and struggles to handle the growing data volume. 
2. Performance analysis reveals high CPU utilisation and slow query execution times, with inefficient queries containing complex joins and lacking proper indexing.

Solution:<br>
- NoSQL quality and performance optimisation techniques, such as denormalisation, indexing, and sharding, are applied to address the performance issues.
- Monitoring and fine-tuning the database configuration lead to improved query response times and resource utilisation.
<br>


Outcome:<br>
faster data retrieval, efficient reporting, and seamless integration with other HR systems, enhancing overall productivity and decision-making capabilities. 



## Summary 
- Choose the right DBMS based on factors like scalability, performance, data consistency, and transaction support, considering the differences between SQL and NoSQL databases.
- Design databases for scalability and performance by considering data volume, growth rate, query patterns, partitioning, sharding, caching, and regular monitoring and tuning.
- Implement robust security measures, including access controls, authentication, role-based access control, data encryption, regular patching, and comprehensive backup and recovery procedures.
- Monitor key data access metrics, such as query response time, throughput, concurrency, resource utilisation, and indexing effectiveness, using various tools and techniques.
- Optimise database performance through query optimisation, indexing strategies, configuration tuning, horizontal scaling (sharding), and vertical scaling.
- Foster collaboration between data engineers and database administrators through effective communication, knowledge sharing, and joint performance optimization efforts.

  





