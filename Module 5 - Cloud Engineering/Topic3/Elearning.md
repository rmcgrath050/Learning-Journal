# L5DE 5.3 - Containers and orchestration

Managing applications on virtual machines can lead to resource underutilisation and increased energy consumption, conflicting with sustainability goals. Organisations need solutions that allow for dynamic scaling, efficient resource utilisation, and reduced operational overhead. 
<br>
Containers and orchestration tools address these challenges, but data engineers must develop skills in designing and managing these technologies effectively. In particular, understanding how to implement auto-scaling and right-sizing instances is crucial for promoting net-zero objectives and supporting sustainable growth.

<br>
Docker provides a standardised way to package applications with their dependencies, ensuring consistency across environments.
This innovation allowed developers to build, ship, and run applications reliably, fostering a new era of DevOps practices.

#### Rise of DevOps Practices
As applications grew in complexity, managing containers manually became impractical, leading to the development of orchestration tools.

#### Development of Kubernetes
Kubernetes, originally developed by Google and released as an open-source project in 2014, addressed this challenge by automating the deployment, scaling, and management of containerised applications.
Kubernetes enables organisations to harness the full potential of containers, providing features like auto-scaling and self-healing, which are essential for sustainable and resilient systems.

### Emergence of Serverless Computing
Serverless computing emerged as another paradigm shift, allowing developers to focus solely on writing code without worrying about the underlying infrastructure.
serverless architectures enable applications to scale automatically in response to demand, promoting efficient resource usage and supporting sustainability objectives.
By only consuming resources when needed, serverless models contribute to reducing the carbon footprint of IT operations.
The concept of containerisation originated from the need to solve the 'works on my machine' problem, where applications behaved differently in development and production environments.


- Energy Consumption of Data Centres: According to the International Energy Agency, data centres account for about 1% of global electricity use. Efficient resource utilisation through        practices like auto-scaling can significantly reduce this impact.
- Google's Contribution to Kubernetes: Kubernetes was born from Google's experience running containers at scale. The name "Kubernetes" comes from the Greek word for "helmsman" or "pilot,"   reflecting its role in steering container deployments.
- Docker's Rise to Popularity: Within a year of its release, Docker had over 20,000 stargazers on GitHub, highlighting the rapid adoption and enthusiasm in the developer community.


## 2. The key skill of visual modelling for container design

To begin practising visual modelling, start by identifying the main components of your application. For a microservices architecture, this may include individual services, databases, message queues, and external APIs. Represent each component with a simple icon or box, labelling it clearly. Use arrows to indicate the flow of data and interactions between components. Containers can be depicted as encapsulating the services they run, highlighting the isolation and consistency they provide.


<img width="456" height="426" alt="image" src="https://github.com/user-attachments/assets/c787e675-9904-4332-bccc-51902414da98" />

<br>
For instance, when designing a containerised application with Docker, you might draw a diagram showing multiple containers, each running a different microservice. These containers communicate with each other over defined network interfaces. Including orchestration tools like Kubernetes in your diagram adds another layer, showing how containers are deployed across nodes, managed by Kubernetes components such as the API server, controller manager, and scheduler.  Promotes business planning for substainable growth and right sizing instances.

<img width="634" height="572" alt="image" src="https://github.com/user-attachments/assets/1b4d4345-799d-47b9-9db8-681b68a09fed" />

Practising drawing these diagrams enhances your understanding of the architecture and aids in identifying dependencies, potential bottlenecks, and opportunities for optimisation. It also facilitates discussions on sustainability considerations, such as how auto-scaling policies can adjust resources in response to demand, reducing unnecessary energy consumption.


<img width="722" height="507" alt="image" src="https://github.com/user-attachments/assets/4250541c-922b-4c87-8994-fcbd1c6d83bc" />

### Serverless Mode vs. the VM Deployment Model

Understanding the differences between serverless mode and the virtual machine (VM) deployment model is essential for choosing the right infrastructure for your applications, especially when considering sustainability objectives.


#### Virtual machine deployment model

In the VM deployment model, applications run on virtualised hardware managed by a hypervisor. Each VM has its own operating system, resources, and applications, isolated from other VMs on the same physical machine.

<b>Pros:</b>
- Isolation and Control: VMs provide a high level of isolation between applications, with full control over the operating system and environment. This control is beneficial for applications requiring specific configurations or legacy systems.
- Compatibility: VMs can run any operating system and support applications that may not be container-ready.
- Secuirty: The isolation between VMs enhances security, reducing the risk of one compromised VM affecting others.

<b>Cons:</b>
- Resource Inefficiency: VMs consume more resources due to the overhead of running separate operating systems, often leading to underutilisation and increased energy consumption.
- Slower Deployment: Spinning up VMs and deploying applications can be time-consuming, affecting agility.
- Maintenance Overhead: Managing and updating operating systems and applications on multiple VMs increases operational complexity and operational carbon footprint.

<img width="789" height="496" alt="image" src="https://github.com/user-attachments/assets/a65712ce-e566-49f0-ace2-b6bc84cd9e9c" />

When comparing these models, sustainability plays a significant role. Serverless architectures inherently promote efficient resource utilisation by allocating resources only when needed. This efficiency reduces energy consumption and supports net-zero objectives. In contrast, VMs often run continuously, even when underutilised, leading to wasted resources and higher carbon emissions.

<br>
#### Severless Deployment 

Serverless computing emerged to address the need for developers to focus on application functionality without the burden of managing infrastructure. Introduced by AWS Lambda in 2014, serverless platforms allow code to run in response to events, scaling automatically based on demand. This model aligns with sustainable practices by ensuring that resources are only consumed when necessary.
The implementation steps are as follows:
1. Writing the Function Code: Develop your function using the supported programming language, such as Python or JavaScript. The code should be stateless and efficient to optimise performance.
2. Configuring the Trigger: Set up the function to trigger based on an event, such as an HTTP request or a message in a queue. This event-driven model ensures that resources are only used when needed.
3. Deploying the Function: Upload your code to the serverless platform, which handles the provisioning and scaling automatically. There is no need to manage servers or worry about capacity planning.
4. Testing the Function: Simulate events to ensure that the function executes correctly and processes data as expected. Monitoring tools can help identify any performance issues or resource bottlenecks.

By using serverless mode, you avoid idle resource consumption, as functions are only active when invoked.

<br>

Deploying a microservices application involves packaging individual services, orchestrating their deployment, and managing their interactions. We will walk through deploying a simple Python application using Docker, Kubernetes, and serverless deployments, setting the scene for each technology and explaining their origins.

Implematation steps: 
- Containerising the Application: Write Dockerfiles for each microservice, specifying the base image, dependencies, and startup commands. This encapsulation simplifies deployment and enhances portability.
- Building Docker Images: Use the Dockerfiles to build images for each service. These images include all necessary components, reducing the risk of missing dependencies.
- Running Containers Locally: Test the containers locally by running them and ensuring they function as expected. This step helps identify any issues early in the development cycle.
- Pushing Images to a Registry: Upload your images to a container registry like Docker Hub or a private registry, facilitating deployment across environments.
- Deploying Containers: Use Docker Compose or Docker Swarm to define and deploy the multi-container application. This orchestration simplifies management and scaling.


<img width="775" height="384" alt="image" src="https://github.com/user-attachments/assets/91de82cc-a62d-4917-be2d-c3649d2c1f04" />


<br>
<b>Implematation steps: </b>
1. Writing Deployment Manifests: Create <b>YAML</b> files defining the deployments and services for each microservice. These manifests specify how applications should run in the cluster.
2. Configuring Kubernetes Objects: Specify details like replicas, container images, ports, and environment variables. Configurations for auto-scaling can be included to adjust resources based on demand.
3. Deploying to a Cluster: Apply the manifests using kubectl, deploying the application to a Kubernetes cluster. The cluster can be on-premises or in the cloud.
4. Managing the Application: Use Kubernetes features like scaling, rolling updates, and self-healing to manage the application. Auto-scaling ensures that resources match the workload, promoting efficient usage.


<img width="778" height="517" alt="image" src="https://github.com/user-attachments/assets/a520ca44-4a24-4834-b240-ec54bcba1caf" />


<br>
<b>Implematation steps: </b>
- Converting Microservices to Functions: Adapt your microservices to function as serverless functions, focusing on stateless operations. This may involve refactoring code to fit the           serverless paradigm.
- Deploying Functions: Use a serverless framework or platform-specific tools to deploy your functions to services like AWS Lambda or Azure Functions. Deployment is simplified, and scaling     is handled automatically.
- Configuring Triggers and Integrations: Set up events that trigger your functions and configure any necessary integrations with other services. This event-driven model enhances               responsiveness and efficiency.
- Monitoring and Managing Functions: Use the platform's tools to monitor performance, set up alerts, and manage scaling policies. Monitoring ensures that functions perform optimally and      resources are used efficiently.

## Lession 3: HR Dashboard deployment in a bank

challenges:
1. Scalability: The application must handle varying workloads, with peak usage during certain times, such as performance review periods.
2. Resource Efficiency: Minimising resource wastage is crucial to align with the bank's sustainability goals.
3. Operational Overhead: Reducing the time and effort spent on managing infrastructure allows the bank to focus on delivering value to employees.

The solution = combination of containers and orchestration tools to deploy the HR dashboard, leveraging auto-scaling and right-sizing practices.


<img width="713" height="711" alt="image" src="https://github.com/user-attachments/assets/374aad92-06d6-4f25-933e-b1fe4672fef6" />

<br>
3. Implementing Serverless Functions: Certain components, such as report generation tasks, are implemented as serverless functions using Azure Functions. These functions are triggered by events, such as the completion of data processing, and scale automatically based on demand.
4. Monitoring and Optimisation: The bank employs monitoring tools to collect data on resource usage, performance, and energy consumption. Reports are generated to analyse resource utilisation, identifying opportunities for optimisation. Adjustments are made to auto-scaling thresholds and instance sizes to improve efficiency further.

<br>
Results include:
- Resource Efficiency: The application scales dynamically, using resources only when needed, reducing energy consumption and operational costs.
- Sustainability Alignment: By implementing auto-scaling and right-sizing, the bank promotes net-zero objectives, contributing to its sustainability commitments.
- Operational Benefits: Reduced operational overhead allows the IT team to focus on improving the application rather than managing infrastructure.
- Improved Performance: The application provides responsive and reliable service to HR managers, enhancing decision-making and employee satisfaction.

<br>
Monitoring resource usage is essential for ensuring that applications run efficiently and support sustainability objectives. By tracking metrics like CPU utilisation, memory usage, and network traffic, organisations can identify bottlenecks, plan for scaling, and optimise resource allocation.


### How is this done?

#### Reporting on Resource Use

- Collecting Metrics: Use monitoring tools like Prometheus, Grafana, or cloud provider services to collect data on resource usage. These tools can aggregate data across containers, nodes, and functions.
- Visualising Data: Create dashboards that display key metrics, helping teams understand the performance and resource utilisation at a glance. Visualisations can highlight trends and anomalies.
- Setting Alerts: Configure alerts to notify teams when resource usage exceeds defined thresholds, enabling proactive management. Alerts can prevent issues like resource exhaustion or performance degradation.


#### Optimising Resource

- Auto-Scaling: Implement auto-scaling policies that adjust resources in response to demand. Kubernetes Horizontal Pod Autoscaler can increase or decrease the number of pods based on metrics.
- Right-Sizing Instances: Select instance types and sizes that match the workload requirements, avoiding over-provisioning and underutilisation. Regular reviews can ensure that instances remain appropriately sized as workloads change.
- Optimising Code and Configurations: Review application code and configurations to improve efficiency. Optimisations can reduce resource consumption, enhancing performance and sustainability.

#### OSubstainable Growth
- Capacity Planning: Use historical data and forecasts to plan for future growth, ensuring that infrastructure can handle increased workloads without waste.
- Cost and Energy Management: Monitor costs and energy consumption associated with resource usage. Implementing cost-saving measures often aligns with reducing energy usage, supporting net-zero objectives.
- Continuous Improvement: Regularly review performance and resource utilisation, making adjustments to maintain optimal efficiency. Embracing a culture of continuous improvement promotes sustainability.


## 4. Putting it all together

we explored the fundamental concepts of containers and orchestration, crucial for modern data engineers focused on sustainability. We highlighted the importance of visual modelling in designing container architectures, enhancing communication, planning, and resource optimisation. Comparing serverless mode and the VM deployment model provided insights into choosing infrastructure that meets performance and sustainability goals.
<br>
Through practical examples, we showed how serverless deployments can simplify operations, reduce overhead, and promote efficient resource usage. The walk-through of deploying a Python microservices application using Docker, Kubernetes, and serverless methods explained each technology’s origins and contributions.







