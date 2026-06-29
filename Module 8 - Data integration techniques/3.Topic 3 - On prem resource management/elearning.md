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

