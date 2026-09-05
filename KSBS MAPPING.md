# KSBS

##### Links :
https://skillsengland.education.gov.uk/apprenticeship-standards/st1386?view=standard
https://skillsengland.education.gov.uk/apprenticeship-standards/st1386 - click on EPA plan 


## Project KSBS

#### K8: Deployment approaches for new data pipelines and automated processes.
I applied progressive deployment techniques when migrating the reporting tasks to the new LPI server. I initially used a canary-style approach by testing one report, then a controlled group of 10 reports, before progressively migrating the remaining tasks in batches. I validated task status, expected outputs and file delivery at each stage using SQL and Excel, with LPI/Kydrall stakeholders supporting the validation in Pre-Prod. I then implemented a parallel/blue-green approach by creating new tasks with the same dependencies as the existing tasks and configuring them to use the new LPI location. This allowed the existing and new processes to run in parallel and provided a controlled way to validate the new configuration before changing the original tasks to the new location.

#### S26: Identify data quality metrics and track them to ensure the quality, accuracy and reliability of the data product.
I established a baseline of the number of tasks sending files to the existing LPI CDN location and used this as a validation metric when configuring the new server. I then compared the results after the change to ensure that the expected tasks continued to run and that the correct files were being generated and transferred. Investigating discrepancies/issues via comparing list sent from LPI and there was 2 reports not accounted for - two turned out to be old reports that have been made redundant (raised to manager and this got added as a later cleanup task for team )


## Assessment KSBS







