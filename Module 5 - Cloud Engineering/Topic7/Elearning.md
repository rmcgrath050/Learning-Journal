# Topic 6 - Putting it all together: Designing full-stack cloud solutions

Netflix uses a full-stack cloud solution to deliver its streaming service.
The frontend is the user interface you interact with, 
the backend services handle user requests and content delivery, 
databases store user data and content metadata, and the infrastructure ensures everything runs smoothly.
They also use DevOps tools to continuously deploy updates and monitor performance.

<br>

<img width="569" height="548" alt="image" src="https://github.com/user-attachments/assets/3ea7e947-8a4d-4a24-94da-3783103172e1" />
<br>
<br>

<img width="534" height="582" alt="image" src="https://github.com/user-attachments/assets/4160c066-3560-4023-86a3-b6daaaaf233e" />

<br>
<br>
No need for cloud when:
<br>




- Cost considerations: For small-scale applications with predictable, low workloads, on-premises solutions may be more costeffective     in the long run.
- Regulatory constraints: Some industries have strict data residency and compliance requirements that necessitate keeping data on      premises.
- Latency sensitivity: Applications requiring ultralow latency might perform better when hosted locally.
- Existing infrastructure: Organisations with significant investments in onpremises infrastructure may prefer to maximise their         current assets.
- Security concerns: Although cloud providers offer robust security, some businesses may have specific security policies that favour       onpremises deployment.


### Sanity checking user and business requirements

Before embarking on a cloud solution, it's essential to validate the requirements, including:
- Assess needs: Understand the problem the solution aims to solve and the value it brings to the business.
- Evaluate constraints: Consider budget, timelines, regulatory compliance, and technical limitations.
- Determine feasibility: Analyse whether cloud deployment aligns with the organisation's strategic goals and capabilities.
- Engage Stakeholders: Collaborate with end-users, management, and IT teams to gather diverse perspectives and ensure alignment.
- Risk Assessment: Identify potential risks and develop mitigation strategies.


## 2. Designing and deploying a Python data product dashboard

#### Data collection and storage
- Data sources: Use of student information systems, learning management systems, and attendance records.
- Data storage: Use of a cloud-based database like Amazon RDS or Azure SQL Database to store the aggregated data securely.

#### Backend development

- API development: Creation of a RESTful API using Python frameworks like Flask or Django to serve data to the frontend and visualisation tools.
- Data processing: The implementation of data processing pipelines to clean, aggregate, and prepare data for analysis.

#### Deployment to the cloud
- Infrastructure setup: Use of Infrastructure as Code tools like Terraform or AWS CloudFormation to provision resources.
- Containerisation: Containerisation of the application using Docker for consistent deployment.
- Cloud services: Deployment of the application on cloud services like AWS Elastic Beanstalk, Azure App Service, or Google App Engine.

#### Monitoring costs - (GCP Calculator for queries? ) 
- Setup costs: Tracking expenses related to infrastructure provisioning, including compute instances, storage, and network services.
- Running costs: Monitoring of ongoing expenses, considering data transfer costs, storage growth, and compute usage.
- Cost optimisation: Implementing cost-saving measures like reserved instances, spot instances, or serverless architectures where appropriate.

#### Supporting net-zero objectives
- Right-sizing instances: Selecting instance types that match the application's workload to avoid over-provisioning.
- Auto-Scaling Policies: Implementing auto-scaling to adjust resources based on demand, ensuring efficient resource utilisation.
- Energy-Efficient Practices: Use of cloud providers' green data centres and consideration of the environmental impact of resource usage.


#### Continuous monitoring
- Performance monitoring: Use of tools like AWS CloudWatch, Azure Monitor, or Prometheus to track application performance metrics.
- Logging and alerts: Implementing logging solutions to capture application logs and set up alerts for critical events.
- Health checks: Configuration of health checks to detect and respond to application issues promptly.
- User analytics: Monitoring user engagement and usage patterns to inform future improvements.


#### Monitoring setup and running costs

- Cost monitoring tools: Utilise cloud providers' cost management tools, such as AWS Cost Explorer or Azure Cost Management, to gain insights into spending.
- Budget alerts: Set up budgets and alerts to notify stakeholders when spending exceeds predefined thresholds.
- Resource tagging: Tag resources with metadata to track costs associated with specific projects, departments, or environments.
- Regular reviews: Conduct periodic reviews of resource utilisation to identify and eliminate waste, such as unused instances or orphaned storage volumes.


### Implemeting zero net strageies 

Right Size instances:
- Analyse resource usage to select the most appropriate instance sizes.
- Avoid over-provisioning, which leads to unnecessary energy consumption and costs.
- Utilise performance data to make informed decisions about scaling.

Auto scaling policies:
- Implement auto-scaling groups that adjust the number of running instances based on real-time demand.
- Schedule scaling actions during predictable periods of high or low activity.
- Use serverless architectures where possible to ensure resources are only consumed when needed.


### Continuous monitoring

Continuous monitoring is essential for maintaining the reliability, performance, and security of cloud applications.

<img width="662" height="548" alt="image" src="https://github.com/user-attachments/assets/4805fc89-7ae1-4763-8309-634929abc7e7" />


<img width="680" height="578" alt="image" src="https://github.com/user-attachments/assets/8a0a7901-8017-483a-ad79-e7e4f4556f88" />


## 3. Hackathon development focus

The purpose of the hackathon is to approximate what it may be like to build a project - something that is required for your EPA.

1. Equirement analysis
- Sanity check: Validating the business requirements to ensure they are feasible and aligned with the project scope.
- User stories: Defining user stories to capture the needs of different stakeholders, such as engineers, managers, and customers.

2. Full-stack design: Planning the frontend, backend, databases, and infrastructure components.
- Technology selection: Choosing appropriate technologies and cloud services for each layer.
- Integration points: Identifying how different components will interact and integrate with external services.

3. Implementation plan
- Task breakdown: Dividing the work among team members based on expertise and interests.
- Development approach: Deciding on methodologies like Agile or Scrum to manage the project efficiently.
- Infrastructure as Code: Utilising IaC tools to define and provision infrastructure consistently.

4. Cost monitoring strategy
- Budget planning: Estimating setup and running costs, considering all components.
- Cost optimisation measures: Planning for right-sizing, auto-scaling, and resource scheduling to control expenses.

5. Net-Zero considerations 
- Energy efficiency: Incorporating practices that reduce energy consumption and support the company's sustainability objectives.
- Carbon footprint analysis: Evaluating the environmental impact of the solution and identifying areas for improvement

6. Continuous monitoring setup
- Monitoring Tools: Selecting tools for infrastructure and application monitoring.
- Alert Configuration: Defining critical metrics and set up alerts to detect issues.
- Dashboard Creation: Building monitoring dashboards for real-time visibility.

7. Presentation and documentation
- Architecture diagram: Creating diagrams illustrating the system design and data flows.
- Documentation: Preparing documentation covering the design decisions, implementation details, and operational guidelines.
- Demo preparation: Developing a demo to showcase the application's features and benefits.


## 4. Recap

Designing full-stack cloud solutions requires a holistic understanding of technology, business needs, and operational practices. By putting all the pieces together, you can create applications that are not only functional but also efficient, scalable, and aligned with organisational goals.

Recognising when cloud solutions are appropriate and when they are not is crucial for making strategic decisions. Sanity checking requirements ensures that efforts are focused on delivering value where it matters most.

- Cloud solutions are beneficial in many scenarios but may not be necessary for small-scale applications, regulatory constraints, latency-sensitive applications, existing infrastructure investments, or specific security policies.
- Monitoring and optimising both setup and running costs of cloud solutions is crucial for sustainability.
- Implementing practices like right-sizing instances and auto-scaling policies supports sustainability and cost-efficiency.
- Continuous monitoring is essential for maintaining system health and driving ongoing improvements.

#### Further learning:

- Explore cloud provider documentation on cost management and monitoring.
- Practice deploying applications using Infrastructure as Code.
- Investigate best practices for implementing auto-scaling and right-sizing!


<img width="716" height="508" alt="image" src="https://github.com/user-attachments/assets/a06b7af8-2005-495b-a1e9-ac9d10cecbe1" />


1. Cloud fundamentals
- Recognise key cloud compute types and cost structures.
- Explore the cloud landscape’s top providers, common utilities, and resources.
- Be able to demonstrate your mastery of continuous learning in your EPA professional discussion.
- Evaluate the business case for cloud adoption and calculate ROI on cloud projects.
- Identify key business and user requirements for cloud-based data products.
- Describe key IAM concepts and the importance of service accounts.
