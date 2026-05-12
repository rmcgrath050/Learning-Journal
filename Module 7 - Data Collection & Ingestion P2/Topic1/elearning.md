# L5DE 7.1 Event-driven architectures fundamentals


In industries like finance and e-commerce, the ability to process and react to data in real-time is no longer a luxury but a necessity. Event-Driven Architectures (EDA) have emerged as a cornerstone in handling this deluge of information, enabling systems to respond to events as they occur.

This is where Event-Driven Architectures come into play, offering a more dynamic and scalable approach to data ingestion and processing.

<br>
##### The key components of EDA:
- Events: Significant changes in state, such as a customer making a purchase, a new charity donation, or a sensor detecting movement.
- Event producers: Entities that generate events. For example, an online banking application generating a transaction event.
- Event consumers: Services that listen for and process events, like a fraud detection system monitoring unusual transactions.
- Event brokers: Middleware that routes events from producers to consumers, ensuring scalable and reliable delivery.


## L2 The pub-sub model and messaging

The Publish-Subscribe (Pub-Sub) model is a messaging pattern central to EDA. In this model, publishers emit messages to specific topics without knowledge of which subscribers will receive them. Subscribers, on the other hand, express interest in certain topics and receive messages accordingly.

Imagine a nature conservation organisation tracking wildlife movements.
Sensors placed in the wild generate location data (publishers), while any researchers worldwide can at any given time subscribe or unsubscribe from this data to monitor animal behaviour.This is the essence of the Pub-Sub model.

1. Publishers: Entities that send messages about events to specific topics without knowledge of who will consume them. For example, an HR system publishes updates about employee promotions to the "employee_updates" topic.

2. Subscribers: Entities that express interest in one or more topics and receive messages published to them. For instance, a payroll system subscribes to the "employee_updates" topic to adjust salaries accordingly.

3. Topics: Channels or categories that messages are published to, such as "elephant_movements" or "temperature_readings". Serve as places for grouping messages, such as "sales_data" or "system_alerts".


Advantages include:
- Decoupling: Enhances system flexibility and scalability.
- Efficient Broadcasting: Messages are efficiently routed to all interested subscribers.
- Scalability: Easily handles an increasing number of publishers and subscribers.

Traditional message queue systems like RabbitMQ and TIBCO EMS operate on a point-to-point model, where each message is delivered to a single consumer. In contrast, the Pub-Sub model allows messages to be broadcasted to multiple subscribers simultaneously. This decouples the producers and consumers, enhancing system flexibility and scalability.



Decoupling ensures producers and customers operate independantly
- Scalability: You can scale consumers without affecting producers.
- Flexibility: Consumers can be added or removed without disrupting producers.
- Resilience: System components can fail independently without causing a complete system outage.


In large organisations, HR systems use Pub-Sub models to manage employee data changes. When an employee updates their address, the change is published to a topic. When an employee receives a promotion, the HR system publishes this event to a different topic. Systems like payroll, benefits, and compliance subscribe to these topics and automatically receive the updates, updating their records accordingly, and ensuring data consistency across the organisation

## L3. Deep dive into Kafka

Apache Kafka is an open-source distributed event streaming platform used by over 80% of Fortune 100 companies, including banking giants like Goldman Sachs and tech firms like LinkedIn. Kafka is renowned for its ability to handle high-throughput, fault-tolerant data streams, making it an indispensable tool for real-time analytics and data processing.


- Topics: Categories or feed names to which messages are published. For example, "transaction_events" or "user_activity."
- Partitions: Subdivisions of topics that allow Kafka to parallelise message processing. Each partition is an ordered, immutable sequence of records that is continually appended to.
- Producers: Applications that write data to Kafka topics. They can send messages to multiple topics and partitions based on their configuration.
- Consumers: Applications that read data from Kafka topics. They can be part of a consumer group to distribute the load.
- A consumer group is a collection of consumers that work together to consume messages from a topic's partitions, ensuring load balancing and fault tolerance.


##### Kafka Clusters

A Kafka cluster consists of multiple brokers (servers) that manage the storage and retrieval of messages. Zookeeper is used to manage and coordinate the cluster, ensuring data consistency and system reliability. Each broker can handle multiple partitions, allowing Kafka to scale horizontally by adding more brokers to the cluster.
<br>
<br>
<img width="742" height="484" alt="image" src="https://github.com/user-attachments/assets/85cf4f6b-ba7b-4abf-910e-c5b95dc136a9" />
<br>

Kafka ensures data consistency through its replication mechanism. Each partition can have multiple replicas across different brokers, with one broker acting as the leader and others as followers. Kafka guarantees strong consistency by ensuring that all replicas acknowledge a message before it is considered successfully written. This ensures that even if a broker fails, the data remains available and consistent across the cluster.
<br>
<br>

<img width="648" height="465" alt="image" src="https://github.com/user-attachments/assets/7187a7d3-b2e9-49b6-8f77-16221e6b7105" />
<br>
<br>


#### Kafka as a log

Kafka treats each partition as an immutable log. Messages are appended to the end of the log and are assigned a sequential offset. Consumers track their position in the log by recording the offsets they have processed. This log-based architecture allows Kafka to efficiently handle large volumes of data and provides durability by retaining messages for a configurable retention period.


Practical configuration considerations
When setting up Kafka, several configuration parameters need to be considered:
- Retention Policies: Define how long Kafka retains messages in a topic, balancing storage costs with data availability.
- Replication Factor: Determines the number of replicas for each partition, impacting data durability and availability.
- Producer and Consumer Settings: Configuring batch sizes, compression, and acknowledgement levels to optimise performance and reliability.


### Challeneges

Setting up Kafka can present several challenges, including:
- Zookeeper coordination: Ensuring Zookeeper is correctly configured and integrated with Kafka can be complex.
- Network configuration: Properly setting up network settings to allow brokers to communicate efficiently.
- Resource allocation: Allocating sufficient memory and storage resources to handle expected data loads.
- Security configuration: Implementing SSL, SASL, and ACLs to secure data streams and broker access.
