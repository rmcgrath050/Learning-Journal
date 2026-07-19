# L5DE 8.3 - Managing computational resources for data pipelines

## 1. Introduction to computational resource management

Data engineers must implement systematic strategies to align their pipelines with operational goals, performance needs, and budget constraint. 

Key principles of computational resource management:

<img width="1812" height="1246" alt="image" src="https://github.com/user-attachments/assets/75608dd7-aaf2-4be7-a9c3-9a8ccb75f1a7" />
</br>

- Right sizing: Accurately determining the appropriate amount of computational resources needed for each task, Using AWS CloudWatch to track resource utilisation and adjust accordantly
- Elastic scaling: scaling based on demand,
- Resource Pooling: Sharing computational resources across multiple workloads to improve efficiency, eg Using a shared Spark cluster 
- Cost optomising: Implementing strategies to minimise resource costs  whilst also still acehiving performance. eg  leasing spare cloud capacity at steep discounts
- Performance monitoring, checking performance metrics, eg Identifying a memory-bound job and switching to a memory-optimised instance type.
- Resource Govarance: Establishing policies and controls for fair resource allocation. (Dividing resources such as CPU, etc across departments)


### Principle 7 - Advanced resource management strategies

Cutting-edge techniques to enhance resource efficiency and scalability in your data engineering tasks, including:

- Containerisation and orchestration: Using Docker and Kubernetes for fine-grained resource control.
- Serverless computing: Leveraging serverless platforms for event-driven workloads. (GCP etc, pay for what you use)
- Workload-aware scheduling: Implementing intelligent scheduling based on workload characteristics.
- Infrastructure as Code (IaC): Managing infrastructure through code-based definition files.
- Hybrid and multi-cloud strategies: Distributing workloads across multiple environments.


## L2. Resource management tools and platforms

The ability to manage resources effectively is crucial for ensuring that data pipelines run smoothly, meet performance requirements, and stay within budget constraints. This lesson will introduce you to key resource management tools and platforms that can help you achieve these goals. 

By understanding and utilising these tools, you can optimise resource allocation, enhance performance, and reduce costs in your data engineering tasks.

### kubernetes

An open-source container orchestration platform that automates deployment, scaling, and management of containerised applications.

Kubernetes supports horizontal pod autoscaling based on custom metrics, allowing data pipelines to adjust parallelism based on queue depth or processing latency. eg queue = total number of unread or unprocessed messages/jobs waiting in your message broker / What it is: The total time it takes for a single item (or batch) to move entirely through your pipeline, from the moment it enters the queue to the time its processing is completed.

### Terraform and CloudFormation

with terraform you decribe the end result, tell it what you want instead of creating steps one at a time
A Terraform configuration might specify a complete data processing environment, including compute resources, network configurations, and security groups.

Consistent environments across deployments, infrastructure testing and validation, and collaborative development through code review and continuous integration.

## L3. Optimising resource management for a Telco data processing pipeline

##### Workload classifcation
Definition: Categorising workloads into critical, important, and routine, and establishing resource allocation policies.
Example: Prioritising regulatory reporting during peak periods to ensure compliance! - Run these first every morning! 

<br>

##### Hybrid infrasturcre approach
Definition: Using a combination of on-premises and cloud resources to meet compliance and scalability needs.
Example: Processing sensitive data on-premises while leveraging cloud resources for peak processing periods.
<br>

##### Auto Scaling
Definition: Automatically scaling cloud resources based on data volume metrics.
Example: Configuring scale-out thresholds to add resources before performance degradation occurs.
<br>

##### Cost Optimisation
Definition: Implementing strategies to minimise costs while maintaining performance.
Example: Using spot instances for fault-tolerant components and scheduling non-time-sensitive processing during off-peak hours.

Cost optimization means reducing cloud costs by using cheaper resources (like spot instances) for workloads that can tolerate interruptions and scheduling non-urgent tasks to run when demand is low, without affecting application performance.

If your reports depend on batch jobs finishing before users can run reports, you are managing resources.

## Reflection
*** EPA 

<i>Think about a recent project where you had to manage computational resources...</i>

You could say:

If your reports depend on batch jobs finishing before users can run reports, you are managing resources:
"I designed SQL Server data sources that were populated as part of an overnight batch process. To ensure reports were available on time, I considered the execution order and timing of dependent processes so that reporting only occurred once the required data sources had been fully generated. This avoided unnecessary reruns via report owners and reduced contention with other batch processes."
<br>

Option 2: Query optimisation:
- added indexes
- rewritten joins
- reduced table scans
- avoided unnecessary calculations
- filtered data earlier


When designing data sources, I optimised SQL queries to minimise execution time by reducing unnecessary joins and ensuring appropriate indexes were used. Faster queries reduced CPU and I/O usage on the SQL Server while still delivering the required reporting data.
<br>


"The reporting framework generated multiple reports from shared data sources. I designed the data sources so they could be reused across reports instead of recalculating the same data multiple times. This reduced processing overhead and improved overall batch execution."

That's resource optimisation because you're avoiding duplicate work.
<br>

Most of my work has been designing SQL Server data sources for a bespoke batch reporting framework. Although I wasn't managing cloud infrastructure directly, I did consider computational resources by designing efficient queries, avoiding redundant processing, and ensuring data sources were generated in the correct sequence so reports could run reliably without placing unnecessary load on the database.



## L4. YARN mechanism - on-premises infrastructure example

Apache Hadoop is an open-source distributed computing framework that uses commodity computers to provide processing capability and data storage space. It offers resilience through data replication and is written in Java™. Hadoop has four main building blocks:
<br>

<img width="1508" height="1194" alt="image" src="https://github.com/user-attachments/assets/025ba2dd-25bd-4306-a333-694d0444337b" />

1. Hadoop Common: The base API jar file that acts as the foundation for the other components.

2. Hadoop Distributed File System (HDFS): Distributes large files across many physical machines to ensure high-speed streaming and resilience.

3. Yet Another Resource Negotiator (YARN): Provides centralised resource management and scheduling.

4. MapReduce: A programming model for processing large datasets.

#### HDFS explained

1. Data Blocks: Files are broken into blocks (default size 128MiB) and stored with triple redundancy.
2. Heartbeat Mechanism: Monitors the health of machines in the cluster.
3. File System Namespace: Keeps track of files, their component blocks, and access permissions.
4. Name Node: The master server responsible for block tracking, access control, and modification timestamps. It operates as an Active/Passive Cluster with a Secondary Name Node for replication and logging tasks.
5. Data Nodes: Service read and write requests, perform block creation, deletion, and replication tasks.
6. Rack Awareness: Helps the Name Node understand the physical layout of Data Nodes to make informed decisions about block distribution.


Hadoop
Apache Spark (which evolved beyond traditional MapReduce)
Large-scale distributed data processing

It's designed for situations where a single database server isn't enough.

Compare it to your work:

Designing SQL Server data sources
Writing SQL queries
Creating datasets for a bespoke reporting framework
Supporting batch reporting
Optimising query performance

That's relational database processing, not distributed computing!

"Although I haven't used YARN directly, I understand that it acts as a resource manager for Hadoop, allocating CPU and memory to different processing jobs so they can run efficiently without competing for the same resources. In my SQL Server reporting work, I apply similar principles by scheduling and sequencing batch processes so that dependent data sources are available when needed and database resources aren't overloaded."


My current experience is in SQL Server batch reporting, where I optimise query performance and schedule data processing so reports are available when needed. Alongside this, I'm learning Terraform, Kubernetes and GCP. This has helped me understand how modern cloud platforms allocate resources and orchestrate workloads. Although I haven't used YARN directly, I understand that it serves a similar purpose within Hadoop by allocating CPU and memory to data processing jobs, scheduling execution, and preventing resource contention across the cluster."

# L5 Conclusion

whats applicable to me :
- Advanced Resource Management Strategies: Employing techniques like containerisation and orchestration (Docker and Kubernetes), serverless computing (AWS Lambda, Azure Functions), workload-aware scheduling, Infrastructure as Code (IaC) tools (Terraform, AWS CloudFormation), and hybrid/multi-cloud strategies to optimise resource utilisation across various environments.

- Resource pooling: Sharing computational resources across multiple workloads to improve utilisation efficiency and reduce overall infrastructure costs, leveraging platforms like Kubernetes.

- Cost optimisation: Using strategies to minimise resource costs while maintaining performance, such as spot instances for fault-tolerant workloads and scheduling intensive processing during off-peak hours.




