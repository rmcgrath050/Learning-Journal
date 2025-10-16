# Introduction to reliable data architectures

<b>When working with data systems, what is your stragey for addressing?</b>
<br>
AWS/azure - manage space automically 
Data statgey where you an store data on cloud, and on site 
using modular scalable architecutre like microservices , data mesh etc. 

Leanring outcomes:
- Model standardised big data ecosystems and architectures for
enterprise data using visual approaches
- Describe the benefits of the three-layered architecture pattern
for organisational data management
- Describe how the microservices architecture style enables
organisations to build flexible, scalable, and resilient data
products
- Define architectural governance and its role in ensuring
reliability and compliance

There are also very special types of diagrams commonly used by data engineers that we will learn about, including:
1. Unified modelling language (UML) diagrams
2. Entity-relationship diagrams (ERDs)
3. Architecture diagrams (e.g. Layered architecture, microservices architecture)

<br>
<br> 

<img width="580" height="378" alt="image" src="https://github.com/user-attachments/assets/a87011db-6b12-4312-b413-c280bba00de8" />

<br>
<br> 

Sequence diagrams are a type of UML diagram that emphasise the timing of interactions between various components or objects within a system. They aid project teams in comprehending the flow of messages and activities across different parts of a system or process.
<br>
<br> 

## A Sequence diagram for student / apprentice registration
<img width="580" height="378" alt="image" src="https://github.com/user-attachments/assets/31fd0360-5992-48b6-9443-e5206da74253" />

<br>
<br> 

## Use Case Diagrams

It illustrates the various interactions between users (actors) and the system to accomplish specific tasks or goals. 

<img width="580" height="378" alt="image" src="https://github.com/user-attachments/assets/04036609-b8f5-42e0-84d0-fc38b789f15e" />

Tips:
1. Clearly define actors (e.g., Project Manager, Team Manager, Team Member etc) and their roles within the system using standard symbols such as stick figures
2. Use arrows to illustrate the flow of information or data between actors and use cases
3. Incorporate data stores or databases to represent where data is stored or retrieved within the system
4. Clearly indicate dependencies between use cases, actors, and system components using appropriate connectors such as associations or include/extend relationships
5. Consider breaking down complex use cases into smaller, more manageable components to avoid overwhelming the audience

   
## ERDS

An entity relationship diagram (ERD) serves as a powerful visualisation tool for understanding the relationships between different entities within an application or database

<br>
<img width="580" height="378" alt="image" src="https://github.com/user-attachments/assets/a3b7aea6-704d-410f-8a90-5463bc8ce3a3" />
<br>
<br>

The ERD consists of two main entities: Student and Course. These entities can be broken down as follows:

Student entity:<br>
Attributes: Name, Email
<br>
Prime Attribute: SSN

Course entity:<br>
Attributes: Title, Duration
<br>
Prime Attribute: Course Identifier (CID)

The relationship between the Student and Course entities is represented by a join relationship in the middle, indicating that a student can enrol in multiple courses, and a course can have multiple students enrolled.


## Logical Diagram / Organisational Architecture 

What information are logical diagrams designed to provide?
Logical diagrams are designed to illustrate the high-level flow of data within our system without referencing any specific vendors. 

They focus on depicting the structure of data across different stages, providing a conceptual overview of how information moves through our architecture. 

<img width="580" height="378"  alt="image" src="https://github.com/user-attachments/assets/1adcbe12-0eae-4a58-84b7-191cfed8e9e5" />

This diagram above does not contain any vendors names, this instead would be shown in a solution design. A Solution design provides a more detailed representation of our system architecture, including specific vendor solutions or platforms. It highlights the exact systems and technologies involved at each stage of data processing, offering a more concrete view of our solution landscape. 



## An Architecture Diagram 

Architectural diagram covers system deails, design diagram focuses on software!

So design focuses on the how and architecture looks at the what (slide diargram incorrect) 

An Architecture Diagram 
- explains what your building
- how stakeholders will interact with it
- the constraints of the systems
- often drawn in layers

A Design Diagram
- more technical design
- normally does not have stakeholders
- Focuses on one part of the system and shows its building blocks


why use these diagrams?
- helps with planning
- understand what teams are needed in delivery
- defines structure and high level decisions that guide how the system is built
- easy to see how systems will flow to each other
- can be viewed though various levels

## Explaining FLowcharts

<img width="1924" height="792" alt="image" src="https://github.com/user-attachments/assets/aeed23e1-d250-4012-ae76-1e201e445dfe" />

## Missue Deployment diagram 

- focus on secuirty , high level arch design
- Shows how attackers exploit weaknesses
-  Includes servers, databases, networks, and controls
- Aids in proactive risk mitigation
- Ensures data protection and system integrity

  Attacks include : SQL injection , spoofingetc. 
Risk migigation action such as gudies, phishing email checks 


## UML Component Diagram

<br>
<img width="608" height="318" alt="image" src="https://github.com/user-attachments/assets/2b8a22b0-b308-464c-992a-8eb33995da78" />
<br>
The purpose of a UML component diagram is to show the relationship between different components in a system

<br>

## System Componet Diagrams
<br>
<br>
<img width="1058" height="334" alt="image" src="https://github.com/user-attachments/assets/7dcf12f0-8454-4b57-9cd6-23845da59517" />

#### Example of a web based app:
<img width="1030" height="342" alt="image" src="https://github.com/user-attachments/assets/2cd973f0-b2b0-41b6-a08e-3291d4360bee" />
<br>
<br>

<b>Drawning Tools </b>
- LucidChart (online)
- Microsoft Visio (part of MS Office)
- Dia (free software)
- Draw.io (cloud based)


<b>Tips </b>
- Version Control your diagrams – they will evolve
- Simplify when possible, split when necessary

- Create logical groupings using polygons and colours
- Complement diagrams with descriptions
- Avoid too many acronyms
- You will normally have to explain the symbols you use


## Applying lenses, layers and chunks

<img width="1078" height="468" alt="image" src="https://github.com/user-attachments/assets/989352d0-c156-4b6b-b3c0-ae3cae82720c" />


### Integration architecture diagram

<img width="1588" height="1056" alt="image" src="https://github.com/user-attachments/assets/c6a019c3-0699-4354-afd9-4635c7a6752d" />


### Deployment architecture diagram

<img width="1862" height="976" alt="image" src="https://github.com/user-attachments/assets/0ca9d5ea-269e-444c-a6df-8e31555fcbb6" />

### Data architecture diagram

<img width="1222" height="468" alt="image" src="https://github.com/user-attachments/assets/ca4d4596-7ee2-428a-8f5b-08538813e512" />


<br> 

## Architecture Problem Space

What is the current user experience or product?
- What are the problems?
- How can it be improved?
- What assumptions have you made?
- New product or user experience?
- How do you think your propose design ideas support, change or extend current ways of doing things?

## Data Mesh Principles

A mesh is a technical approach to distrubed data ownership.
Domian driven,  ecosytem Goverance, Self serve infrastructure as a Platform 

<b>Data silos (each owner having storage mine cant use it ) > central data > leads to data mesh </b>
<br>
<br>

<img width="1044" height="522" alt="image" src="https://github.com/user-attachments/assets/e16c883f-f11f-4b55-ad41-5cba63d2a625" />

<br>
<br>


## Logical Diagram 

<img width="580" height="378" alt="image" src="https://github.com/user-attachments/assets/f763135e-fe9a-4c9d-96d5-972f7985a6d0" />

## Platform Architecture

<img width="2044" height="722" alt="image" src="https://github.com/user-attachments/assets/aea1da62-e715-4b89-81c1-7288a76f4ada" />
From the pre-cloud era and the dominance of Hadoop. 

Data ingress refers to external traffic entering an organisation's network, while egress denotes the opposite direction of data transfer.


## Lession 2 - Layered architecture
 
Enter the three-layered data architecture pattern – a strategic blueprint that has revolutionised the way enterprises approach data management.

<img  width="580" height="378" alt="image" src="https://github.com/user-attachments/assets/b0eb2e5a-a5d9-4379-aa1b-528d7a55ab79" />

<br>
<br>


### Data Storage layer

Benefits:
1. Scalability: Separating data storage from processing allows the system to scale more efficiently to handle larger volumes of data.
2. Security: It is possible to secure the data storage layer independently, which helps mitigate the risk of unauthorised access.
3. Data integrity: The data storage layer maintains data consistency and accuracy by enforcing data integrity constraints like unique keys and foreign key relationships.

### Data Processing layer

Filtering, sorting, aggregation, and transformation. It typically uses data processing frameworks like Apache Spark or Apache Flink, or stream processing engines like Apache Kafka. 

1. Performance: By processing data in parallel, this layer can achieve high output and low latency.
2. Flexibility: The data processing layer supports a diverse range of data processing tasks, from simple filtering to complex machine learning algorithms.
3. Resilience: It provides fault tolerance and automatic recovery, helping the system handle failures smoothly and stay operational.


### Data Presentation layer

The data presentation layer is responsible for displaying the data to end-users in a useful manner, this layer is usually implemented through a web application or business intelligence tools like Tableau or Power BI.

1. Usability: A user-friendly interface makes it straightforward for end-users to interact with the data and gain insights.
2. Customisation: The presentation layer can be tailored to meet a wide array of use cases and user preferences, offering a flexible and adaptable interface.
3. Integration: It can integrate with other applications and services to provide a seamless user experience, enabling users to utilise the data across different contexts.

Keep in mind the benefits of scalability, security, performance, and usability offered by this pattern as you continue your journey in data management.


## Lession 3 Microservices architectures 

A monolithic architecture is like a single large object that cannot be easily broken down into smaller pieces. Therefore makes it inflexible and difficult to make changes or scale specific parts independently.

A microservices architecture breaks down an application into small, independent services, each responsible for a specific business capability or domain. These services are loosely coupled, meaning they can be developed, deployed, and scaled independently without affecting the entire system.

<img width="580" height="378"  alt="image" src="https://github.com/user-attachments/assets/6a45cf52-feb1-4618-b494-a4226122e72a" />

<br>
<br>
They communicate with each other through well-defined APIs, much like how residents of a city interact with different service providers to fulfil their needs

Benefits include:
1. Decentralised services - Each service is a separate codebase, managed by a small development team, allowing for faster development cycles and easier maintenance.
2. Independent deployment - Services can be updated and deployed independently, without impacting the rest of the application, enabling faster bug fixes and feature releases.
3. Polygot programming - Services can be written in different programming languages and technologies, allowing teams to choose the best tools for their specific needs.
4. Scalability - Individual services can be scaled independently based on demand, optimising resource utilisation and improving cost-efficiency
5. Fault isolation - If one service fails, it does not bring down the entire application, ensuring better resilience and availability.
6. API Gateway - The API gateway acts as a single-entry point for clients, separating them from the internal services and enabling cross-cutting concerns like authentication, logging, and load balancing.


 ## Lesson 4 - Designing data products visually  


### Data Products 
Raw data alone is often insufficient to achieve these goals. Enter data products – valuable assets created by transforming raw data into actionable insights, tools, or services that deliver tangible value to the organisation and its stakeholders. 

Data products encompass a wide range of deliverables, including dashboards, reports, APIs, and data feeds. They are characterised by their relevance, accuracy, timeliness, and usability, making them indispensable assets for data-driven organisations.

<b>KPIS/ Objectives </b> <br>
Effective data products are closely aligned with business objectives and key performance indicators (KPIs). 
By understanding the organisation's goals and priorities, data architects can design products that address specific needs, support decision-making processes, and drive measurable outcomes.

<b>Valuable Data Products </b> <br>
Designing valuable data products requires a deep understanding of user needs, pain points, and workflows. Incoportates user feedback

<b>Understanding user needs/ pain points </b> <br>
By empathising with users and gathering feedback, architects can tailor data products to meet specific needs and deliver maximum value.

<b>Iterative development methodologies </b> <br>
terative development methodologies, such as Agile or Lean, are essential for building valuable data products. 
These approaches emphasise rapid prototyping, frequent releases, and continuous improvement based on user feedback. 
By incorporating user feedback loops into the development process, architects can ensure that data products evolve to meet changing business needs and user expectations.


### Wireframes: 
Purpose: Provide a basic structural outline of the data product, emphasising functionality over aesthetics.

### Mockups: 
Purpose: Add aesthetic elements like colour schemes and fonts to wireframes, offering stakeholders a more realistic view of the final product. 

### Prototypes: 
Purpose: Simulate user interactions with the product, instrumental in identifying usability issues before final development. 

For data engineers, interfacing with design teams for prototypes is crucial. 
This involves effective communication of technical constraints and data capabilities, ensuring prototypes align with the overarching business goals. (Real life example - speaking to data analyst around what they need in final powerBI table?) 


### Behavioural skills

1. Effective collaboration involves working closely with UX designers and stakeholders, fostering communication and teamwork to ensure prototypes meet the needs of all parties involved. (Maybe introducing at start of calls who is dealing with what regarding project?)
2. Providing constructive feedback on prototypes is essential, emphasising the integration of data functionalities to enhance the overall effectiveness of the product.
3. Taking an active role in prototype reviews and usability testing allows data engineers to advocate for data integrity and contribute valuable insights to the development process.
4. Professional development : Learning from interdisciplinary interactions and enhancing communication skills are crucial aspects of professional development for data engineers, facilitating effective collaboration and teamwork.

## Lesson 5 - Navigating data seas with architectural governance

To ensure effective governance and minimise risks, architecture modelling must consider various lenses such as usage patterns, data flow, physical setup, and networking. 

1. Usage patterns - Understanding how different user groups interact with the system aids in designing user-centric architectures.
2. Data flow - Visualising how data moves through systems identifies potential bottlenecks and security risks.
3. Physical setup - Considering the physical deployment of resources impacts performance, redundancy, and disaster recovery strategies.
4. Networking - Outlining network topologies and protocols ensures efficient data transfer and compliance with security policies.


By integrating data catalogues, dictionaries, and meticulous metadata management practices into our diagrams, we not only chart clearer paths but also fortify our governance strategies against the turbulent seas of data complexity.


<img width="580" height="378" alt="image" src="https://github.com/user-attachments/assets/14589dc4-9855-416e-8408-eea1d71280f4" />

<br>
<br>

By marking out where compliance checks are made, setting up access controls based on roles, and visualising security measures, we create solid defences to protect our data from cyber threats. 


1. Illustrating compliance checkpoints: Showing where and how compliance checks are integrated within the architecture
2. Role-based access control: Mapping out data access permissions ensures only authorised personnel can access sensitive data, supporting compliance with data protection regulations
3. Security protocols: Visualising security mechanisms reinforces the system’s defence against breaches.

TOGAF serves as a governance framework that ensures alignment with business goals, compliance with regulatory requirements, and promotes standardisation in data architecture. 


## Lession 6 summary 


- Diagrams act as visual maps to simplify complexity and promote alignment among teams in project management
- Sequence diagrams are a type of UML diagram used to visualise the timing and interactions between components within a system
- Use case diagrams provide a visual representation of how users interact with a system, aiding in understanding functional requirements
- Entity Relationship Diagrams (ERDs) illustrate the relationships between different data entities within an application or database
- In a three-layered data architecture:

      Data storage layer uses databases or data lakes for data persistence
      Data processing layer uses frameworks like Apache Spark for operations like filtering, sorting, transformation
      Presentation layer displays data to end-users via dashboards or reports

- A microservices architecture breaks down an application into small, independent services focused on specific business capabilities that can be developed, deployed, and scaled independently
- The API gateway acts as the entry point for clients in a microservices architecture, decoupling them from internal services and enabling cross-cutting concerns like authentication and logging

## Summary 

- Architecture diagrams are crucial for managing complexity and change in data systems
- Diagrams help convey key system aspects, initiate discussions, and provide different perspectives
- Applying lenses, layers, and chunks enhances system comprehensibility and adaptability
- Public cloud computing offers powerful capabilities for reliable data architectures
- Data Mesh promotes decentralised data ownership and empowers domain-driven data management



