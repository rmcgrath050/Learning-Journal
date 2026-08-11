# L5DE 9.4 Compliance and risk reporting

## L1. Identifying relevant compliance standards and regulations

#### Compliance challenges 

- Inconsistent regional practices: Different teams used varying data retention policies, creating compliance risks
- Data breaches: A lack of encryption for some customer data led to a costly breach.
- Auditing difficulties: Without clear documentation, the company struggled during regulatory audits.

The solution : The company implemented a unified compliance framework, appointing compliance officers in each region. This included standardised encryption practices, a global data catalog to track data lineage, and automated compliance monitoring tools. The result was a 40% improvement in regulatory audit success and a significant reduction in data-related risks.

<br>
<img width="1104" height="784" alt="image" src="https://github.com/user-attachments/assets/40017238-2784-42b1-b051-3781ee791fb5" />
<br>

#### GDPR
- The General Data Protection Regulation (GDPR) focuses on protecting personal data and privacy for individuals within the European Union.
- It ensures that organisations process data lawfully, minimise data usage to what is necessary, and secure explicit consent from users.
- GDPR also provides individuals the "right to be forgotten," which allows them to request the deletion of their personal data (Eryurek & Gilad, 2021).

#### DPA
The Data Protection Act (DPA) in the UK complements GDPR but includes specific updates for the UK post-Brexit.

<b> EPA Question: "How would you ensure a data pipeline complies with data protection requirements?"</b>
<br>
A strong answer could mention:
"I'd first establish whether the data contains personal or sensitive information and identify the lawful basis for processing. I'd apply data minimisation and purpose limitation, restrict access using appropriate permissions, encrypt data where appropriate, consider retention and deletion requirements, and make sure data isn't exposed unnecessarily through logs, development environments or downstream systems. I'd also follow the organisation's data governance policies."
<br>

When collecting data, compliance standards like GDPR and CCPA require explicit user consent and transparency about how the data will be used. During data processing, techniques like pseudonymisation or anonymisation are essential to protect sensitive information, particularly under HIPAA and GDPR. Storage practices must include encryption and adherence to retention policies, as outlined in SOX and PCI DSS. Finally, data engineers must ensure clear documentation and data lineage to pass audits and meet ISO 27001 requirements 

<br>

## L2. Compliance strategies and best practices

1. Policy Standardisation: The organisation implemented a global compliance strategy, aligning data protection policies with GDPR and PCI DSS requirements.

2. Training Programs: All employees underwent training on compliance best practices, focusing on secure data handling and breach protocols.

3. Automated Monitoring: Real-time monitoring tools were deployed to track data access and flag anomalies.

4. Incident Response Framework: A standardised response protocol was introduced to handle potential data breaches.


#### Policy development
For example, creating a standardised data retention policy ensures organisations store data only for as long as necessary, aligning with regulations like GDPR. Policies also define expectations for secure data handling, giving employees and stakeholders a foundation for compliance practices.

#### Colleague training 
Training workshops and online modules help teams identify risks such as phishing attempts or data breaches. This consistent education fosters a compliance-first culture, where individuals are equipped to manage data responsibly and recognise vulnerabilities.

#### Automated Compliance tools
Another critical element is the use of automated compliance tools. Technologies such as real-time data monitoring systems can flag potential breaches, track data lineage, and ensure encryption protocols are active. For instance, automated tools can verify that payment transactions comply with PCI DSS standards by encrypting sensitive information in real time.


#### Reg Risk Assessments 
Finally, regular risk assessments identify and address vulnerabilities in data management systems. For example, reassessing encryption protocols every six months ensures they remain robust against evolving cyber threats.

<br>
What can we learn from this diagram? The connection between compliance strategies and best practices
1. Strategy: Policy creation and risk identification.
2. Implementation: Training, monitoring tools, and process updates.
3. Assessment: Regular audits and risk assessments.
4. Improvement: Iterative updates to strategies and practices.

##### Answers 
- Best Practice - Regularly updating encryption protocols
- Policy Development - Conducting breach response simulations
- Proactive Incident Management - Conducting breach response simulations
- Centralized Data Catalogue - Establishing a centralised data catalogue


### Example for EPA about lloyds bank:
<i>Challenge: Lloyds had a regulatory requirement to provide customers with information about accessing their payment transaction history when they closed their account. Their processes failed to consistently provide this information, affecting around 360,000 former customers.</i> 

Resolution: Lloyds changed the account-closing process so the information was included in the closing statement. They also introduced reconciliation controls to compare account closures against closure statements, helping identify missing records and prevent the problem recurring.

Data engineering relevance: This demonstrates why data quality, reconciliation, validation and automated controls are important in a regulated organisation. A data engineer could help build automated checks that compare source records against downstream outputs and flag discrepancies before they result in a regulatory breach.

https://www.gov.uk/government/publications/breaches-of-the-cmas-markets-and-mergers-remedies/register-of-breaches-2024?utm_source=chatgpt.com

<br>

## L3.  Selecting tools for monitoring and ensuring compliance


1. Tool Selection: The institution deployed automated compliance monitoring tools, such as SIEM (Security Information and Event Management) systems, to track security events and flag anomalies.

2. Integration: Tools were integrated across departments to create a unified compliance framework, linking to existing data catalogs and encryption systems.

3. Real-time Dashboards: Custom dashboards were developed to display compliance status, audit trails, and risk assessments.

4. Regular Training: Employees were trained to use these tools effectively, ensuring alignment with best practices.


#### Tools

- Security Information and Event Management) systems track security events, identify breaches, and maintain detailed audit trails.
- Data Loss Prevention : monitors sensitive data flows to prevent unauthorised access or sharing.
- Compliance automation Platform: 



