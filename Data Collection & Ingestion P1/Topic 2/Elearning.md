# L5DE 6.2 - Heterogeneous data ingestion patterns

There are two main types of data ingestion:

1. Batch Processing
2. Real-Time (or Stream) Processing

###### Batch

1. Timing, Data is collected in large 'batches' at scheduled intervals - hourly, daily, weekly, etc., depending on the system's requirements.
2. Suitabaility ,  Ideal for scenarios where its not necessary to have real-time data insights and where processing large volumes of data at once is more efficient.
3. Often simpler and less resource-intensive compared to real-time processing. The downside is latency in data availability and potential relevancy.
4. Use Caes, Common in situations where the data doesn't change rapidly, like processing sales records at the end of the day or generating daily reports.


###### Data Velcocity
Data velocity refers to the speed with which data enters your system and how long it takes for processing to occur. Data velocity can affect network latency and user traffic.
Your design must account for questions like:
- How fast does data flow happen?
- Will this velocity compete with my business traffic?
- Can my network bandwidth handle the data flow?
- Will it increase latency for my users?

###### Data Volume
All data ingestion tools are built in diverse ways and have workload limits, some to the petabyte or terabyte scale. Therefore, in deciding what ingestion tools to implement, you must ask questions like:
- What is the volume of data ingested frequently?
- How many rows/columns are present?
- Are there plans to scale in the future?
- Will your solution scale to accommodate the growing/changing business demand?

###### Data Frequency
our ingestion framework should note your business goal, timeliness of responses, and budget to select the best ingestion design.
- How often does ingestion from sources occur?
- What is the response time needed on the data to create value? Some data contains a time window and lose value for longer response times.
- Will batched or real-time streaming work?
- Can you implement micro-batching to ensure near real-time updates?

###### Data Format
Your ingestion design must consider data schema and format in your workflow.
- In what format does the data arrive?
- Is it unstructured, like video or text, or structured, like JSON and CSV?
- Does this tool validate and enforce schema?
- Can you afford the engineering time needed to configure and validate the schema if not?


###### Data security and governance
Ensuring data security and governance is crucial to your ingestion design and may involve asking questions like:
- Who has access to this data?
- Will data be consumed internally or externally?
- Are sensitive data like Personally Identifiable Information (PII) present in the data?
- What are some security measures to implement to ensure no leaks or breaches?

Additionally, your tooling infrastructure must employ ingestion best practices like validating data at strategic points in the pipeline, auditing, log-viewing, and visualisations to observe and track the ingestion workflow.

Every ingestion tool combines data security and privacy methods to ensure governance during ingestion.
These methods include encryption, security protocols like SSHH , HTTPS, SSL/TLS, and IPSec, data quality checks, and data audits.
Implementing one or more of these measures depends on your organisation’s needs and objectives.
For example, for healthcare and finance industries with strict data privacy regulation laws, your ingestion pipeline should include security measures to hide PII to prevent sensitive data leaks.


<br>
For real-time analytics, it’s crucial to consider data velocity to ensure low latency and high performance. Security is also important to protect sensitive financial data!
Ensuring data security and governance involves implementing encryption, validating data at strategic points, and using security protocols like HTTPS and SSL/TLS to protect data throughout the ingestion process!

## 2. Heterogeneous data ingestion use cases



