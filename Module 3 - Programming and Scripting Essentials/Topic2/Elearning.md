# 3.2 DevOps : Version Control for Data engineers

##Introduction 

We delve into the world of DevOps, a revolutionary approach that bridges the gap between software development and IT operations.
Our focus will be on the role of version control, a cornerstone of DevOps practices, especially for data engineers. By the end of this lesson, you will have a solid understanding of version control systems like Git, their benefits, and their application in managing code versions and collaborating on data projects. 

DevOps seeks to improve collaboration and efficiency between development and operations teams.
<br>
DevOps, a combination of "Development" and "Operations," emerged as a set of practices aimed at bridging the gap between software development and IT operations.
<br>
DevOps advocates for continuous integration, continuous delivery, and continuous deployment, emphasising collaboration, automation, and monitoring throughout the software development lifecycle.
<br>
<br>
<img width="778" height="636" alt="image" src="https://github.com/user-attachments/assets/99ee45b6-8059-46bf-83a5-582a174a633a" />

<br>
<br>
Distributed version control systems (DVCS), such as GIT, allow each developer to have a local copy of the entire repository. This feature facilitates collaboration as developers can work on their own repository and then synchronise with others
<br>
<br>
<img width="780" height="512" alt="image" src="https://github.com/user-attachments/assets/4d493a95-05a2-46bd-ba09-24743003413e" />

<br>
<br>

Version control is a pivotal aspect of DevOps, epitomising the principles of collaboration, automation, and continuous improvement. 
It serves as the backbone for many DevOps practices, ensuring that software development and IT operations are seamlessly integrated. 
Furthermore, version control is crucial for implementing Continuous Integration and Continuous Deployment (CI/CD), enhancing the overall efficiency and reliability of data products.
Version control tracks changes, manages versions, and allows rollback to previous states, ensuring that any errors can be swiftly corrected without disrupting the entire system.

<br>

<b>Benefits of git include:</b> <br>
- Collaboration
- Code history
- Branching
- Merging

For data engineers, version control extends beyond code. It includes managing configuration files, SQL scripts, and data pipeline definitions. By using VCS, data engineers can maintain a history of changes, collaborate more effectively with team members, and ensure that data processing tasks are consistent and reproducible.

For data engineers, DevOps practices extend beyond managing code. 

They include maintaining data pipelines, managing configuration files, and ensuring that data processing tasks are consistent and reproducible.
<br>

##  Lession 2 - Mastering CI/CD: A guide for data engineers

#### Job Scheduling: 
Data pipeline jobs are often defined in scripts executed on Linux systems. These scripts are version-controlled using Git and GitHub, ensuring that any changes are tracked, and historical versions can be restored if necessary.

#### Branches and Commits: 
Developers create branches to work on new features or fixes independently. Once changes are tested and reviewed, they are merged into the main branch through pull requests.

#### Continuous Integration: 
Jenkins is used to automate the testing of new commits. Each commit triggers a series of tests to ensure that changes do not introduce any errors.

#### Continuous Deployment: 
After successful testing, Jenkins automates the deployment of updates to the production environment. Notifications are sent to the team regarding the deployment status, and error logs are monitored for any issues.

#### Jenkins: 
Jenkins is an open source automation server. It helps automate the parts of software development related to building, testing, and deploying, facilitating continuous integration, and continuous delivery. 


#### Version Control: 
Every change to the recommendation algorithms is tracked using Git and GitHub. This ensures that all updates are documented, and previous versions can be restored if needed.

#### Automated Testing: 
Jenkins automates the testing of new commits. Automated tests include unit tests, integration tests, and performance tests to validate the changes.


#### Benefits include:
- Timeliness: Automated scheduling ensures that data processing tasks are performed according to the defined schedule, which is critical for   generating timely reports and insights.
- Version Control : Using Git for pipeline scripts provides a robust framework for managing changes, facilitating collaboration among          engineers, and ensuring the production environment's stability.
- Scalability: DevOps practices enable Airbnb to scale its data operations efficiently, accommodating the growing volume of data and increasing complexity of workflows.
- Quality assurance: Automated testing ensures that only reliable and high-performing updates are deployed, maintaining a high-quality user    experience.
- Quality assurance: Automated testing ensures that only reliable and high-performing updates are deployed, maintaining a high-quality user   experience.
-Rapid innovation: Continuous deployment allows Netflix to introduce new features and improvements quickly, keeping the service competitive   and engaging.
- Operational efficiency : The integration of version control and CI/CD practices streamlines the workflow, reducing manual intervention and   the risk of errors.


 ### Continuous Integration and Continuous Deployment (CI/CD)

Continuous Integration (CI) involves frequently integrating code changes into a shared repository, where automated tests validate the changes. Continuous Deployment (CD) automates the release of validated changes to production.
For data engineers, CI/CD pipelines automate the deployment of data products, ensuring they are tested and released rapidly and reliably.


<img width="370" height="328" alt="image" src="https://github.com/user-attachments/assets/bd313bbf-d566-4b2e-8fac-494552a5244a" />
<br>
<br>

<img width="830" height="538" alt="image" src="https://github.com/user-attachments/assets/0f1d1e59-7360-486e-b569-afb18752d7a5" />


### Jenkins

Jenkins will notify team members if a failed commit has broken a build 

<img width="770" height="462" alt="image" src="https://github.com/user-attachments/assets/2dcfe39a-3e3f-4f42-aa67-f747b48d9cf1" />

## Lession 3: Conducting a code review

This process involves a systematic examination of a fellow developer’s code, aimed at catching errors, enhancing code quality, and promoting knowledge sharing. 

<img width="724" height="470" alt="image" src="https://github.com/user-attachments/assets/9db50862-8093-44d0-b0c6-b9cc195605b8" />

A developer works on a new feature for the data pipeline and pushes their changes to a feature branch in GitHub. 
They then create a pull request, summarising the changes and why they are necessary. Other team members are notified of the PR and begin reviewing the changes.

- Step 1 : Team members check the overall structure of the code, ensuring it adheres to coding standards and project guidelines.
- Step 2 : look for specific issues such as bugs, logic errors, and performance inefficiencies. Also Ensure that the code is well-            documented and readable.
- Step 3 : Feedback , Reviewers leave comments on specific lines of code or sections, providing constructive feedback. may suggest            alternative approaches, point out potential bugs, or ask for clarifications.
- Step 4 : Discussion, This back-and-forth helps improve the code and foster a collaborative environment.
- Step 5: Approval : Once the reviewers are satisfied with the changes, they approve the pull request. Can then be merged into the main
  branch, typically after passing automated tests and continuous integration checks.

<br>
Constructive Feedback - “Consider using a dictionary here instead of a list for faster lookups. This will improve the performance of this function, especially with larger datasets.”

<br>


## Summary
- Effective code reviews not only improve code quality but also enhance team collaboration and knowledge sharing
- DevOps are not just about tools and technologies, but also about fostering a culture of collaboration and shared responsibility
- For data engineers, mastering version control is essential for managing scripts, configurations, and data pipelines efficiently

