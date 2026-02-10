# 4.2 Cyber Secuirty Essentials

1. Threat: Any circumstance or event with the potential to cause harm to an information system.`For example, an email sent out by a cyber criminal

2. Asset: Anything valuable in your organisation or at home. It could be someone’s computer, or it could be your data.

3. Zero-Trust Approach: A security concept centred on the belief that organisations should not automatically trust anything inside or outside its perimeters and must verify anything trying to connect to its systems before granting access. (IT tickets, AD groups etc)

5. White Hat: Ethical hackers who use their skills to improve security by finding and fixing vulnerabilities.

### CIA Traid
The CIA triad is a model designed to guide policies for information security within an organisation. The triad stands for Confidentiality, Integrity, and Availability, as shown in the image below:

Knowledge of the CIA triad helps in designing comprehensive security strategies that protect sensitive information from various threats. Additionally, this understanding is crucial for your professional discussion in the End Point Assessment (EPA), <b>where demonstrating a deep awareness of security principles is essential!!</b>.

- Confidentiality: Ensuring that information is not accessed by unauthorised individuals.
- Integrity: Maintaining the accuracy and completeness of data.
- Availability: Ensuring that information is accessible to authorised users when needed, in a timely manner.

### AA Model
<br>
The AAA model is complementary to the CIA triad, and highlights the three key functions that need to be performed at all times in a secure system, these are:
- Authentication: Verifying the identity of users before granting access to systems.
- Authorisation: Determining the level of access or permissions a user has once authenticated.
- Accounting: Tracking and logging user activities within the system.
<br>

<img width="708" height="778" alt="image" src="https://github.com/user-attachments/assets/22791687-8d4d-4d35-80e9-bddb5fece7a5" />

Effective application of the CIA triad can significantly reduce the risk of data breaches and ensure compliance with regulatory requirements. It helps in building trust with stakeholders by safeguarding sensitive information.

#### Examples of implementing C, I and A include:

1. Confidentiality Measures: Encryption, access controls, and authentication protocols.

2. Integrity Measures: Checksums, hash functions, and version control systems.

3. Availability Measures: Redundancy, failover mechanisms, and regular backups.

<b>
Understanding how to apply these principles in real-world scenarios enhances your ability to design secure data products and infrastructures!! (EPA)
</b>
<br>
<br>
<b>A real-world example...</b> 
</br>

Implementing multi-factor authentication (MFA) for accessing sensitive data enhances confidentiality by ensuring that only authorised users can access the data.

Using version control systems like Git helps maintain the integrity of code and data by tracking changes and allowing rollbacks if necessary.

Employing redundancy and failover mechanisms ensures that critical systems remain available even during hardware failures or cyber-attacks.


### Multifactor Authenication
<br>
<img width="1184" height="950" alt="image" src="https://github.com/user-attachments/assets/33484403-b17a-4b95-983f-d821852af475" />


## 2. Vulnerabilities and risks

An outdated operating system, for instance, may have known weaknesses that attackers can exploit. For example, an organisation using an old version of Windows faces risks from unpatched vulnerabilities. Updating the operating system and applying security patches can mitigate these risks and strengthen overall security.
<br>

Identifying vulnerabilities, measuring risks and addressing them is crucial for maintaining robust security. Evaluating the probability of risks materialising is essential for effective risk management. Furthermore, addressing risks requires prioritisation, as different assets have different values, and understanding the value of each asset helps in understanding the severity of losing access to those assets. A proper understanding of risk also helps allocating your organisational resources more effectively to prevent potential security breaches and mitigate their impact.
<br>
Critical assets, such as sensitive customer data, intellectual property, and financial records, have high value and require stringent security measures.

<b>How do organisations protect sensitive customer data?</b>
<br>
Usually, organisations will use frameworks to proactively identify and address cybersecurity threats.
By systematically evaluating each potential hazard in terms of its severity, probability, and controllability, organisations can prioritise their cybersecurity efforts effectively. Specialised frameworks, like the one given in the chart below, help in documenting existing vulnerabilities, the efficacy of implemented controls, and the overall resilience of the organisation against cyber threats. Such a tool is invaluable not only for IT security teams but also for senior management to understand the cybersecurity posture of their organisation and make informed decisions regarding resource allocation and strategic security enhancements.



<img width="902" height="786" alt="image" src="https://github.com/user-attachments/assets/34e24df8-324c-473e-a2cb-1a80a932ad1e" />

- The organisation should assess the risk based on both the severity of the vulnerability and the value of the asset.
- While the vulnerability is high-risk, the value of the asset also plays a crucial role in risk prioritisation.


## 3. Understanding threats and attacks

By understanding the nature of these dangers, we can develop robust defence mechanisms to protect our data and infrastructure.
An attack is an intentional act by a malicious actor to exploit a vulnerability.
 Being aware of common attack vectors enhances your ability to protect data products and infrastructures. Additionally, it prepares you for discussing these topics in your <b>EPA professional discussion!! <b/>

### Threats
- Malware: Malicious software designed to damage or disrupt systems, steal data, or perform other unwanted actions. Types of malware include viruses, worms, and spyware. Example: A piece of malware might be downloaded unknowingly from an email attachment, which then spreads through the network, stealing sensitive data.
- Phishing: A tactic used to trick individuals into divulging confidential information by pretending to be a trustworthy entity in electronic communications. Example: An email that appears to be from a bank, asking the recipient to click on a link and enter their login credentials. The link leads to a fake website controlled by attackers.
- Insider Threats: Risks posed by individuals within the organisation who have access to sensitive information and misuse it. Example: A disgruntled employee who leaks confidential data to a competitor.
- Social Engineering: Manipulating people into breaking normal security procedures and divulging confidential information. Example: An attacker calls an employee pretending to be from IT support and convinces them to reveal their password.

<br>
A phishing attack may trick employees into divulging sensitive information. Implementing email filtering and user training can reduce the risk of such attacks. For instance, a company might face a phishing threat where attackers send emails pretending to be from a trusted source. 

<br>
Spearphishing is a more targeted form of phishing, where attackers tailor their messages to specific individuals or organisations, often using personal information to make the attack more convincing.

<b>A real life example:</b>
- The attackers gained access through a third-party HVAC vendor, highlighting how insider threats and social engineering can be exploited to breach large networks.
- In fact, there are several types of threat actors you should be aware of, including Hacktivists, Rogue State Actors, Script Kiddies, and Common Hackers
