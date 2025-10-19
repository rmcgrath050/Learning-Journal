# Storing and Querying Data


# Lession 1 : Why businesses are not throwing away data

Historic data paves the way for advanced analytics and big data initiatives, enabling businesses to derive insights from their accumulated data, driving innovation and strategic decisions.

### Chief Data Officer

What they do:
- Lead the data and analytics agenda of an organisation.
- Establish and deliver technologies, tools, approaches and methodologies to unlock the value in enterprise data assets of an organisation.
- Manage data as a strategic asset and operational data governance, data quality and other controls to sustain the integrity of the data of an organisation.
- Serve as trusted partner to key business executives focused on the customer, enterprise risk management, regulatory compliance and finance.
Fosters innovation leveraging emerging Big Data and analytics technologies.

      Q. Who is chief data officer in my area?

### Data Marketplaces

Data marketplaces are online platforms where individuals and organisations can buy, sell, or exchange various types of data. These platforms serve as intermediaries, connecting data providers with data consumers, and facilitating transactions between them.

<b>Examples of Data Marketplaces:</b> <br>
- AWS Data Exchange
- Kaggle Datasets
- Data. world


Consolidation Exercise
- Reflect on the dramatic decrease in storage costs over the decades and the strategic implications of this trend for data-driven decision-making within the context of the HR department.
- Consider how this data-centric approach could be replicated or adapted to enhance decision-making and operational efficiency in other sectors.
- Write a brief analysis in your learning journal, focusing on potential impacts on your organisation.
- Identify a stakeholder in your business from whom you could learn more about the effective use of data.
- Identify a few data sources about competitive trends in the industry, identify the relevant datasets on Google Dataset Search and data marketplaces, and estimate their dataset sizes.
- Also investigate how often this data gets updated and when new data becomes available. Estimate the yearly costs involved in storing this data.

# Lession 2 : Storing Files: HDFS, Key-Value Stores, Columnar – Parquet Format, Filesystems

In Lesson 2, we explore storing files using various systems, from Hadoop Distributed File System (HDFS) to key-value stores and Parquet format. We delve into HDFS's transformative impact on data storage and computation, examine key-value stores' efficiency for rapid data retrieval, and highlight Parquet's advantages for analytical workloads. 

An introduction to Hadoop Distributed File System (HDFS) as a revolutionary technology between 2008-2016, which turned data centres into computing clusters by bringing computation to the data. 

This innovative approach allowed for cheap commodity storage, offering resilience by storing three copies of each file and distribution by ensuring each file resides on at least three different machines. This configuration not only provided a cost-effective solution for managing vast amounts of data but also enhanced data accessibility and analysis capabilities.

### Key-value stores 

Key-value stores offer a straightforward yet efficient method for storing and retrieving data based on a unique key, tailoring their approach for scenarios where quick data access is critical. 

Meanwhile, the Parquet format, designed for efficiency in analytic queries, employs a columnar storage strategy that significantly reduces disk I/O, facilitating faster data processing and enabling schema evolution with minimal overhead.

<img width="696" height="482" alt="image" src="https://github.com/user-attachments/assets/2e6cb21c-bb82-4e34-9556-3893ea3c9dbd" />

<br>
<br>

### Selecting a Storage Format

This section discusses the trade-offs between using Hard Disk Drives (HDDs) and Solid-State Drives (SSDs) for data storage, touching on aspects of speed, durability, and cost. HDDs, with their mechanical parts, are generally more affordable but slower and more prone to failure compared to SSDs, which offer faster data access but at a higher price point. 

The Parquet format, by addressing the need for efficient data analytics through its columnar storage approach, enables organisations to conduct analytic queries more efficiently, leveraging schema evolution to adapt to changing data requirements without significant reengineering.

<img  width="696" height="482" alt="image" src="https://github.com/user-attachments/assets/5581129c-18e5-439d-ba72-fdc06e40786f" />

<br>
<br>
So how does it differ from other file formats? 

CSVS:
Structure - CSV files are plain text files where each line represents a single row of data, and values are separated by commas or other delimiters.
Efficiency - CSV files are simple and easy to read/write but may not be efficient for large datasets or analytical workloads due to their row-oriented structure.
Functionality - CSV files are widely supported and easy to work with in many programming languages and tools. However, they lack built-in support for nested data structures or data types.



JSON:
Structure - JSON files store data in a hierarchical format using key-value pairs, making them suitable for representing nested or complex data structures.
Efficiency - JSON files offer flexibility and support for complex data structures but can be less efficient in terms of storage and processing compared to more optimized formats.
Functionality - JSON files support nested structures and are commonly used for representing semi-structured data. They are well-suited for web APIs and applications where flexibility is important.



Parquet files:
Structure - Parquet files are columnar storage formats, meaning data is stored by column rather than by row. This structure allows for better compression and efficient storage, especially for large datasets with many columns.
Efficiency - Parquet files are highly optimized for analytical queries, as they allow for selective column reads and efficient compression techniques. This results in faster data processing and reduced I/O overhead compared to CSV and JSON files.
Functionality - Parquet files offer advanced features such as schema evolution, predicate pushdown, and efficient encoding schemes. These features make Parquet ideal for data analytics and big data processing frameworks like Apache Spark and Apache Hive.


Consolidation Exercise:
Reflect on how different storage solutions—HDFS, key-value stores, and Parquet—can meet the diverse data storage and analysis needs within your organisation.
Consider the impact of these technologies on data accessibility, analytics capabilities, and overall strategic objectives.
Identify a specific data challenge in your organisation and propose a storage solution that addresses this challenge, outlining the benefits and any potential limitations.

      Q. Would this be compared to current on prem design or would this be with GCP ??

<br>
### Some popular key-value databases include:

Redis - An open-source, in-memory data structure store that can be used as a database, cache, and message broker.
Riak - An open-source, distributed key-value database that is designed for high availability and scalability.
Berkeley DB - A family of embedded key-value databases that are designed for high performance and low-level storage, and are often used in embedded systems and mobile devices.
Memcached- An open-source, in-memory key-value cache that is often used to speed up dynamic web applications by reducing the number of times an external data source must be read.
RocksDB - An open-source, persistent key-value store that is based on LevelDB and is optimized for storage on flash and hard disk drives.
Amazon DynamoDB - A fully managed, highly available, key-value database service that is part of the Amazon Web Services (AWS) ecosystem.
Azure Cosmos DB - A globally distributed, multi-model database service that supports key-value, document, graph, and column-family data models.
Google Cloud Bigtable - A fully managed, high-performance, wide-column NoSQL key-value store that is part of the Google Cloud Platform (GCP) ecosystem.


## Key value database

<b>Caching</b> <br>
Key-value databases are often used as a caching layer in front of a more persistent data store to improve the read performance of an application

<b>Session management</b> <br>
Key-value databases can be used to store user session data, such as login status, shopping cart contents, or other temporary data.

<b>Real-time analytics</b> <br>
Key-value databases can be used to store and process large amounts of data in real -time, such as sensor data, social media feeds and IoT data.

<b>Gaming leaderboards</b> <br>
Key-value databases can be used to store and retrieve high scores and rankings for online games.

<b>Distributed systems</b> <br>
Key-value databases can be used to store data that is distributed across multiple machines, such as distributed hash tables or distributed key-value stores.

<b>Content management systems</b><br>
Key-value databases can be used to store and retrieve content such as images, videos and audio.

<b>Product catalogues</b><br>
Key-value databases can be used to store and retrieve product information, such as description, prices and inventory levels.


<b>The advantages of the parquet format:</b><br>
The Parquet format is designed to bring efficiency to the storage and retrieval of data, particularly for analytical workloads. Its columnar storage format allows for better compression and enhanced query performance by reading only the necessary columns of data, significantly reducing the I/O overhead. Parquet's compatibility with a wide range of data processing frameworks, including Apache Hadoop, Apache Spark, and Amazon Athena, makes it a versatile choice for enterprises looking to optimise their big data analytics pipelines. Furthermore, its support for schema evolution enables organisations to adapt their data models over time without disrupting existing applications.


Consolidation Exercise:
Reflect on a recent project or a data challenge within your organisation.
How might the choice between HDFS, key-value stores, and Parquet influence the outcome of this project? 
Consider factors such as data volume, query performance requirements, and the nature of the data (structured vs. unstructured).
Identifying a stakeholder in your business who could provide further insights or feedback on your proposed solution

    Q. If stakeholder does agreed with a prosposed soltion, is it possible on current way sever is set up 


# Lession 3 : Data Lakes, Data Warehouses, and Operational Data Stores

<b>Data Lakes </b> <br>
Data lakes act as vast reservoirs of raw, unstructured data, capturing everything from logs and XML files to social media posts. They offer unparalleled flexibility in data storage, allowing businesses to store data in its native format without the need for upfront schema definition. 

<b>Data Warehouses </b> <br>
Makes it easily accessible for specific queries and reports. This structured environment supports complex queries, business intelligence, and data mining efforts, enabling organisations to derive actionable insights from their accumulated data. Data warehouses are essential for businesses that rely on historical data analysis to inform strategic decisions, offering a stable and reliable platform for data storage and retrieval.

<b>Operational Data Stores (ODS) </b> <br>

Real-Time Data Processing: Operational data stores are designed for the real-time processing of transactional data, supporting day-to-day business operations. They enable the immediate availability of operational data for analysis and decision-making, acting as a bridge between transactional databases and data warehouses or data lakes.

Consolidation Exercise:
- Consider a specific business scenario or project within your organisation where the choice between a data lake, data warehouse, and ODS would be critical. 
- Discuss your thoughts in your learning journal, and identify a stakeholder who could offer additional perspective on this decision.


# Lession 4 :  Data Structuring: Schema-on-Write, Relational Modelling



  
