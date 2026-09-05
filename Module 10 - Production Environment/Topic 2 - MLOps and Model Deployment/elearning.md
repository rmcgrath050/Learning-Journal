# L5DE 10.2 - MLOps and model deployment

Machine Learning Operations - or MLOps - is the discipline that manages the full lifecycle of machine learning models in production. If machine learning models are the engines of intelligent systems, then MLOps is everything that ensures they’re built, tested, deployed, monitored, updated, and governed properly - not just once, but continuously.

it includes:
- Version control for data, code, and models
- Automated testing and deployment pipelines
- Monitoring for model performance and data drift
- Collaboration between data science, engineering, and operations

<br>
<img width="660" height="285" alt="image" src="https://github.com/user-attachments/assets/785d5d75-db85-4563-aeb2-12b4af60ef33" />
<br>

- DevOps bridge the gap between software development teams and IT operations. It introduces CI/CD pipelines, automated testing and infrastructure coding
- DataOps emerged to solve problems in pipeline - improving quality governance and delivery of data for analytics
- Machine learning systems combine software code, training data, model artifacts and runtime infrasture

This makes ML systems more fragile and unpredictable than traditional software
<br>

it is a collection of practices and components which include:
- Model Tracking: logging every model version, training dataset, configuration and performance metrics 
- Model Registry: central system for storing/managing model artifacts - often link to git and data sources 
- CI/ CD Pipelines: automation for training, testing and deploying models 
- Monitoring and Observability : accuracy, latency and data drift
- Collaboration and Handover

 without MLOps organisations often encounter:
 - unrealiable models that break in production
 - inconsistent environments between dev/ prod
 - No rollback plan for models
 - Lack of auditability

<br>

MLOps resolves this by 
- enforcing reproducibility : same model , same data, same results
- enablement of continuous improvement: automate retraning and redployment
- ensures compliance and governance : tracks decisions and configuration

<br>
<img width="873" height="498" alt="image" src="https://github.com/user-attachments/assets/50e39b0d-2a41-4356-a3eb-713bd8a2a00e" />

##### MLOPs Perks:
-Every part and step is tracked
- Blueprints are versioned
- Quality control catches issues early
- Products are delivered reliably, every time


## L2: Automating the machine learning lifecycle

 typical CI/CD process for ML might start with a new dataset becoming available. This change triggers an automated pipeline: the model is retrained using the updated data, evaluated against performance benchmarks, and - if successful - packaged and deployed into staging or production environments. If the model doesn’t meet required performance thresholds, the deployment can be halted, or the previous model can remain in place. This feedback loop allows for frequent, safe updates and eliminates the bottlenecks of manual review.
<br>
A level of reproducibility is essential for auditing, debugging, and improving models over time. It ensures that when a model is promoted to production, teams can trust where it came from and how it behaves! 

#### What is a model registry?

A model registry acts as a central hub where machine learning models are versioned, stored, and managed. It brings structure and control to model lifecycle management by clearly documenting which versions of a model are approved for production, which are under review, and which have been deprecated. Imagine a model registry as a digital warehouse. Each model stored inside has a label describing how it was trained, what data it used, and whether it's ready for deployment. When something goes wrong in production, engineers can quickly check the registry, identify the active version, and - if needed - roll back to a previous version that’s known to be stable.


### Tools that support automation 
Kubeflow is built for teams already using Kubernetes. It allows for scalable, production-grade machine learning workflows and supports complex orchestration of tasks like distributed training, hyperparameter tuning, and multi-step pipelines. It’s more infrastructure-heavy but offers excellent flexibility for organisations operating in cloud-native environments.
Goal is to streamline the development-to-deployment process in machine learning - (Perhaps for project mention this an improvement moving forward?) 

Without experiment tracking or a model registry, teams lose visibility into how a model was created - making it hard to debug or revert changes confidently! 

