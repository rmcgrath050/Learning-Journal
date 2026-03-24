# Topic 5 - Migrations, archiving, monitoring and disaster recovery

Analyse typical types of cloud migration projects, including failed ones, and explain how to document “lessons learned”. 
Develop archiving policies and frameworks. 
Explain the significance of introducing redundancy for performance and availability. 
Explain the importance of, and the differences between, business continuity management, disaster recovery, and incident response. 
Deploy and monitor cloud-native applications using Azure Monitor and Python monitoring services. 


<br>

#### BCM 
BCM is the comprehensive approach by which organisations prepare for, and ensure the maintenance of, critical functions in the face of disruptive events.

Includes:
- restoration of IT services
- maintaining essential operations,
- managing communication with stakeholders
- safeguarding legal and regulatory compliance.

For instance, even as the cyber-attack unfolds, a pre-established BCM strategy ensures that client services continue via secondary systems and manual processes, thus upholding the firm’s operational integrity.


#### DR

- This aspect focuses specifically on the recovery of IT infrastructure and data access after a disaster strikes.
- It is a subset of BCM but with a narrower scope, concentrating primarily on technical recovery and data integrity.

After a finanincal attack, the DR protocol kicks in immediately after the attack is detected, involving steps such as switching to a backup data centre, restoring data from secure backups, and deploying advanced malware removal tools to cleanse the network, aiming for a swift resumption of services.


#### Incident Response

IR deals with the immediate reaction to an incident, aiming to limit damage and reduce recovery time and costs.

- this process involves detailed planning that includes incident identification, escalation procedures, mitigation steps, and documentation.

At Sterling Finance, the IR team springs into action by first containing the breach to prevent further damage, followed by forensic analysis to understand the breach’s extent and origins.


<img width="776" height="530" alt="image" src="https://github.com/user-attachments/assets/308afe80-67ee-49c9-9609-6d457f6d4446" />

## Lession 2 - Cloud migration

Cloud migration involves moving applications, data, and infrastructure from on-premises environments to cloud platforms. 
<br>
<img width="582" height="564" alt="image" src="https://github.com/user-attachments/assets/bf08e3b5-812f-4f5b-8f97-9802da7f454b" />

The Power/Interest matrix is a strategic framework used to categorise stakeholders into four quadrants based on two primary factors, namely, their power to influence a subject and their level of interest in its outcomes.


- High Power/ Higher Interest , Stakeholders with a lot of power and a strong interest in the project's outcomes. These stakeholders are important and require close collaboration.
- High Power / Low Interest, Stakeholders with a lot of power but not much interest in the project's outcomes. These stakeholders should be kept satisfied without being overwhelmed with communication.
- Stakeholders with limited power but a strong interest in the project's outcomes. These stakeholders can be helpful with project details and should be kept informed
- Lower Power / Low Interest, Stakeholders with limited power and interest in the project's outcomes. These stakeholders should be monitored and kept informed, but not overwhelmed with communication.

#### Successful migration Scenario 

The company adopted a phased migration strategy, starting with non-critical applications to gain experience.
They conducted thorough planning, involving cross-functional teams to assess application dependencies, data requirements, and compliance considerations.

1. Comprehensive Planning: Detailed assessment of the existing infrastructure and clear migration roadmap.
2. Stakeholder Engagement: Involving IT, business units, and external partners to ensure alignment.
3. Testing and Validation: Rigorous testing in a staging environment before production deployment.
4. Training and Support: Providing training for staff to manage and operate cloud services effectively.


### Lessions Learned:
The importance of phased migration to mitigate risks!
Ensuring that all stakeholders are involved and informed throughout the process, using the power/interest framework (example above)!
Allocating sufficient time for testing and validation to prevent post-migration issues!

#### Failed migration Scenario 

The project faced significant challenges, ultimately leading to failure and reverting to on-premises systems

1. Lack of Compatibility: Legacy systems were not compatible with the cloud environment, requiring extensive re-engineering.
2. Insufficient Planning: Underestimating the complexity of migrating mission-critical systems.
3. Security and Compliance Issues: Failure to meet regulatory requirements for data protection and privacy.
4. Resistance to Change: Lack of buy-in from key stakeholders and insufficient training for staff.

### Lessons learned:
The necessity of conducting a thorough feasibility study before migration!
Understanding the limitations of legacy systems and the potential need for re-architecting applications!
Prioritising security and compliance considerations, especially in regulated industries!
Managing organisational change effectively by involving stakeholders and providing adequate training!


### Documenting lessons learned

Documenting lessons learned involves capturing the experiences, challenges, and outcomes of migration projects. This process includes:
- Post-Migration Reviews: Conducting meetings to discuss what went well and areas for improvement.
- Creating Reports: Documenting findings, decisions made, and their impacts.
- Sharing Knowledge: Distributing lessons learned across the organisation to inform future projects.
- Continuous Improvement: Implementing changes based on feedback to enhance processes and methodologies.


## Lession 3: The importance of robust archiving policies and frameworks

Imagine a global financial institution facing a regulatory audit. The auditors request access to historical transaction records spanning the last decade. However, due to inadequate archiving policies, the institution struggles to retrieve the necessary data, leading to compliance issues and hefty fines.

In this lesson, we will explore the significance of effective archiving, best practices for developing and implementing archiving policies, and the challenges organisations face in managing archived data. By examining real-world examples, we will highlight how proper archiving can ensure regulatory compliance, support legal needs, and provide valuable business insights, ultimately transforming historical data into a strategic asset.


The significance of archiving:
- Regulatory Compliance: Many industries are subject to regulations that require data retention for specific periods (e.g., financial records, medical data).
- Legal Considerations: Archived data may be needed for legal proceedings or audits.
- Business Intelligence: Historical data can provide valuable insights for strategic decision-making.
- Cost Management: Archiving reduces storage costs by moving infrequently accessed data to cost-effective storage solutions.

<br>
Best practies of archiving include:
- Policy Development: Define clear policies outlining what data should be archived, retention periods, and access controls.
- Classification of Data: Categorise data based on sensitivity, importance, and regulatory requirements.
- Secure Storage Solutions: Use reliable and secure storage options, such as cloud-based archival storage (e.g., Azure Archive Storage, Amazon Glacier).
- Data Integrity and Preservation: Implement measures to ensure data integrity over time, including checksums and regular validation.
- Access Management: Control who can access archived data, implementing strict authentication and authorisation mechanisms.
- Disaster Recovery Integration: Include archived data in disaster recovery plans to ensure it can be restored if needed.



#### Challenges in Archiving

- Data Growth: Managing the increasing volume of data requires scalable archiving solutions.
- Format Obsolescence: Ensuring that daData redundancy involves storing copies of data in multiple locations or systems. Introducing redundancy enhances performance and availability by providing alternative pathways for data access and recovery in case of failuresta remains readable despite changes in technology and file formats.
- Security Risks: Protecting archived data from unauthorised access and breaches.


By adhering to best practices such as clear policy development, data classification, secure storage, and disaster recovery integration, organisations can ensure compliance, support legal needs, and gain valuable business insights.

<br>

## Lession 4 - Introducing redundancy for performance and availability

However, thanks to a robust redundancy strategy, the retailer's systems remain operational even when a critical server fails. This seamless experience is made possible by storing copies of data in multiple locations and having alternative pathways for data access and recovery.

Data redundancy involves storing copies of data in multiple locations or systems. Introducing redundancy enhances performance and availability by providing alternative pathways for data access and recovery in case of failures. 
Redundancy is a fundamental principle in designing resilient systems that can withstand hardware failures, network issues, or other disruptions.


#### Benefits include:
- Improved Availability: Redundant systems, such as systems following the Active/Standby set-up, ensure that services remain accessible even if one component fails.
- Enhanced Performance: Distributing data across multiple systems can balance loads and reduce latency.
- Data Protection: Redundant data storage protects against data loss due to hardware failures or corruption.
- Disaster Recovery: Redundancy facilitates faster recovery times during disasters by having backups readily available

<img width="534" height="582" alt="image" src="https://github.com/user-attachments/assets/2514ee86-cbd1-4f2d-9718-4604f3d4c7fd" />

<br>
Best practices for implementing redundancy include:
- Replication Strategies: Use data replication techniques, such as synchronous or asynchronous replication, to keep data copies up to date.
- Geographical Distribution: Store redundant data in different geographic locations to protect against regional disasters.
- Redundant Infrastructure: Implement redundant network paths, power supplies, and hardware components.
- Regular Testing: Conduct failover tests to ensure that redundant systems function correctly when needed.
- Monitoring and Alerts: Monitor redundant systems for synchronisation issues or failures, setting up alerts for timely intervention.
- Cost-Benefit Analysis: Balance the costs of redundancy with the benefits, ensuring that investments align with business priorities.



