14/11/25 10:38

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




