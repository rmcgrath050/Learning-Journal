
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

### HTTPS 

A secured protocol (Hypertext Transfer Protocol Secure)
- provides a encrypted transmission of data 
- encryption of data in the exchange between ssl client and ssl server 


### Downgrade Attacks
-- A channel not ungraded and not used - supposed to be removed, an attacker can take advantage
- VPS/VPN provides a secure exchange 
- Make sure to keep up to date with updates

<img width="778" height="536" alt="image" src="https://github.com/user-attachments/assets/7bd5d5ad-c68d-4d19-8fa8-158d005a5bc4" />

**Part of assignment will be designing a diagram , of pipeline , infrastucture etc. Please avoid AI to draw diagrams! Could fail for this!! 

Go though this lens:
1. on your job
2. Porject role
3. area of expertise
4. Stage of project design


<img width="592" height="632" alt="image" src="https://github.com/user-attachments/assets/c2c0871e-5363-46b1-a215-f7e9e94ab942" />

- why is there no firewall in public zone? Eaxmple assessement question, must be able to justify why? - can say as its public need everyone to have access here!
- DMZ , delimited zone!
- Lots of examples of UML diagrams/ networking diagrams on slides to consider for own design!
- Cna draw on draw.io, lucidchart, Dia, Microsoft Visio
- http://plantunml.com/ (Can design with tags and viarbles) I would recommend as includes data store icons, boxes to represent systems, see story below:
<br>
<br>
<img width="584" height="266" alt="image" src="https://github.com/user-attachments/assets/24e80d95-6250-49c8-888c-6a71b46e092c" />

chat access groups and service accounts and all that and not worry too much about all this!

  





