
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


<br>


Bottlenecks can appear at any stage in the pipeline:
- Data Ingestion: API rate limits or slow file parsing.
- Transformation: Poorly optimised joins, sorting, or aggregations.
- Storage: Slow reads/writes to the database.
- Output: Heavy dashboards or inefficient visualisation queries.


Use profiling tools or logging (e.g., Spark UI, SQL query plans, resource monitors) to trace delays. Focus your investigation on the slowest part of the pipeline - fixing that can lead to big performance gains.
EG. In one customer pipeline, 80% of processing time was spent enriching customer records via complex joins. A simple indexing strategy reduced processing time by half.

<br>

### Tunning for Performance:
- Parallelisation : Break tasks into smaller pieces that run in parallel
- Caching: Save repeated computations, especially for static reference data. - check does GCP have this?
- Query optimisation : Use indexes, avoid full-table scans, simplify joins.
- Vertical scaling: Give more CPU/memory to key components
- Horizontal scaling: Add more nodes or workers


#### Keep Monitoring
Example: A real-time recommendation engine monitored latency and throughput over time, adjusting scaling rules automatically when user spikes occurred during peak traffic.
Use continuous monitoring tools (e.g., Prometheus, Grafana, CloudWatch) to set alerts and track trends over time.

- Throughput - Volume of data handled over time
- Latency - Processing delays in the pipeline
- Error rate - Points of failue under load
- CPU Usage - System strain or inefficiencies


## L3: Lesson 3: Deployment Strategies for Data Pipelines

Deployments can be risky. A new feature or change to a data pipeline might seem small, but a single misstep could result in broken dashboards, delayed reports, or even data loss. 

- Blue / Green deployment :  When the green environment is ready, traffic is simply switched over. If something goes wrong, teams can easily switch back to blue

(Maybe this is what the develop branch is about in Jenkins??! )
- In the initial setup, both Blue and Green environments are complete and independent. Each includes application servers, services, and a database. Blue Environment is the live, user-facing version. Green Environment mirrors the blue environment and is ready to be updated for the next release.

<br>
This staging model allows internal teams to verify:
- Functionality
- Performance
- Integration with shared resources

<br> 

- Rollback is faster and safer in the short term.
- Roll-forward is useful when rollback isn’t possible (e.g. irreversible database changes)


### Deployment automation tools
 - Github actions
 - SSH

## Lesson 4: Automating Deployments and Managing Risk

- Docker: Package pipeline components in isolated environments to run consistently anywhere
- Infrastructure as code: Version-control your environments, not just your code
- CI/CD Orchestration : Trigger tests, builds, and deployments automatically on code events.

<i> Case Study: A team managing data pipelines for daily retail pricing used Docker containers to version their transformation logic, and GitHub Actions to deploy to a Kubernetes cluster on merge </i> 

##### Safeguards and quality gates:
- schema validation: insures structure of incoming/ transformed data has not changed
- Test coverage checks : require 90% coverage for all new pipeline functions
- Performance thresholds: processing must remain under 10 mins or below 80% memory usage
  
##### Monitoring and alerting :
- pipeline health dashboards (job fails, success, runtimes. delays)
- data quality metrics (null values , dups, row counts, freshness)
- System metrics : CPU/memory usage . disk I/O , queue dept

<i>Tooling Suggestion: Combine Prometheus or CloudWatch with Grafana dashboards and Slack alerts for live notifications. </i>
<br>

#### Operational Risk:

Risk isn’t just technical - it’s operational. Effective teams prepare for failure with structure! 
- Blameless post analysis:  learn from failures update process!
- Stakeholder coordination
- Scheduled releases: Avoid deploying during high risk business hours
- Deployment playbook - clear steps for deploying verifying and rolling back


By combing tools such as docker and github actions with quality gate alerting and team protcols, deployments become fast repeatable and safe! 


## Summary 
- UAT Testing ensures pipeline has useful actionable outputs and align with business workflows
- Stress / load testing helps identify how system behaves under pressure
- Deployment strategies such as blue green / canary rollouts reduce risk by isolating releases and allowing safe rollback
- Automation tools such as GitHub Actions, Ansible, and CI/CD pipelines make deployments faster, more consistent, and less error-prone
- Quality gates and monitoring enforce standards and alert teams to problems before they impact users - key for production-grade systems.
- Operational risk management (clear communication, fallback planning, and structured releases) ensures data engineers work in sync with the broader business





