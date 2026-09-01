
# L5DE 10.1 - Advanced Testing and Deployment Strategies

User Acceptance Testing is the final verification step before a data pipeline is declared “production ready.” It answers a crucial question: does the output meet the expectations and day-to-day needs of business users? While functional testing proves the pipeline behaves as intended from a technical perspective, UAT determines if that functionality translates into real-world value

<br>
Requirements might include 
- Data accuracy 
- Output timeliness
- Business rule application

<br>

Good UAT scenarios should include:
- Normal operations
- Peak use periods
- Edge cases

<br>
Validating user experiences: 
- Are labels for columns clear?
- Navigation , is data easy to find?
- Can user extract data for their use?  eg Excel
- Performance - can reports get generated without lag? 

- Consider running a brief usability survey alongside UAT. Ask users to rate ease-of-use, clarity, and confidence in the data!!


#### Setting Acceptance Criteria 

Examples include: 
- “Pipeline must process 95% of incoming data within 15 minutes of arrival”
- “Dashboard should display latest data without requiring a manual refresh”
- “Exported reports must contain all fields specified in the agreed template”

It’s best to write these in collaboration with stakeholders and document them in a shared UAT plan or spreadsheet. This ensures mutual understanding and creates a paper trail for auditing.
- Don’t forget non-functional requirements: uptime, user concurrency, supported browsers, etc. These are just as important for acceptance.


## L2: Lesson 2: Stress Testing and Performance Tuning

Objectives:
- Differentiate between load testing and stress testing in data pipelines
- Interpret performance metrics to identify system bottlenecks.
- Apply performance tuning techniques to optimise pipeline throughput and efficiency


- Load Testing checks how the system handles expected conditions. For example, simulating the average daily volume of data processed or the number of concurrent users accessing a dashboard
- Stress Testing goes beyond expectations, deliberately overwhelming the system to discover breaking points, recovery behaviour, and weak spots in infrastructure
- Tip: Use both tests together - one validates reliability, the other prepares you for chaos!!


<br>
<img width="858" height="742" alt="image" src="https://github.com/user-attachments/assets/6838bdf9-ea13-4f8e-bb0c-63f5b029e97b" />


  
- 
