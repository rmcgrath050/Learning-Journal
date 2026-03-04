

Agenda today:
- Should be able to explain secuirty policies over data systems and their practical use
- DescribinG comon cyber incidents and how they occur
- How to apply risk migatation strageties
- Responding to secuirty incidents professionally
- Trying to describe downtime from operational perspective , eg finanical impact downtime can cause
- important that there is policies to instruct how we should respond to particular incidents


As looking after a server we have a policy where we review everyone's access to the server. and if they no longer require access they are removed

### CSO server
So I have HC data on my server, and we need to have a register to specify how much data we have, 
how many customers will be impacted if there is a data breach, how much $ damage there would be, 
who we need to notify (depending on how much HC data is breached) - e.g local news, national news, FCA etc..



Downtime can have financial impact and market downtime affects share price too? 
Regulatory downtime also to consider! Especially with data breach with FCA
Downtime can also affect public repetition 


#### risk mitigation
-Reducing the likelihood
-Reducing the impact
-Reducing exposure time

####  Data Classification policy
Encryption policy
Backup & Recovery policy
Mobile/BYOD policy
Patching and Vulnerability policy


What is an incident - An unplanned event that disrupts or reduces quality of service

CIA - Confidential , integrity and availability 
**Make sure to know difference between different types of attacks 
How can malicious code attack integrity 

malicious code can run a script in background to open back door for attackers
unauthorised access-  someone else's login, attack could include a insider! 
IT access -redirecting traffic using another port  - creates a small network ( eg playing restricted game though another port) 

Financial gain- access to data 
Aggressive probe - constant knocking


#### Incident response 

Start Prep of incident :
from what type of incident - identification
Does the policy exist for this  - if not we can create one! 

Pipeline - server logs, CI/CD logs, logging failures etc login in attempted
Ask to see log - and analyse this to create an incident

3. Containment - isolate affected system, deauthorise the affected account , 
4. Lessons learned - document everything done, improve education of staff 

<br>

Class exercise: 
1. what incident was this? Priority 1 incident 
2. How was the incident identified - Helpdesk log incident documentation
3. How was the incident escalated - security manager 
4. What are the technical investigation done - web server restored from backup, log examined and VPN account identified 
5. What was the root cause - internal employee noted a vulnerability and misused it 
6. Was the solution a remediation or mitigation? remediation 



Mitigation reduces impact, remediation fixes the source
Or 
mitigation = rules put in place to stop something happening. Remediation = actions to put things right when something happens / removing malware etc



### Non repudiation 

- providing an excuse for an action happening 
- a service that provides undeniable proof of origin and integrity of data


Polices include:
- software access
- non external email access
- monitor polices 
- need to know where to access polices! - Area to explore 


### Security Policy (which security are talking about) 
- secure storage
- internal security 
- application security
- access management 
- network security 




Storing sensitive data in secure network areas with specific named access.
- Dev/test/prod server structure so any changes to data are fully tested before going into the wild.
- Phased Migration Strategy - Migrating data in smaller logical chucks , so reduces the affected radius if a failure occurs 

<br>

Identify and access management policy - Assigning permissions based on job junctions (Eg data engineer, analyst etc) 
- Network Security policies eg. Isolating migration environments using Virtual private clouds and firewalls 
- General security policies such as email, internet usage etc…






