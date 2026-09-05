# KSBS

##### Links :
https://skillsengland.education.gov.uk/apprenticeship-standards/st1386?view=standard
https://skillsengland.education.gov.uk/apprenticeship-standards/st1386 - click on EPA plan 


## Project KSBS

#### K8: Deployment approaches for new data pipelines and automated processes.
I applied progressive deployment techniques when migrating the reporting tasks to the new LPI server. I initially used a canary-style approach by testing one report, then a controlled group of 10 reports, before progressively migrating the remaining tasks in batches. I validated task status, expected outputs and file delivery at each stage using SQL and Excel, with LPI/Kydrall stakeholders supporting the validation in Pre-Prod. I then implemented a parallel/blue-green approach by creating new tasks with the same dependencies as the existing tasks and configuring them to use the new LPI location. This allowed the existing and new processes to run in parallel and provided a controlled way to validate the new configuration before changing the original tasks to the new location.

#### S26: Identify data quality metrics and track them to ensure the quality, accuracy and reliability of the data product.
I established a baseline of the number of tasks sending files to the existing LPI CDN location and used this as a validation metric when configuring the new server. I then compared the results after the change to ensure that the expected tasks continued to run and that the correct files were being generated and transferred. Investigating discrepancies/issues via comparing list sent from LPI and there was 2 reports not accounted for - two turned out to be old reports that have been made redundant (raised to manager and this got added as a later cleanup task for team )


## Professional Discussion KSBS


#### S19 Identify and escalate risks with suggested mitigation/resolutions as appropriate.

During the LPI server migration, the LPI engineer initially proposed testing against their Production environment. I reviewed the proposed setup and identified that, because of the domain and access requirements, this would mean our Production server would effectively be involved in the testing. I considered this an unnecessary operational risk because we were testing a new configuration that hadn't yet been fully validated. I raised this concern with the relevant stakeholders and pushed back on using Production for the initial testing. I proposed that a Pre-Production environment should be made available instead. This provided a controlled environment where we could validate the new LPI location and file transfers before making changes to the Production tasks. Once the testing was successful, we could then proceed with the Production migration with much lower risk. 

The risk was that an incorrectly configured task or file destination could affect live reporting/file transfers, and because the new configuration had not been validated, troubleshooting it directly in Production could cause disruption. Also harder to debug on production due to more operational tasks and therefore would also create an incident involving more operational support. 





#### Need to place somewhere: 
Question → technical action → reason → validation → outcome

"For my SQL Server reporting migration, I first established a baseline of how many tasks were sending files to the LPI location. I used SQL validation queries to check task status and counts. I then tested one task initially, followed by a group of 10 and then the remaining tasks in controlled batches. I compared the expected and actual results in Excel and worked with the LPI stakeholder and Kydrall to confirm that the expected files were being received in Pre-Prod'

"Why did you use SQL?" 
I used SQL validation queries to establish a baseline of the existing tasks and confirm that I had identified and matched all the necessary tasks in the SQL database. I also used SQL to check the status of the tasks after the changes, which allowed me to validate that the migration hadn't missed any tasks or affected their expected operation

"How did you make sure you didn't introduce duplicates?
I used a SQL MERGE statement to control how the new tasks were inserted. I used a join condition of 1 = 0 so that the existing task records could not match the new records, meaning the operation would insert the required new tasks rather than unintentionally update or duplicate existing records. I then validated the resulting task set using SQL to make sure the expected tasks were present


"Why did you test in batches?" 
I tested in batches to reduce the risk of moving all of the reporting tasks to the new LPI location at once. I initially tested a single report, then increased this to 10 and subsequently migrated the remaining tasks in controlled groups. At each stage I could validate the task status and expected file output and confirm with the LPI stakeholder and Kydrall that the files were being received correctly in Pre-Prod. This gave me confidence that the new location was working as expected before increasing the scope of the migration."


During the LPI server migration, an LPI engineer initially wanted us to carry out testing against their Production environment. I investigated the implications of the required domain access and identified that this would effectively result in our Production server being involved in the testing. I considered this an unnecessary operational risk because the new configuration had not yet been fully validated. I therefore pushed back on the proposed approach and requested that a Pre-Production environment was made available for testing first. This allowed us to validate the new LPI location and file transfers in a controlled environment before making changes to Production


Risks:
- An incorrectly configured task could have affected live processing.
- Files could have been sent to the wrong location.
- Production data/processes could potentially have been disrupted.
- Troubleshooting a new configuration in Production would increase operational risk.
- It would be harder to distinguish migration issues from existing production issues.

1. Risk identification
LPI proposed Production testing → you identified the risk.

2. Stakeholder challenge
You pushed back and requested Pre-Prod.

3. Controlled testing
Tested 1 → 10 → batches.

4. Technical validation
SQL checks, task status, counts, Excel comparisons.

5. Deployment approach
Canary-style progressive testing + parallel/blue-green principles.

6. Safe migration
Only changed the original tasks to the new LPI location after validation.





