18/11/25

# NoSQL 

In a JSON object usually has an array of categories,
Made up of keys and values - a key can have more than one value also , this would be added by an additional nested object 

Curry bracket -  main JSON object
Square bracket - Array of objects

Json also used double quotes to declare Strings

## SQL Databases 

Relational databases - the ‘TABLE’ itself should be related ( not just one common key) 

A table is represented by a two-dimensional table: each column represents a data item, each row represents an observation.

### Why is SQL not sufficient

Not flexlexible , 
big data 


### Enter NoSQL
<br>
<img width="404" height="324" alt="image" src="https://github.com/user-attachments/assets/a9af04c6-ad0b-4972-9fcc-ff5c7f0500c4" />
<br>
<br>
<br>

<img width="546" height="434" alt="image" src="https://github.com/user-attachments/assets/68eb7ad2-9147-4df7-b5ed-c88e8705b750" />

## Major types of NoSQL databases
<br>
<img width="596" height="272" alt="image" src="https://github.com/user-attachments/assets/085e269e-1a75-4e77-8cc0-7fbb52d69fb8" />

Json files - easy to read from memory<br>
Document Based - Nicer format to store this type of information<br>
Column based - nearest design to a table , usually row is the information is where information is stored, however stored vertically in columns instead<br>
Graph - use nodes as points of interest, data stored in attributes 


### Why is SQL not sufficient

Not flexlexible , 
big data 

## Drawbacks of NOSQL
- Merges between different tables are difficult to perform
- Therefore data not stored in a normalised way ( denormalisation)

### Redis
- Fast return and information, don’t have to worry about high complexity 
- Redis is an in memory database - everything stored in RAM 
- Therefore reading and writing extremely fast

### Column-based database

When you should use them…
- Optimised for data warehousing: Ideal for managing
and querying large volumes of data efficiently,
particularly in analytics and reporting.
- Real-time big data analytics: Facilitates rapid
analysis and reporting, crucial for applications like
financial trading and web analytics.
- Scalability and flexibility: Excellently suited for
scalable, cloud-based applications with variable
workloads due to efficient data distribution capabilities.
- Efficient sparse data management: Highly effective
in handling datasets with many empty or null fields,
common in telecommunications and IoT.

## MongoDB

##### What is a document 
- an obseration of data 
- think of a row in a classic table, a row of information
- collection is a bunch of rows and have them in a block
  
#### When to use them
- the schema is not clear in advance
- dump data fast
- also useful for search for exactly one record
- not suitable for complex queries


<br>
<img width="405" height="327" alt="image" src="https://github.com/user-attachments/assets/0b22e53e-f7d3-443d-a079-1a6e55910f93" />
<br>
<br>

<b>Remember <b/b>
- no schemas, no transaction or no joins
- also no max documnet exceeding 16gb?
- Monddb data is stored as BSON (Binary jason) - which is used for speed
- Runs on most common operating systems


- pymungo is used a library , base knowledge of phyton required
- 





 



