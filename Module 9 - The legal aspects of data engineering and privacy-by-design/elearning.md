
# Legal aspects of data engineering and privacy-by-design

## L1. Data engineering and data protection laws

Data protection laws like General Data Protection Regulation (GDPR) and the Data Protection Act (DPA) exist to ensure organisations handle personal data responsibly

The focus here is on how these laws apply to data engineering practices, ensuring compliance and protecting user privacy. To begin, let's explore the core principles of GDPR.

<img width="1878" height="1156" alt="image" src="https://github.com/user-attachments/assets/24b8c330-0f28-42a4-9609-51f88b78a642" />
<br>

Example of breach of customer details getting exposed:
- The breach violated several GDPR principles, including security (lack of encryption), transparency (customers weren’t informed immediately), and minimisation (excessive details stored).

- Lawfulness, fairness and transpaarency : People must know what data is collected, why, and how.
- Purpose limitation : Data collected for one reason should not be used for unrelated purposes without additional consent.
- Data minimisation : anisations must only collect the data they need to achieve specific purposes.
- Storage limitation : Data should not be retained longer than necessary
- Security (Integrity and confidentiality) : Organisations must ensure data is secure against breaches and misuse.


## L2. Legal obligations for data engineers

Soultions included:
- Implemented a centralised data access system, ensuring all users required multi-factor authentication to view patient records.
- Migrated legacy systems to encrypted cloud storage with automated logging features.
- Conducted compliance training sessions for all hospital staff, focusing on the importance of secure system design and documentation.

#### Obligation 1: Secure system design

- Secure system design involves encryption, user authentication, and controlled access.
- Engineers use encryption protocols like SSL/TLS for data transfer, ensuring that sensitive information like test results cannot be intercepted.

#### Obligation 2: Documentation and accountability

- Documentation includes maintaining logs of data access, processing activities, and breach reports.
- This ensures accountability, as organisations can track who accessed patient records, when, and for what purpose.

#### Obligation 3: Stakeholder communication

- Data engineers must clearly communicate compliance measures and security protocols to stakeholders.
- This might involve employee training sessions, policy updates, or breach notifications.

## L3 . The consequences of non-compliance with data protection

So what are the consequences for non compliance with data protection laws?

#### Consequence 1: Financial penalties
Non-compliance often results in severe financial penalties, which can cripple organisations, especially smaller entities.

#### Consequence 2: Reputational damage
Data breaches harm an organisation's reputation, leading to loss of trust among customers, partners, and stakeholders. This can lead to customer attrition, reduced sales, and difficulty in attracting new clients.

#### Consequence 3: Operational disruption

Non-compliance can lead to investigations, audits, and the need to overhaul processes and systems.
This diverts resources from normal operations and increases downtime.


## L4. Understanding privacy-by-design

Privacy-by-design ensures that these systems are created with robust privacy protections from the outset, fostering customer trust and compliance with data protection laws.

#### Core principle 1: Proactive, not reactive

Privacy-by-design focuses on identifying and addressing risks during development rather than reacting to breaches after they occur.Online retailers anticipate potential risks, such as fraudulent access to payment systems, and implement safeguards like tokenised payment methods.

#### Core Principle 2 : Privacy embedded into design

Retailers design systems with privacy defaults, such as anonymising customer data during analytics.

#### Core Principle 3 : End to End secuirty

Retailers secure customer data using encryption for transactions, access controls for databases, and secure deletion methods for outdated information.

#### Technical and security infrastructure

<br>
<br>

<img width="1074" height="682" alt="image" src="https://github.com/user-attachments/assets/b5f64d2e-58d2-4edb-a58e-65d7c20de11a" />

<br>
<br>

- Hosting : The hosting and e-commerce platform (website) is fully managed and maintained by an outsourced company called PCIData Hosting.
- Secuirty Measures : A firewall is deployed between the Internet and the AutoRental website. The AutoRental website is housed within an AutoRental demilitarized zone (DMZ) with a Microsoft SQL Server 2015 server housed within an AutoRental internal zone.
- Techinal specs : The website is running on a Windows 2012 Server, using Microsoft Internet Information Services (IIS) and Microsoft ASP (Active Server Pages). The AutoRental DMZ and internal zone are both isolated networks for just AutoRental’s use.
- Payment page generation : All cardholder data (CHD) is entered into the payment form, which is built by the website using the PSP’s JavaScript payment form.
- Data handling : With the JavaScript payment form, the AutoRental website is responsible for building the payment page, albeit with JavaScript code downloaded from the PSP.

## L5. Techniques for embedding privacy into data systems  

### Privacy integration in banking platforms

- Integrated role-based access control (RBAC) to limit data exposure based on job responsibilities.
- Used end-to-end encryption for all customer data in the mobile banking app.
- Applied pseudonymisation techniques for analytics, replacing identifiable customer information with anonymous IDs.




