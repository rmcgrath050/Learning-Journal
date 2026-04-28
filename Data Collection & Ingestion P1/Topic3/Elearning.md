# 5DE 6.3 - APIs and Microservices for data engineers

#### API
Definition: APIs allow two or more applications to communicate by providing a set of procedures and functions.

Use Cases:
- Data Retrieval: Fetch data from databases, external services, or APIs.
- Integration: Connect different components within an application.
- Communication: Facilitate interactions between microservices.
<br>

benefits include:
- Adaptation: APIs help to anticipate changes. This is especially important for data migration as the APIs make service provision more flexible.
- Automation: By using APIs, companies can update workflows to make them quicker and more productive through automation.
- Efficiency: With APIs, the content generated can be automatically published, making it readily available for every channel. This allows the sharing and distribution of new content to occur instantly.
- Integration: APIs allow content to be immersed from any site or application more efficiently. This allows for more content fluidity and an integrated user experience.
- Personalisation: With APIs, developers can customise the content they want delivered in terms of when and where it is supposed to go.


#### MicroServices
Definition: Small, independent blocks within the data engineering ecosystem.

Benefits:
- Isolation: Modify a microservice without impacting the entire system.
- Fault Tolerance: Errors in one microservice don’t bring down the entire system.
- Language Agnostic: Microservices can run on different programming languages.
- Cost-Efficiency: Elastic scaling based on need.

<br>
other benefits:
- Faster Time-to-market: With microservices, developers can build one component, test it, and then deploy it individually, reducing the time to create a finished application.
- Reduced Risk: By isolating the code, developers can work on several modular but separate blocks at a time. This reduces the risk of making drastic changes that could damage the whole application.
- Productivity: Individual teams being able to work on different components enables better quality assurance. With one team testing and another deploying, deadlines are better predicted than with a monolithic application.
- Security: By connecting microservices through secure APIs, data processing is enhanced by specifically authorising applications, users, and servers, ensuring greater security.
- Scalability: As demand increases, microservices make it possible to channel the resources to the areas only where the microservice is being impacted by increasing demand. In addition, container orchestration tools can scale the microservice automatically and reduce downtime.
- Better fault isolation: If one microservice fails, all the others will likely continue to work. This is a key part of the microservices architectural design.
- Simplified debugging and maintenance: Building individual microservices is easier than coding for a monolithic architecture; developers can be much more productive when debugging code and performing maintenance.
- Future-proofed applications: When innovations happen and new or updated technology disrupt your software development process, microservice architectures makes it easier to respond by replacing or upgrading the individual services affected without impacting the whole application.

<br>
<img width="1084" height="576" alt="image" src="https://github.com/user-attachments/assets/c0e7e9bc-cb6a-4f2c-9ded-35228b9e83f1" />

<br>
<br>
With the introduction of microservices, large coding projects could break apart applications into a set of small, independent processes. Here the applications are simpler to build and maintain when broken down into smaller modules that work seamlessly together. These modules communicate with each other through simple, universally accessible APIs. 


<br>
<img width="748" height="574" alt="image" src="https://github.com/user-attachments/assets/8481db9f-5b92-482c-8af6-d99ea0802aa8" />
<br>
<br>


Microservices help data engineers overcome the following challenges related to monolithic architectures, including:
1. To make a minor change to the backend component of the architecture, the monolithic system needs to be restructured/revisited.
2. Deployment time proportionally increases along with new feature requests into the monolithic system.
3. Even after a minor change to the monolithic codebase, a thorough inside-out regression testing needs to be done before the code is deployed in production.

<br>
<br>

Microservices benefit from 'loose coupling' in the following ways:
- Within a massive code base, you can surgically modify a microservice without impacting the entire system.
- An erroneous microservice will not necessarily bring down the entire system. It would only impact a specific area.
- One microservice’s development, deployment, and continuous integration does not affect nor impact neighbouring microservices or the entire ecosystem.
- Logs are captured for an individual microservice vs. an entire ecosystem. This reduces debugging time.
- Even if a bunch of microservices are sequentially connected they all can still run on different programming languages and logic to achieve the same overarching goal.
- One microservice ideally addresses one core functionality to achieve a service-oriented architecture, which is one the best methodologies when it comes to building data applications.

<br>
In short, microservices are more about the software architecture, while the APIs deal with how to expose the microservice to a consumer. In other words, APIs are the entry point for microservices. They act as gatekeepers, doing all the basic functionalities before passing the request to the respective application, allowing the end-user to interact with the application.
<br>
<br>
<img width="1100" height="546" alt="image" src="https://github.com/user-attachments/assets/6a65c760-ea09-490b-bcdb-6338c963abd0" />

<br>
Meanwhile, APIs allow the standardised mechanisms for web governance – the inspection mechanisms that are looking to make sure everything is where it should be and configured correctly – while retaining development agility and making the reuse and discoverability of microservices possible.

