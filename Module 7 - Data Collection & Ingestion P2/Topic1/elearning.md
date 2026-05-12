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

