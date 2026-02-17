
# 4.3 Designing secure architectures

Address (IP)
Port/Protocols (Http/ https)
Controls
Traffic controls (Firewalls)
Encryption

- Non web attack - attack doesn't use internet (IP, port) ,
- web based-  sql injection
  
Authenticate will check you are the right person, authorisation will be what your allowed to do

a honeypot is a tool of threat modelling, where it catches attackers.
Quite an expensive tool, honeypots are the tripwires that test the security blueprint is actually working. Honeypots provide tools and techquies that hackers are using right now. 

what does redundancy safeguard - availability of data and systems.
Redundancy is a core defence against DDos (Distributed denial of service ) attacks.
If an attacker tried to clog one with traffic , a new clean pathway can be created for secure users. 


Penetration testing is testing the vulnerabilities.

Always good to design system in layers, firewalls, passwords, etc
Good for debugging and also acts as a deterrent to attackers. 

### Economy of mechanism

Keeping mechanisms simple ('economical') 
what is the default if system fails - should be deny!
if system fails should be failed for everyone, should be denied


### Separation of Privilege

If we help each other with security we design a pattern together. 


### root / admin account
= all or nothing access
- any privileged action regards admin privileges
- most operating systems use a admin account


### Least common mechanism
- if you have a system component , then do not allow many users to share the system component
- the more used the component is, the higher the risk 


### Psychological acceptability
- how people perceive security 
- there should be ease of installation, in fear of people bypassing this due to difficulty
- avoids frustration and non compliance


### Anti Patterns
- one of the benefits include 'Hardcoded secrets'
- sometimes api keys are included in the code (that's an anti pattern as key easily obtained) 
