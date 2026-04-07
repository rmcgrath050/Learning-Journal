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
No need for cloud when:
- Cost considerations: For small-scale applications with predictable, low workloads, on-premises solutions may be more cost-effective in the long run.
- Regulatory constraints: Some industries have strict data residency and compliance requirements that necessitate keeping data on-premises.
- Latency sensitivity: Applications requiring ultra-low latency might perform better when hosted locally.
- Existing infrastructure: Organisations with significant investments in on-premises infrastructure may prefer to maximise their current assets.
- Security concerns: Although cloud providers offer robust security, some businesses may have specific security policies that favour on-premises deployment.


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


  

