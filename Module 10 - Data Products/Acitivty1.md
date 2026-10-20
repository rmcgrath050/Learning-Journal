
#### Task 1

Financial Risk Reduction

Business objective: Minimise credit risk in loan approvals and reduce the loan default rate by automating customer risk profiling during onboarding.
product features to support: 

* automated credit risk scoring which uses a variety of data sources to generate a risk score for each applicant
* use an API to provide real time credit file information
* use historical data to predict future risk of default based on lending and repayment patterns
* flag high risk customers for a human review
* dashboard showing credit risk analysts a whole picture of key risk elements such as history of missed payments, defaults, DTI (debt to income) ratio and any recommended actions during the review
* Income and Employment Verification – Analyse employment status, income level, and income stability to assess a customer’s ability to repay the loan.

#### Task 2

Step 1: Understand the matrix
You need to plot each feature on a matrix using two questions:
* Business Impact: How much will this feature help reduce loan defaults and improve lending decisions?  
* Implementation Feasibility: How easy and realistic is it to build the feature with the time, budget, and data available?


1. Which design choice had the most impact on scalability?
The most impactful design choice was using a modular and automated data pipeline. This allows the system to process increasing amounts of customer data without redesigning the entire system. New features, such as AI-powered risk scoring, can also be added as the fintech startup grows

3. What resilience strategy was most important for your pipeline?
The most important strategy was error handling and automatic retries. If a data source becomes temporarily unavailable or a processing step fails, the pipeline can retry the operation instead of stopping completely. Data validation and monitoring also help identify errors and maintain data quality

5. How did this review influence your design thinking?
The review helped me understand the importance of balancing scalability, reliability, cost and implementation time. I realised that a good design should not only meet current business needs but also support future growth. I would prioritise essential features first, ensure the pipeline handles failures effectively, and design the system so that new features can be added easily


Template 1: Architecture Design Canvas
Instructions: Use this template to sketch your scalable data pipeline. You may recreate
this layout on a whiteboard or use a digital canvas.
Pipeline Layers
1. Data Ingestion Layer
a. Sources (e.g., APIs, databases, sensors):
b. Batch or streaming:
2. Processing Layer
a. ETL tools / frameworks:
b. Is distributed processing applied? (Yes/No):
c. Real-time or scheduled jobs:
3. Storage Layer
a. Type (e.g., data lake, warehouse, NoSQL):
b. Partitioning or indexing strategies:
4. Delivery Layer
a. Access method (e.g., dashboards, APIs):
b. Frequency of updates:
Scalability Features Included
 Load balancing
 Caching
 Horizontal scaling
 Distributed processing


#### Activity 3

