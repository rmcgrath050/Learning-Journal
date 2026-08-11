#### Plan

By the end of today you'll be able to:
- Work out which rules actually apply - and why "we're not in the EU" isn't the answer people think it is
- Turn a regulation into an action - and say which requirement justifies it
- Pick the right control for the right failure -not the tool with the best marketing
- Tell a director and an engineer the same bad news - two versions, both true
- Look at a dataset and say what's wrong with it - in language a regulator would recognise

Write a risk report someone acts on - the only kind worth writing
-----------------------------------------------
- What you will have by the end- 
- One finished risk report. Built from a real case study, in your own words. Good practice for your professional discussion.
- Compliance is the proof. Risk reporting is what you write when the proof isn't there!!!!



- GDPR tells you what u owe people
- ISO-21001 gives you the machinery needed to deliver it


** this diagram useful for activity 2:
<br>
<br>
<img width="672" height="572" alt="image" src="https://github.com/user-attachments/assets/446caac4-27fb-4ce6-b22d-3fc659688d9e" />
<br>

<img width="910" height="516" alt="image" src="https://github.com/user-attachments/assets/27e17f7c-c150-4429-a398-721d7ed5c796" />

#### Actvity 4 mapping :

<img width="1716" height="1086" alt="image" src="https://github.com/user-attachments/assets/67c39a2b-c843-4e2f-889a-5ded516a6aa2" />


<br>

### Activity 1 Answer:

1. What are the key compliance standards applicable in this scenario (e.g.,
GDPR, HIPAA, ISO 27001)?
GDPR - Cannot Delete/Access Data - Forms out of date, Transfer of data
HIPPA - Medical Data, Breach notification delayed, Transfer of data
ISO 27001 - Asia no encryption - Possibly the Transfer of data too.

2. How do the standards affect each role’s responsibilities and challenges?
Sophia - Her problem is organisation-wide governance, Different regions have different controls.
Emily - Make sure data is available and PII is not exposed between regions. Additional Training
Rajesh - Responsible for tech security, protect data, implement encryption, data anonymisation. Fix Vulnerabilities
Jake - Update consent forms to standard,

#### upgrade to distinction 
- rajesh should deploy SIEM specifically to close the delayed-breach-notification gap.
- HIPAA requires timely reporting, and you cannot report a breach that you have not detected -
- detection latency as the root cause, not the reporting process.
- The trade-off is alert volume- an under-tuned SIEM in a hospital would generate enough noise so people are going to ignore it. As a result, I'd tune against high-sensitivity access patterns before switiching it on fully 

4. What steps can the team take to align practices across regions while addressing local regulations?
5. How can Global HealthCorp rebuild patient trust and avoid further legal or reputational damage?


### Activity 2 

Develop a compliance strategy to address the following challenges:
1. GDPR Compliance:
a. How will you ensure customers give informed consent for data
collection?
- Policies of consent in place, including retention policy - customers need to confirm twice the consent to hold data, detailing how long and why this is retained, how its used etc
- auditing to have evidence of these choices and monitoring this is in place
- Whether it is used for personalised advertising/recommendations
- How customers can withdraw consent

Justifications: 
- GDPR requires transparency so individuals understand how their personal data is processed.
- Consent under GDPR must be freely given, specific, informed and unambiguous
- GDPR requires withdrawal of consent to be as easy as giving consent.

- 
b. What steps will you take to manage and enforce data retention
policies?
- have internal governance frameworks set up and collibra used to manage standardisation across teams
- Create a schedule via automation and establish a maximum retention period for each type of data
- Establish a data inventory

Justification: 
- GDPR's storage limitation and data minimisation principles require organisations not to retain personal data longer than necessary for its purpose
- Automation reduces the risk of employees forgetting to delete information and creates consistent enforcement across customer records

3. Data Security:
a. How will you implement encryption to protect payment information and
meet PCI DSS requirements?
- encryption on data transfer and data at rest though
- ShopNow should avoid storing raw card information altogether and use tokens instead
- Implement strong key management
- Implement multi-factor authentication
- Apply least-privilege access
- Deploy SIEM and security monitoring. The SIEM can detect suspicious patterns such as repeated failed logins, unusual geographic access or large data exports.

Justifications: 
- PCI DSS requires organisations to protect payment account data using appropriate technical controls. Encryption significantly reduces the impact of unauthorised access.
- Reducing the amount of cardholder data stored reduces the potential impact and scope of a payment data compromise and can simplify PCI DSS compliance
- Poor key management can undermine otherwise strong encryption
- Limiting access reduces the number of accounts that could potentially expose sensitive information.
- Continuous monitoring helps ShopNow detect and investigate security incidents quickly.

b. What additional security measures will you introduce to minimise
breach risks?

5. Global Compliance Framework:
a. How will you align compliance practices across multiple regions while
addressing local laws?



b. What tools or technologies can help you monitor compliance
effectively?


#### Activity 3 


Scenario 1	- Consent and Data Deletion Requests
Tool: OneTrust	
Justification: The global retailer is struggling to process customer consent and fulfill data deletion requests under GDPR and CCPA. Customers frequently complain about delays in deleting their data and unclear communication regarding how their data is used. OneTrust is built to help with these issues for GDPR and CCPA, it has consent management and automated responses around data deletion.
<br>

Scenario 2 -Unauthorised Data Access
Tool:	SIEM Systems e.g Splunk	
Justification: Employees are already being flagged for not accessing but not clear if this is automatically or due to observations from other employees. This would have real-time monitoring to detect unauthorized access

<br>

Scenario 3 - Payment data unencrypted
Tool: KMS	
Failure Mode: Cardholder data stored without adequate encryption
Justification: KMS manages encryption keys used to protect sensitive payment information. This helps address the lack of encryption and supports PCI DSS requirements for protecting stored cardholder data.


<br>



Scenario 4 - No documentation of data flows
Tool: Collibra
Failure Mode: The organisation cannot clearly track where data comes from, where it goes or how it is used
Justification: Collibra provides data cataloguing and data-lineage capabilities, allowing the organisation to document and track how customer information moves between systems and third parties. This supports GDPR compliance.

<br>
Scenario 5 - Confidential IP shared outside the org
Tool: DLP
Failure Mode:Cofidential data shared outside the organisation 
Justification: . DLP can monitor data being transferred through email, cloud services and endpoints and block unauthorised transfers, reducing the risk of accidental or malicious data loss.

<br> 

Scenario 6 - Breach undetected for weeks
Tool: Secuirty awareness training platforms 
Failure Mode: weak breach monitoring protocols,
justification: prevents unauthorised access , data mishandling and educates staff


