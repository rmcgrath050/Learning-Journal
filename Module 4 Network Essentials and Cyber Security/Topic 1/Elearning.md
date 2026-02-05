# Introduction to networks for Data Engineers

#### Key Definitions

- Router: A device that forwards data packets between computer networks, creating an overlay internetwork.
- Local Area Network (LAN): A network that connects computers within a limited area such as a residence, school, or office building.
- Access Point: A device that allows wireless devices to connect to a wired network using Wi-Fi or related standards.
- Firewall: A network security system that monitors and controls incoming and outgoing network traffic based on predetermined security rules.

<img width="756" height="564" alt="image" src="https://github.com/user-attachments/assets/0d6c4575-5362-41cb-ae84-daeff7afcfbe" />


### TCP / IP and the OSI layer model

In the digital age, understanding network models such as TCP/IP and OSI is not just beneficial, it’s essential. These models serve as the backbone of internet communication, enabling data to be transmitted efficiently across diverse networks. The layered design of these models allows for systematic troubleshooting, speeding up the problem-solving process by isolating network issues effectively.

TCP/IP (Transmission Control Protocol/Internet Protocol) is a set of rules that allows computers to communicate over the internet. Think of it as the language that computers use to talk to each other, ensuring that data sent from one computer arrives accurately and in the right order at another computer.

#### TCP 
- Understanding TCP/IP helps you become more tech-savvy and better at troubleshooting connectivity issues.
- The TCP/IP model is fundamental in ensuring reliable data transmission across diverse networks.
- It serves as the backbone for internet communication by defining how data should be packetized, addressed, transmitted, routed, and received.

#### OSI Model
- The OSI model provides a more detailed and structured framework for network architecture.
- It divides network communication into seven distinct layers, from physical transmission to      application-specific functionalities.
- By compartmentalising network functions into layers, the OSI model complements the practical framework of TCP/IP.
- This enhances our conceptual understanding and enables more robust, adaptable network design and operation.

#### Other Protocols
- The TCP/IP model is not the only model used to represent the traffic on the internet.
- There are more protocols in modern networks, and they can be neatly mapped to the             comprehensive OSI model (Open Systems Interconnection Model).


#### Understanding the OSI Model

<img width="736" height="608" alt="image" src="https://github.com/user-attachments/assets/a9949da3-1fe2-4953-b098-d825687cfeac" />

We can describe the OSI Model as a conceptual framework used to understand and implement network communications. It divides the communication process into seven distinct layers, each with specific functions.
<br>
The TCP/IP model can be seen as part of the OSI model, where data can be mapped from a high-level application to the physical transmission.

<br>
The OSI Model helps network engineers and IT professionals understand the complex interactions in network systems, making it easier to design, manage, and troubleshoot networks.


<br>
<br>

Imagine planning a road trip:
- Physical Layer: The actual roads and vehicles.
- Data Link Layer: Traffic lights ensuring orderly driving.
- Network Layer: Network Layer: a map with all intersections, junctions and building numbers clearly marked.
- Transport Layer: The traffic light system and the smart motorway traffic updates.
- Session Layer: Your phone keeping the GPS session active.
- Presentation Layer: Your GPS app translating satellite data into readable maps.
- Application Layer: The GPS app itself that you interact with


#### OSI Model Steps
- Physical Layer: Physical hardware connections.
- Data Link Layer: Direct data transfer and error correction.
- Network Layer: Routing data to its destination.
- Transport Layer: Ensuring complete data transfer.
- Session Layer: Managing sessions between applications.
- Presentation Layer: Translating and encrypting data.
- Application Layer: Interacting with user applications.


<br>
TCP/IP (Transmission Control Protocol/Internet Protocol) is a set of rules that allows computers to communicate over the internet.
It ensures that data sent from one computer arrives accurately and in the right order at another computer.


## Modern networking practices

Logical networking involves the configuration of networks that are largely independent of the physical setup. Instead of relying on hardware alone, logical networks utilise software to manage, segment, and secure network traffic.

- At the core of logical networking, virtualisation allows for the creation of multiple simulated environments or dedicated resources from a single, physical hardware system. This is often used to run multiple virtual servers on a single physical server.
- SDN provides an agile networking infrastructure that is centrally controlled through software applications. This helps automate and fine-tune network resource management, improving flexibility and responsiveness.
- NFV decouples network functions from traditional hardware appliances, enabling them to run in virtual environments. This reduces dependency on specific hardware, lowers costs, and increases deployment speed for network services.

- 
