
## GDPR Principles

<img width="2024" height="1062" alt="image" src="https://github.com/user-attachments/assets/65ddcabb-f709-4418-b5e3-4db2a9571110" />


<br>

<br>


<br> 

## Activity 1 : Match GDPR principles to real-world examples.


<img width="704" height="549" alt="image" src="https://github.com/user-attachments/assets/21428695-0029-4778-8a46-694fb56215e6" />


<br>

<br>


Answers: 

- A: •	Lawfulness, Fairness, and Transparency
- B: •	Storage Limitation
- C: •	Data Minimization
- D: •	Accuracy
- E: •	Integrity and Confidentiality (Security)
- F: •	Purpose Limitation
- G: •	Accountability


## Activity 2 : Addressing Legal Challenges in Data engineering 

<br>

<img width="745" height="1017" alt="image" src="https://github.com/user-attachments/assets/864e2ca1-3455-4e11-96d0-92e4515b0e68" />

<br> 


Activity 2 (20 mins):
Scenario-Based Discussion: Addressing legal challenges in data engineering.

1.	Identify and discuss the specific legal challenges presented in the scenario.
a.	Consider GDPR principles such as lawfulness, transparency, and accountability.
Lawfulness, Fairness, and Transparency - data is pre-GDPR compliant so may not have the required valid lawful basis, nor have the transparency required to share the data
Accountability - the marketing agency remains accountable, even if they choose to use a third party tool


b.	Analyse risks related to third-party data sharing.
    Risks include breach of confidentiality and security
    Lack of security guarantees and insufficient data processing agreements
    International data transfer risks
    Loss of customer trust
    Possible sharing of data without lawful basis

2.	Propose solutions to address these challenges.
a.	How can the agency ensure GDPR compliance while using the analytics tool?

Conduct a data protection impact assessement (DPIA)
Consider whether third party can provide the necessary guarantees to make the tool GDPR compliant - reconsider use if not
Agency should verify that third party tool has a clear privacy policy and retention policies


b.	What processes can be implemented to ensure customer data security and privacy?

Regular reviews of third 
Encryption (At rest) and TLS (In transit) 

c.	How can the agency communicate effectively with customers to rebuild trust?

Updated Privacy Notice to customers


## Activity 3 : Case Study Analysis – Facebook and Cambridge Analytica Data Privacy Scandal

About communication stratiegies and privacy. What has facebook done wrong?

<img width="674" height="266" alt="image" src="https://github.com/user-attachments/assets/2675d513-148e-4c8f-9ed8-a7d2c6209bf5" />

<br>
<br>


Activity 3

Discussion Points
1.	Identify the privacy gaps and ethical concerns in Facebook's data practices. Consider consent, transparency, and data security policies.
- Completely breached in terms of purpose limitation, as cambridge analytica was using the data for a new purpose
- Users completely unaware that their data was being farmed and used
- Poor transparency from Facebook, slow to act so accountability an issue too, even if they did eventually introduce new  policies

2.	Propose actionable solutions to mitigate such risks in the future.
a)	What changes could Facebook have implemented to comply with privacy laws?
- Explicit and informed consent to be obtained from users.
- Only use data for its original purpose.
- Additional security so that friend's data can't be retrieved alongside other accounts, friends who may not have consented.
- Did they properly know and vet what cambridge analytica were doing with their personality quiz? Could they have done more to identify issues before it was even rolled out.

 b ) How could privacy-by-design principles have prevented this issue?
- Ensured that data minimisation was in place so that it wasn't possible to pull back too much data using Facebook API
- Ensure users knew and had consented to what their data was going to be used for. 
- User data should remain private by default unless users actively go and choose to share it.


3. Suggest strategies for rebuilding user trust and preventing future breaches.
- Offer simply clear easy ways for users to manage their data and delete it.
- Default should always be set to private.  Only user can explicitly choose to share what and with whom.
- If completing something like a game or quiz, should be clear on that what data will be gathered and where it will be sent, privacy policy for user to agree to.


## Activity 4 : Designing a Privacy-byDesign Framework 


<img width="920" height="593" alt="image" src="https://github.com/user-attachments/assets/0554cb14-0cd7-417c-90de-edbec2e465de" />

<br> 

Activity 4:  Designing a Privacy-byDesign Framework

Review the scenario below about a mobile health app. 
• Identify key privacy considerations and challenges. 
• Collaboratively design a privacy-by-design framework. 
• Summarise your framework in a visual format (e.g., bullet points, table, or diagram) and prepare to present it in 2 minutes to the class. 


Discussion Points
1.	What privacy features can be implemented in the app to protect user data? Consider anonymisation, encryption, and role-based access.
- Encryption using TLS for data in transit, and encryption for rest data/ backups
- Strong authenication using MFA and strong password polcies , including biometric logins
- Role based access - based on what data each user should only see
- Anoymisation - giving customers a userID instead of being identified by personal details


2.	How will user consent be obtained and managed?
- Propose a mechanism for obtaining and updating consent.
- Use of tools such as OneTrust

3.	How will the framework ensure compliance with GDPR and HIPAA?
- Identify specific organisational policies and best practices.
- NIST Privacy Framework to create a standardised approach to privacy risk management

4.	How will you ensure data minimisation while delivering useful insights?
- Explore strategies for collecting only necessary data.
- Automatic deletion for data no longer required


