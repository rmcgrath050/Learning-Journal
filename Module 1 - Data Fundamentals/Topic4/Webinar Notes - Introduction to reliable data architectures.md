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




## Summary 

- Architecture diagrams are crucial for managing complexity and change in data systems
- Diagrams help convey key system aspects, initiate discussions, and provide different perspectives
- Applying lenses, layers, and chunks enhances system comprehensibility and adaptability
- Public cloud computing offers powerful capabilities for reliable data architectures
- Data Mesh promotes decentralised data ownership and empowers domain-driven data management



