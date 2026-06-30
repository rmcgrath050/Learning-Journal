# Scalability – From Data Pipelines to Data Architectures

Think of a data pipeline like a system of pipes in your house. It’s easy to manage when just one tap is on. But what happens when every shower, kitchen tap, and garden hose is turned on at once. That’s the challenge of scale. 
Pipelines need to handle more throughput, avoid congestion, and ensure that nothing gets lost or delayed. Scaling a pipeline isn’t just about throwing more power at the problem; it’s about designing with growth in mind.

#### Learning objectives:
1. Distinguish between vertical and horizontal scaling strategies in data pipeline design.
2. Explain the benefits of partitioning, decoupling, and caching for scalable pipelines.
3. Describe how batch and stream processing approaches differ in scalability.
4. Identify tools and patterns used to support scalable data processing.


<br>
<img width="1614" height="1256" alt="image" src="https://github.com/user-attachments/assets/4e1c06ad-b8a8-4a12-8822-43cc836227fe" />
<br>

<img width="1462" height="1056" alt="image" src="https://github.com/user-attachments/assets/92dfb306-6dc0-440f-a223-12c8d8e0c569" />
<br>

<img width="1546" height="1356" alt="image" src="https://github.com/user-attachments/assets/4c0a3d60-a137-4ac1-94be-04bba31e2d3a" />
<br>
<br>
<img width="1582" height="1354" alt="image" src="https://github.com/user-attachments/assets/cba4097b-3dae-451f-8763-0a2784ced979" />
<br>
<br>
<img width="1620" height="1074" alt="image" src="https://github.com/user-attachments/assets/ba868c96-96ac-4d9c-8e13-27c6a76eca45" />
<br>
<br>

<b>Begin by monitoring performance - track data volume, task duration, and system load. Use these signals to decide what to scale: compute, memory, network, or storage. Choose tools that match your context. </b>

<br>
systems from an answer:
- Apache Kafka is a distributed event streaming platform that allows pipeline components to operate asynchronously by passing messages through topics. This decoupling improves fault tolerance and flexibility.
- (Spark) is a processing engine, not a messaging system.
- (PostgreSQL) is a relational database, not suited for asynchronous messaging.
- Redis) can cache data but doesn’t offer event-based decoupling.


## L2. Ensuring performance and reliability at scale

Performance issues - like slow processing times or memory bottlenecks - can creep in. Reliability issues - like silent failures or dropped records - can damage trust in the data. Your job is to build pipelines that aren’t just fast - they're also dependable.

1. Identify key factors that affect the performance and reliability of data pipelines.
2. Apply techniques to monitor and tune pipeline performance at scale.
3. Describe the role of fault tolerance, retries, and observability in reliable data systems.
4. Recognise the importance of testing and validation in scalable pipelines.

### Performance at scale: Making pipelines efficient

1. Monitor correct metrics:

Start with visibility. Key performance indicators (KPIs) might include:

- Throughput – How much data is processed per unit time.
- Latency – Time taken from source to destination.
- Resource usage – CPU, memory, and disk consumption.
- Backlog size – In stream systems, how much data is waiting to be processed.
- Tools like Prometheus, Grafana, or cloud-native services (e.g. AWS CloudWatch) help visualise this data and reveal bottlenecks.



