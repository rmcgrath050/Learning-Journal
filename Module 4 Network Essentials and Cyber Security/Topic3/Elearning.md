
# L5DE 4.3 - Designing secure architectures

In this lesson, you’ll explore the critical stages of developing, implementing, and monitoring a robust cybersecurity framework. Understanding these phases is essential for creating secure data products and pipelines that can withstand sophisticated cyber threats.


<img width="586" height="698" alt="image" src="https://github.com/user-attachments/assets/53472cd1-69d0-426e-a404-8ceda835c96a" />

#### Develop 
This includes identifying the organisation's specific security requirements, assessing risks, and defining security policies and procedures. During this phase, architects will reference established standards and best practices such as ISO/IEC 27001, NIST Cybersecurity Framework, etc. These standards provide guidelines for creating a comprehensive security strategy that addresses various aspects of cybersecurity, including data protection, access control, and risk management.


#### Implement
In the implementation phase, the strategies and plans devised during the development phase are put into action.
setting up technical controls like firewalls, antivirus software, encryption tools, and intrusion detection systems.
Administrative controls, such as security policies, training programmes, and incident response plans, are also established.
This phase often includes extensive testing to verify that the security measures function as intended and provide adequate protection against identified threats.


#### Monitor
The monitoring phase focuses on continuously observing and assessing the performance of the implemented security measures.
Tools such as Security Information and Event Management (SIEM) systems, automated threat detection, and regular audits are employed. Continuous monitoring allows for the timely detection of vulnerabilities and threats, ensuring that security measures remain effective against evolving risk.
Additionally, this phase includes reviewing and updating security policies and procedures to adapt to new standards, technologies, and threat landscapes. Regular reporting and analysis help in refining and improving the cybersecurity architecture


## 2. Secure network design

You will learn how to implement least privilege access, defence in depth, network segmentation, and other key strategies to protect your organisation’s information assets.
(Could mention service account prilage set up for GCP)

Secure network design is fundamental to protecting an organisation's information assets from cyber threats, ensuring confidentiality, integrity, and availability of data. Key design principles for creating a secure network include:
<br>
<img width="1846" height="992" alt="image" src="https://github.com/user-attachments/assets/3d851e36-bb73-46a5-8bf1-bfefc02c122c" />


## 3. The five rules of networking

This lesson will guide you through the essential principles of redundancy, scalability, security, manageability, and functionality. Understanding these rules will help you design networks that are resilient, efficient, and secure, supporting your organisation’s day-to-day operations effectively.

The Five Rules of networking provide a robust approach to support network functions to support your organisations in there day by day operations. The five rules are:

#### Rule 1 - Redundancy
Involves creating additional or alternative instances of network devices and communication mediums to ensure network availability and reliability. This approach is used to prevent or minimise downtime and service interruptions in the event of hardware failures, software crashes, network congestion, or other issues that can affect the primary network pathways.

By implementing redundant components such as routers, switches, data paths, and connections, organisations can ensure that if one part of the network fails, the data traffic can automatically reroute through another, maintaining continuous operation.

Redundancy can be achieved through various methods, including duplicate hardware, failover clustering, load balancing, and having multiple data centres.

The goal is to provide a seamless experience for users and maintain business operations without disruption, enhancing the overall resilience of the network against faults and failures.


#### Rule 2 - Scalability

Network scalability refers to the ability of a network to grow and manage increased demand without compromising performance or requiring a complete overhaul of the infrastructure. (Coudl compare GCP cloud scability to legacy hardware issues here) 
A scalable network is designed to accommodate growth in the number of users, devices, traffic volume, or application services efficiently and cost-effectively.

This is achieved through thoughtful planning and the use of scalable network architectures, such as modular hardware, flexible software solutions, and technologies like cloud services and virtualisation.

Scalability allows for the incremental expansion of network resources (such as bandwidth, storage, and processing capacity) to meet evolving needs, ensuring that the network remains robust, responsive, and capable of supporting new applications and technologies as they emerge.

Cloud Scalability is called elasticity - Cloud elasticity refers to the ability of a cloud computing environment to dynamically allocate and de-allocate resources as needed to accommodate fluctuating workloads.


#### Rule 3 - Security

Network security encompasses a broad set of policies, practices, and tools designed to protect the integrity, confidentiality, and accessibility of computer networks and data using both hardware and software technologies.

It aims to safeguard against unauthorised access, cyberattacks, and other threats that can compromise network operations and sensitive information.

Effective network security involves a layered approach that combines multiple defensive mechanisms at the edge and within the network. This includes firewalls, antivirus software, intrusion detection and prevention systems (IDPS), virtual private networks (VPNs), and strict access controls alongside regular security assessments, vulnerability scanning, and user education.


#### Rule 4 - Manageability

Network manageability refers to the ease with which a network can be monitored, configured, maintained, and optimised to ensure its efficient and effective operation. It encompasses the tools, processes, and policies that network administrators use to manage network resources, performance, and security.

Good network manageability allows for quick identification and resolution of issues, efficient allocation of resources, and adaptation to changing demands and threats.

This is achieved through a combination of network management software that provides comprehensive visibility into network activity, automated alerting systems for early detection of problems, and configuration management tools that enable rapid adjustments to network settings.


#### Rule 5 - Functionality

Network functionality encompasses the range of capabilities and services that a network is designed to provide to support communication among devices and facilitate the efficient and effective transmission of data.

This includes basic services such as connectivity, routing, and switching, which allow devices to connect to the network and communicate with each other, as well as more advanced functionalities like load balancing, fault tolerance, quality of service (QoS), and security measures designed to optimise network performance and protect data.


