
## Ethical Foundation in DE

1. Fairness = non biased data
2. Accountability = Accountable for what system does, leads to trust in company 
3. Transparency 

<br>
<img width="1816" height="860" alt="image" src="https://github.com/user-attachments/assets/9e8348b4-67eb-4728-a1ad-8b1fa7d62603" />
<br>

Examples of Anonymisation
1. data masking in snowflake
2. in SQL we just have a proc to replace text with ######## and default dates to 1/1/1900


We dont anonymise data but we do restrict access using agent roles. Tools can be used: (Typically recognised Cols that are PII) 
- ARX : Risk analysis and data masking
- Synthea
- Microsoft Presidio


#### Activity 1 : 

1 . The ethical principle are : Transparency , Privacy , consent , Accountabilty, fairness and Data minimisation
1. What ethical principles (e.g., transparency, privacy, accountability) are relevant in this scenario?

<br>

Transparency
- Customers should have been aware what's being collected, how it's being used and who it's being shared with
<br>

Privacy
- Private activities like holiday planning were used in advertising, raising privacy concerns
- Company expanded into collecting third-party personal data without informing users or obtaining consent.
<br>

Accountability
- Regular audits should be conducted to identify privacy risks
<br>

Fairness
- Third party data may introduce bais that affect product recommendations
<br>

Data minimisation
- Gathering excessive information, such as detailed location history or unrelated social media activity, violates the principle of collecting only what is needed
<br> 

<br>


<b>2. How should the company address concerns about the use of third-party data?</b>
- Increase transparency
- Obtain consent
- Limit data collection
- Clearly informing customers about all sources of data used.
- Updating privacy notices to explain how personal and third-party data is processed.
= Obtaining explicit consent before using third-party data for personalisation.
- Giving customers the ability to opt in or opt out of personalised advertising.
- Conducting a Data Protection Impact Assessment (DPIA) to identify privacy risks.
- Working with legal, compliance and data governance teams to ensure GDPR requirements are met.
- Responding publicly to customer concerns and demonstrating a commitment to ethical data practices.

<br>

<b>3. What actions would align with ethical best practices in data engineering?</b>
- Build Privacy by Design into systems from the start.
- Collect only the data needed (data minimisation).
- Obtain clear consent and be transparent about data use.
- Protect personal data with strong security and access controls.
- Regularly audit data processing and AI systems for compliance and fairness.
- Ensure data use complies with GDPR and ethical standards.



#### Activity 2:

Questions to Guide Your Discussion 
1. What are the benefits of implementing this innovative system for the company, customers, and the environment? 
2. What ethical concerns arise from the collection and use of detailed driver behaviour data? 
3. How could the company balance innovation with ethical responsibilities? Debate Guidelines 


1. Benefits of implementing this innovative system
- Contribute to Company - improved operational efficiency: AI analyses real-time traffic and vehicle data to optimise delivery routes, reducing travel time.
- Customer - faster delivery time and greater reliability
- Environment - Reduced fuel consumption and less fuel used therefore reducing greenhouse gas emissions. Sustainability benefits both the company and society by reducing environmental impact.



2.Emphasise the importance of employee privacy, transparency, and creating a positive work culture. Discuss the potential risks of excessive data collection and its misuse.

Continuous monitoring may invade privacy.
- Lack of transparency can reduce trust.
- Data could be misused for disciplinary action or redundancies.
- Excessive surveillance may create a stressful work environment.
- Employees deserve control and clarity over how their personal data is used.

<br> 

3. How could the company balance innovation with ethical responsibilities? 
- Using Data Fairly - only use driver data for coaching and training purposes not disciplinary or employment decisions, only using data for development not punishment 
- Human oversight , managers can review recommendations before taking action
- Transparency - what data is collected, why, how it benefits drivers/ business and who can access it
- Limit Data Collection - collect only what is needed for improving safetly and operational efficiency
- Establish Governance control - comply with GDPR
