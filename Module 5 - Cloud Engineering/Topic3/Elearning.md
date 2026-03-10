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




