
## title hre

without clear roles it would lead to
- compliance risks
- operational inefficiencies
- data quality issues

#### Roles in order

<b>Data Owners</b> are senior leaders are responsible for ensuring data under their domain is managed appropriately. Use tools such as data governance framework and use collibra 
<b>Data Steward</b> - Responsible for maintaining data quality, standards and day to day use (Closest to the data) . enforces policies, 5 core pricnciples
<b>Data Custodians</b> -  manager data storage , backup and security

<br>

### 5 Core principles
- Accountability
- Data quality management
- security and compliance
- Collaboration and communication
- Lifecycle management

## Ensure Quality and Integrity 

<img width="2032" height="560" alt="image" src="https://github.com/user-attachments/assets/ac24cea2-34b4-4610-a207-477de6ac5e24" />

<br>
- monitoring: could be a python script, checking validation of inputs/ outputs 


<br>
<img width="1182" height="746" alt="image" src="https://github.com/user-attachments/assets/55190a57-0690-49e2-a816-719fe6b3905e" />

<br>


### Activity 1

- Data owners:
Description: Manages access to datasets and ensures policies are consistently enforced.
Responsibilities: Approve or deny access request , ensure compliance with access policies access policies, and maintain data security

- Chief Data Officer:
Description: Oversees data strategy and governance across the organisation, ensuring alignment with business goals and compliance.
Responsibilities: Develops governance frameworks, monitors compliance, and aligns policies with business priorities.

- Data Stewards:
Description: Maintains data quality and integrity in assigned domains.
Responsibilities:Perform regular data quality checks, implement standards, and resolve inconsistencies.


- IT Secuirty Manager:
Description: Manages the company's data security infrastructure and ensures data is protected against breaches.
Responsibilities: Enforces encryption, access controls, and authentication protocols; monitors and resolves security gaps.


RolePurpose
- Data Protection Officer (DPO)	Ensures compliance with GDPR, advises on privacy requirements, manages data protection impact assessments, and acts as the contact point for regulators.
- Compliance Manager	Monitors compliance with legal and industry regulations (e.g., GDPR, HIPAA), conducts audits, and ensures policies are followed throughout the organisation.
- Data Governance Committee	A cross-functional team that oversees governance initiatives, approves policies, resolves data-related issues, and aligns governance with business objectives.
- Business/Data Analysts	Help identify data quality issues, analyse business requirements, and ensure reliable reporting and decision-making.
- Training and Awareness Coordinator	Develops employee training programmes on data governance, security, privacy, and regulatory compliance to reduce human error.


2. How can each role contribute to resolving the identified challenges?
Issue 1 : Unauthorised Access Incidents : critical Roles : 1. Data Owners  2. IT security Manager . 3 CDO
Issue 2, CDO if compliance requirements are unclear
Issue 3: Data quality problems, Critical Roles: Data Stewards, Data Owners, CDO


### Activity 2

1. How effective are the current policies in addressing data governance challenges?
Good foundational basis however the data access control policy annual reviews are too infrequent and lack of role based access increase risk of unauthorised access 
Current policies  are setting themselves up for breaches as policy 1 is open to employees having access to data they don't really need, policy 2 is going to lead to over-retained records that breach GDPR, policy 3 is at risk of having data issues not being rectified in a timely manner

<br> 

2. What improvements could be made to align these policies with compliance standards like GDPR or HIPAA?
Data access policy: Implement role based access, apply principle of least privilege, conduct monthly reviews and maintain detailed audit logs for access acitivity, Introduce Multi-Factor Authentication (MFA) and automate access provisioning and de-provisioning.
Data retention policy: create a data retention schedule based on legal / business requirements, automated retention, redaction and deletion 

<br>  

3. How would your proposed changes enhance data quality, security, or compliance in an organisation?
- Reduced risk of unauthorised access
- Stronger protection of sensitive information
- Better incident detection
- Compliance Improvements
- Improved GDPR compliance
- Improved HIPAA compliance
- Stronger audit readiness
- Reduced risk of regulatory penalties

<br>

<img width="1184" height="764" alt="image" src="https://github.com/user-attachments/assets/83bd788f-f6a7-47c2-ad72-cd89e856d299" />

<br>

### Activity 3

(Designing a framework)
<br>

Develop a Governance Framework that includes the following:
1. Roles and Responsibilities:
a. Identify the key roles (e.g., Chief Data Officer, Data Steward,
Compliance Officer) and define their responsibilities.

Chief Data Officer (CDO):Provides strategic leadership for data governance, develops governance policies, monitors compliance, and aligns data practices with business objectives.
Data stewards to maintain data quality and monitor data accuracy, completeness and consistency
Data Owner : Accountable for specific datasets, approves access requests, ensures data is used appropriately, and owns data-related risk
Data Protection Officer (DPO): Ensures GDPR compliance, manages privacy impact assessments, oversees breach reporting, and acts as liaison with regulators
IT Security Manager: implements security controls such as encryption, MFA, role based access controls and also monitors security incidents 
Compliance Officer : Monitors compliance with GDPR, HIPAA, and internal policies; coordinates audits and regulatory reporting.
Data Governance Committee :Reviews governance performance, approves policies, resolves escalated issues, and drives continuous improvement.

2. Policies and Procedures:
a. Develop policies for data access, quality management, and compliance with GDPR and HIPAA.
b. Outline procedures for breach reporting, regular audits, and employee training.

- Data Protect sensitive data from unauthorised access.Implement Role-Based Access Control (RBAC), least-privilege access, Multi-Factor Authentication (MFA), and quarterly access reviews.
- Data Ownership Policy Establish clear accountability for all datasets.Assign Data Owners and Data Stewards to every critical dataset; maintain ownership register; review quarterly.
- Data Governance Committee :Reviews governance performance, approves policies, resolves escalated issues, and drives continuous improvement.


3. Governance Metrics:
a. Define measurable indicators to track governance success (e.g.,
percentage of datasets assigned ownership, data quality scores).
- Data Quality Score (% completeness, accuracy, consistency)
- Critical Data Element Compliance (% meeting quality standards)
- Data Ownership Coverage (% of data assets with assigned owners)
- Data Stewardship Coverage (% of domains with assigned stewards)
- Data Policy Compliance Rate (% adherence to governance policies)
- Access Review Completion Rate (% of access rights reviewed on schedule)
- Data Incident Count (privacy, security, or quality incidents)
- Issue Resolution Time (average time to resolve data issues)
- Metadata Completeness (% of assets documented in the data catalog)
- Regulatory Compliance Findings (number of GDPR/HIPAA audit findings)
- Data Retention Compliance (% compliance with retention policies)
- User Training Completion Rate (% of staff completing governance training)
- Percentage of datasets with assigned Data Owners Measure accountability and ownership coverage 100%


<img width="1478" height="614" alt="image" src="https://github.com/user-attachments/assets/00b0f7bd-f1da-42b0-8848-392237f1f174" />
<br>
<br>

### Activity 4

1. What stewardship practices exist in your organisation, and how do they align with stewardship principles?
- Data Governance Council and within that we have CDO, Data Owner, Data Stewart, Legal, Data Architecture, Data Custodians (SME's probably fit here), IT Security
- Data Steward practices - Monitoring data arrival and processing, Access control and approval, Maintaining metadata and processing history, Data-quality issue resolution, Database maintenance and integrity checks, Incident monitoring and escalation and data-quality validation
- Role based access control, and mandatory employee training 
- Legal - contracts with 3rd party companies on how data is handled - usage, retention, security

2. Which principles (e.g., accountability, transparency, compliance) are best demonstrated by these practices?
- Accountability - assigns clear responsibility to data stewards
- Transparency - Employees are informed about how customer data is collected, used, stored, and shared, helping to promote openness and trust.
- Availability - authorised users have reliable access to critical systems and data when needed through infrastructure monitoring, server and service alerts, disk-space checks and the investigation of failed or delayed jobs.
- Governance - governance framework that defines policies, standards, roles, and responsibilities for managing data across the organisation


3. Are there gaps or areas where stewardship practices could be improved?
- Greater automation to detect errors/ duplicates 

4. How do these practices enhance data governance and compliance
- Problems are detected and escalated
- Access is limited to authorised users
- Responsibility for issues can be identified
- Systems remain reliable and available
- Evidence exists for audits and investigations (paperwork!!!)
- Regulatory compliance: Policies and procedures help comply with the UK GDPR, Data Protection Act 2018, and regulations from the Financial Conduct Authority (FCA) and Prudential

<br>

<img width="1124" height="450" alt="image" src="https://github.com/user-attachments/assets/25d4ac1a-eb49-4b7c-8b53-076c0d24d435" />
<br> 
<br>
<img width="1426" height="686" alt="image" src="https://github.com/user-attachments/assets/59c0124f-a189-4d79-866b-44f0b9fcdfe7" />
<br> 

### Activity 5


