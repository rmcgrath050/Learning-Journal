

### Lloyds example
Robert G: We havee event driven failures and also event driven ETL (so when files land, then trigger pipeline), event driven PowerBI/Dataflow refresh

### Event driven
- when "something" happens, do "something"
- A change of state in a component



Kafa cluster is a group of servers and we call that group of servers brokers
Each broker manages a set of portions , including read/write , no single point of failure

For each partition , we have one broker, one leader broker with follow up brokers, handles all reads and writes 


Partitions as immutuble log 
- never gets overwritten
- consumers track their progress here
