# Project planning

Word count: up to 500 words (+/- 10%)

For this assessment you are required to write an individual project proposal for a
substantial data engineering project that you will undertake during your
apprenticeship. The project must be based on a real business need within your
organisation and should describe a piece of work that delivers a clear business
benefit, typically undertaken on your employer’s premises and completed pregateway.
Your proposal must outline a project that will allow you to demonstrate the
Knowledge, Skills and Behaviours (KSBs) from the Level 5 Data Engineer Standard
listed later in this document.

Your task is to produce a concise written proposal of no more than 500 words that
could be presented to both your line manager and training provider. It should be
written in clear, professional language that would be understandable to both
technical and non-technical stakeholders.
Within your proposal, you must:

<i>
• Describe the business context, including the problem or opportunity your project will address.
• Set out the project objectives, expected business benefits and how success will be measured.
• Summarise the data and technologies you expect to use (for example, data sources, storage, processing, and any analytics or reporting).
• Outline the scope of work, including key activities you will undertake and the main deliverables you intend to produce.
• Identify key stakeholders and how you will engage with them throughout the
project.
• Highlight any known risks, assumptions or constraints that may affect delivery.
Crucially, your proposal must also explain why this project is a good fit for
demonstrating the KSBs listed in the appendix. You should briefly indicate how the
planned work will enable you to show:
• application of core data engineering knowledge.
• practical data engineering skills across the project lifecycle.
• professional behaviours in a real organisational setting.
</i>


### My notes

Project title: Modernising a Legacy Excel Reporting Process Through Automated Data Pipelines in Google Cloud Platform

The business problem is we receive third party dataset which helps us analyse last branches in town which has usually been achieved though excel marcos by report owners. This report however has started to load into the GCP FDP and reporting owners are now wanting to create a automated report from this. The project will reduce manual effort, improve data quality and enable report owners to access up to date information without relying on complex Excel macros.

#### The project objectives include:
- Design and build an automated pipeline within GCP
- Replace the existing macro process with a cloud based solution
- Reduce manual processing time for report owners
- Improve data quality though automated validation
- Ensure a solution that is scalable and maintainable for future enhancements

<br>
Expected Business Benefits includes: 
- Reduced manual effort.
- Faster report production.
- Improved consistency and accuracy.
- Better governance through centralised cloud based data processing.

Success will be measured by:
- Elimination or significant reduction of manual Excel processing.
- Accurate matching of outputs between the new cloud report and the existing report.
- Positive feedback from reporting stakeholders.
- Successful deployment into the production environment.

#### Data and technologies being used: 
- DataSources include third party branch metrics dataset via CACI fed into an ODP and the existing Excel report to use for validation.
- Using BigQuery to test SQL result and use it to store the transformed data
- For data processing/ transformation using SQL, DBT (Data Build Tool) to develop models with business logic and Python for scripting/automation 
- Apache airflow via Cloud composer to create/schedule DAGS that run the data pipeline
- Cloud Composer manages the orchestration environment, enabling reliable scheduling, monitoring and execution of workflows.
- Terraform to manage and provision cloud infrastuture using iaC
- Github for version control, code reviews and collaboration
- Jenkins and Harness for CI/CD automating rh build, testing and deployment of the data pipeline 
- Jira/ mims for managing user stories, tracking progress and providing test evidence




#### Scope of work

The project will include:

Discovery
- Understand the existing Excel macro process
- Review reporting requirements with report owners
- Analyse source datasets

Design
- Design the target data model
- Design transformation logic
- Define data quality checks

Development
- Build automated data pipeline in GCP
- Develop SQL transformations
- Configure scheduling and automation
- Implement validation checks


Testing
- Compare outputs against the legacy Excel report.
- Conduct User Acceptance Testing (UAT).


Deployment
- Deploy pipeline into production.
- Support transition to business users.
- Produce documentation and handover materials.

Deliverables
- Automated GCP data pipeline
- SQL transformation script
- Reporting ready dataset
- Data validation and technical documentation
- User handover documentation


#### Stakeholders
- Report owners who will define reporting requirements and validate outputs, engagement via regular meeting and team chats 
- Data engineering team , to ensure standardisation is being meet, offer technical guidance and code reviews, and engagement via daily stand ups 
- Platform teams who own the ODP , to engage with them to access the data and understand the ODP and raise any data issues 
- The business users who will be using the report and feedback during testing


#### Risks, Assumptions and Constraints

Risks
- Changes to the third party data structure
- Differences between Excel calculations and SQL logic
- Data quality issues within source files
- Delays in stakeholder availability for testing

Assumptions
- Required data remains available within GCP 
- Existing business logic is fully understood
- Required access to GCP environments is provided

Constraints
- Project timescales.
- Compliance with organisational data governance standards.
- Dependency on upstream data availability.
- must integrate with the organisation's existing GCP environment and follow established technical standards and deployment processes
- Access permissions, development is dependent on access to GCP environments, repositories and datasets



******************************************

Reporting and Validation
* BigQuery reporting datasets.
* Comparison of outputs against the legacy Excel report to ensure consistency and accuracy.



Summarise the data and technologies you expect to use (for example, data sources, storage, processing, and any analytics or reporting).
- 


You may do this through a short narrative paragraph or by briefly referencing specific
KSB codes within your description.
Your proposal will be assessed on how clearly and realistically it defines the project,
the strength of the business rationale, and the extent to which it demonstrates that
the project provides appropriate opportunities to evidence the required KSBs.
KSBs
These are the KSBs you will be focusing on as part of this assessment.
KSB Descriptor
 - K2 Methodologies for moving data from one system to another for storage
and further handling.

- K4 Frameworks for data quality, covering dimensions such as accuracy,
completeness, consistency, timeliness, and accessibility.

- K6 Software development principles for data products, including
debugging, version control, and testing.

- K7 Principles of sustainable data products and organisational
responsibilities for environmental social governance.

- K8 Deployment approaches for new data pipelines and automated
processes.

- K9 How to build a data product that complies with regulatory requirements.

- K12 How to cost and build a system whilst ensuring that organisational
strategies for sustainable, net zero technologies are considered.

- K13 The implications of financial, strategic and compliance regarding to
security, scalability, compliance and cost of local, remote or distributed
solutions.

- K14 The uses of on-demand Cloud computing platform(s) in a public or
private environment such as Amazon AWS, Google Cloud, Hadoop,
IBM Cloud, Salesforce and Microsoft Azure.

- K15 Data warehousing principles, including techniques such as star
schemas, data lakes, and data marts.

- K17 Approaches to data integration and how combining disparate data
sources delivers value to an organisation.
K19 Differences between structured, semi-structured, and unstructured
data.

- K20 Types and uses of data engineering tools and applications in own
organisation.

- K24 Processes for evaluating prototypes and taking them to implementation
within a production environment.

- K25 The lifecycle of implementing data solutions in a business, from
scoping, though prototyping, development, production, and continuous
improvement.

- K26 Data development frameworks and approved organisational
architectures.

- K30 The methods and techniques used to communicate messages to meet
the needs of the audience.


KSB Descriptor
- S1 Collate, evaluate and refine user requirements to design the data
product.

- S2 Collate, evaluate and refine business requirements including cost,
resourcing, and accessibility to design the data product.

- S3 Design a data product to serve multiple needs and with scalability,
efficiency, and security in mind.

- S4 Automate data pipelines such as batch, real-time, on demand and
other processes using programming languages and data integration
platforms with graphical user interfaces.

- S5 Produce and maintain technical documentation explaining the data
product, that meets organisational, technical and non-technical user
requirements, retaining critical information.

- S6 Systematically clean, validate, and describe data at all stages of
extract, transform, load (ETL).

- S9 Query and manipulate data using tools and programming such as SQL
and Python. Manage database access, and implement automated
validation checks.

- S16 Develop algorithms and processes to extract structured data from
unstructured sources.

- S22 Develop, maintain collaborative relationships using adaptive business
methodology with stakeholders such as, business users, data
scientists, data analysts and business intelligence teams.

- S23 Present, communicate, and disseminate messages about the data
product, tailoring the message and medium to the needs of the
audience.

- S24 Evaluate the strengths and weaknesses of prototype data products and
how these integrate within an organisation’s overarching data
infrastructure.

- S26 Identify data quality metrics and track them to ensure the quality,
accuracy and reliability of the data product.

- S27 Selects and apply sustainable solutions to contribute to net zero and
environmental strategies across the various stages of product and
service delivery.

- B1 Acts proactively and takes accountability adapting positively to
changing work priorities, ensuring deadlines are met.

- B2 Works collaboratively with stakeholders and colleagues, developing
strong working relationships to achieve common goals. Support an
inclusive culture and treat technical and non- technical colleagues and
stakeholders with respect.
