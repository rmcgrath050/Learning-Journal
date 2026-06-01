#### What signs would tell us data is delayed with Kafta?
- timelines - out of date
- outdated responses via monitoring systems, logs
- sensor data timestamps lagging behind real Time 


#### What do you think could cause the delay?
- bottlenecks with slow logic?
- network latency? (Between producers and brokers) 
- delays in ingestion, data generated too slowly 
- loss of network / faulty sensors


#### How would you improve the speed?
Use compression to reduce network load

Kaggle - datases website 

Event Hubs - ingestion system of real time data 
Event Grid - how to trigger a reaction to that event 

Kafta - u are in charge of clusters, scaling, upgrades, issues, infrastucture 
Azure event hubs - fully managed, manages clusters , 


What would work best for organisation? 
- Kafta would be more ideal for on prem and bespoke customer solutions


Disadvantages of Cloud services
- latency 
- vendor lock ins
- increased costs  - pay as you go , but increases cost for more controlled services like Kafta 

SSL - Secure Socket Layer / TLS (Transport Layer Security) 
Provide encryption and integrity for transfer
Needs it legally! - Instant messaging services, finance , gov systems 


#### ACLS is about what level of access  u have, who can read/write.delete data. 

- Examples : PII data, high value financial transactions, trading/market data, 

Schema - type of event generated

Event Hubs is Microsoft's own version of Kafka and integrates with their own ecosystem
Azure is fully managed and scalable, Kafka is more configurable


