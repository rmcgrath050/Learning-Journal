# L2 . Ethical and legal responsibilities of data engineers

## 1. Ethical considerations in data engineering

Ethical considerations in data engineering ensure that systems are fair, transparent, and accountable while protecting the rights of individuals.

Amazon implemented an AI-driven recruitment system to screen job applications but found that it disproportionately favoured male candidates for technical roles. This bias was due to the training data reflecting historical hiring patterns.

1. Amazon retrained the AI using more diverse datasets to mitigate bias.

2. They increased transparency by closely monitoring and adjusting the AI's decision-making process.
<br>
<img width="762" height="654" alt="image" src="https://github.com/user-attachments/assets/53062cee-9456-40b1-ae2f-0f8858281d0a" />
<br>

- Innovation vrs privacy : To address this, companies can make the process transparent by clearly explaining how data is used and allowing users to opt in or out.
- Efficiency vrs fairness : Addressing this issue requires data engineers to carefully select unbiased datasets and regularly test the system for discriminatory patterns.
- Profit vrs Social responsibility : In such cases, data engineers can help by setting limits on surge pricing or introducing discounts for users in need


## 2.  The trade-offs between innovation and ethics

<br>
<img width="726" height="610" alt="image" src="https://github.com/user-attachments/assets/d227699f-dc6b-41cc-9a8c-efc69bbb6012" />

<br>

#### Obligation 1: Secure system design

- Secure system design involves encryption, user authentication, and controlled access.
- Engineers use encryption protocols like SSL/TLS for data transfer, ensuring that sensitive information like test results cannot be intercepted.
- Firewalls and intrusion detection systems prevent unauthorised access to medical records.


 #### Obligation 2: Documentation and accountability

 - Accurate records ensure companies can demonstrate compliance during audits and investigations
 - Documentation includes maintaining logs of data access, processing activities, and breach reports.
 - This ensures accountability, as organisations can track who accessed patient records, when, and for what purpose
 - helping track suspicious activity and meet GDPR’s accountability requirements


#### Obligation 3: Stakeholder communication

- Data engineers must clearly communicate compliance measures and security protocols to stakeholders.
- This might involve employee training sessions, policy updates, or breach notifications


## L3 Ethical dilemmas and resolutions

- Ethical frameworks: Collaborated with experts to develop ethical guidelines for decision-making.
- Transparency: Shared algorithms and guidelines with the public, and engaged in community dialogues.
- Continuous improvement: Updated the system based on real-world data and ethical reviews


outcome : The company built a trustworthy AV system, increasing public confidence and setting a precedent for ethical considerations in autonomous vehicle development.

<br>
<img width="728" height="646" alt="image" src="https://github.com/user-attachments/assets/71e1438d-38ad-4c8e-b007-3144a573fa8a" />
<br>

Resolution: The company re-trained its AI using balanced datasets and included a human review step in the recruitment process.
Resolution: The platform updated its privacy policies, introduced transparency tools for users, and implemented stricter data access controls.
Resolution: Restricted the technology's use to specific high-risk areas and implemented oversight committees to monitor its deployment.


- Bias in AI - Re-trained algorithms with balanced datasets.
- Data privacy violations - Updated policies and implemented transparency tools.
- Surveillance Concerns - Restricted use and established oversight committees.

 <br>

 ## L4. Anonymising data while preserving utility

By applying anonymisation techniques like data masking or differential privacy, the council can analyse the data to make informed decisions without exposing sensitive details about individuals.

how to achieve this?
- Data masking: Account numbers and customer names were replaced with unique identifiers.
- Differential privacy: Noise was added to transaction amounts, ensuring that individual transactions could not be linked to customers.
- Synthetic data: Artificial datasets were generated to simulate high-value transactions for model stress testing.

<br>
outcomes: 
- The anonymised data enabled the fraud detection model to achieve 95% accuracy without exposing sensitive customer details.
- The bank remained compliant with GDPR and industry-specific regulations while enhancing its fraud detection capabilities.

1. Data Masking - Hides identifiable information by replacing it with fictional or scrambled data while retaining the structure and format.
2. Differential privacy - Adds statistical noise to datasets, preventing the identification of individual records while preserving aggregate trends, Think of a privacy "filter" that obscures details while keeping the big picture intact.
3. Synthetic data - This technique obscures sensitive data, such as names or account numbers, to prevent unauthorised access.

## L5. Legal and ethical implications of data anonymisation

<b>Legal Compliance:</b>
- Applied differential privacy to add statistical noise, preventing re-identification.
- Masked direct identifiers like names and addresses.

<br>

<b>Ethical Integrity:</b>
- Consulted ethics boards and patient advocacy groups to ensure responsible anonymisation practices.
- Analysed datasets to avoid exposing vulnerable subgroups (e.g., rare conditions).

<br>

<b>Outcomes:</b>
- Achieved GDPR compliance, avoiding potential fines.
- Retained 95% of the data’s analytical utility for the trial.
- Enhanced public trust by transparently sharing anonymisation policies.

##### Navigating legal and ethical dimensions of data anonymisation

his section explores the legal and ethical considerations of data anonymisation, highlighting the challenges and strategies for achieving this balance.


##### Legal Considerations

Laws such as GDPR and HIPAA mandate that data must be anonymised to an irreversible extent to prevent unauthorised identification of individuals. These laws require organisations to adopt techniques like k-anonymity, pseudonymisation, or differential privacy to protect personal data (GDPR Report, 2021).

#### Ethical Considerations
Ethical anonymisation is grounded in respect for individual privacy and autonomy. It involves obtaining informed consent and ensuring that the anonymised data cannot cause harm if misused 

#### Challenges Legal vrs Ethical
While strict anonymisation safeguards privacy, it can also limit data utility, posing challenges for organisations.
Over-anonymisation could lead to incomplete data, while under-anonymisation risks privacy breaches. 

## L6. Selecting tools and technologies for data anonymisation

Differential privacy is appropriate for census data, where the goal is to publish useful statistics while preventing re-identification.
Data masking is appropriate for database testing, where developers need realistic data without exposing real people's personal information.

<br>
Common tools for data anonymisation include the following:
- ARX : Provides robust anonymisation and re-identification risk analysis.
- Synthea : Generates synthetic healthcare datasets for research.
- Microsoft Presidio : Identifies and masks personally identifiable information (PII).

<br>
<img width="1612" height="784" alt="image" src="https://github.com/user-attachments/assets/b986edfa-0a12-4d4b-80f8-8eb5a2f1c4ca" />

## L7. Summary

- Ethical considerations are crucial in data engineering to ensure fairness, transparency, and accountability.
- Balancing innovation with ethical responsibilities requires careful navigation of trade-offs.
- Anonymisation techniques like differential privacy, synthetic data, and data masking protect privacy while maintaining data utility.
- Legal frameworks such as GDPR and HIPAA mandate strict anonymisation practices to prevent re-identification.
- Selecting the right anonymisation tools involves evaluating their scalability, compliance capabilities, and utility preservation.
