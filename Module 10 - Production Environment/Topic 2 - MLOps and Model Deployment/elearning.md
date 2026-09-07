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

## L3: Deploying machine learning models

Before a model can be deployed, it must be prepared to run outside its original development environment. This process, called packaging, makes sure the model can operate reliably on different machines and platforms.

For more complex systems, it often involves placing the model inside a container - for example, with Docker - along with all its dependencies. Benefits of containerisation include:

- Consistency between development, testing, and production environments
- Portability across cloud providers and local servers
- Isolation from other system processes, reducing conflicts

#### Different deployment strategies

- Embedded deployment – the model is shipped within an application, ideal for offline or mobile environments.
- Model-as-a-Service – the model is hosted remotely and accessed through an API, allowing frequent updates without changing the        application itself.
- Blue-green deployments – two identical environments are maintained; one is live, one is idle. New models are deployed to the idle     environment and swapped in only when validated.
- Canary releases – a new model is given to a small percentage of users first, so its performance can be monitored before a wider       rollout

The infrastructure you choose directly affects a model’s performance, scalability, and cost. Small-scale applications might work well on a single server or virtual machine. For high-traffic scenarios, orchestration systems like Kubernetes allow for scaling up resources automatically, balancing workloads, and providing resilience if something fails. Cloud providers also offer managed services such as AWS SageMaker, Azure Machine Learning, and Google Vertex AI, which take care of much of the operational complexity - ideal for teams who want to focus on models rather than infrastructure management. Could maybe use this for project using kubernetes!

A good deployment process includes the ability to roll back to previous versions, retrain models when performance drops, and monitor their behaviour continuously. Treat deployment as a living process, not a single event.

## L4 Monitoring and maintaining models in production

When models first go into production, they’re optimised for a specific dataset and context. But production environments are dynamic. The inputs, user base, and business objectives may evolve. Without a monitoring plan, these changes can degrade the model’s predictions - sometimes subtly, sometimes drastically. Model monitoring ensures that you can detect issues early and take corrective action before they impact business outcomes. It turns deployment from a “fire and forget” process into a cycle of observation, evaluation, and improvement.


- Model performance - tracking accuracy, precision, recall, or other relevant KPIs over time.
- Data drift - identifying when the characteristics of incoming data deviate from the training data.
- Prediction distribution - watching for changes in the spread or frequency of certain predictions that might indicate a bias or imbalance.
- Latency and throughput - ensuring the model is serving predictions within required timeframes

Data drift is one of the most common causes of performance degradation. It occurs when the statistical properties of input data change over time. There are different types:
- Covariate drift - when the distribution of input features changes.
- Prior probability drift - when the relative frequency of labels changes.
- Concept drift - when the relationship between inputs and outputs changes.

Detection methods might include comparing statistical summaries of current data with the training data or using secondary models trained to recognise distribution changes. The goal is to trigger an alert when drift is significant enough to require retraining.

### Responding to a model degrade:
- Retraining - updating the model with new data to reflect the current environment.
- Rollback - reverting to a previous, more reliable model version from the model registry.
- Parameter tuning - making targeted adjustments without a full retrain

## L5. Managing and evolving deployed models

Once a model is running in production, the job is not simply to keep it alive; it’s to ensure it stays relevant, accurate, and aligned with business goals. Over time, the world changes - data evolves, user behaviour shifts, regulations are updated, and new business priorities emerge

<br>
Models are trained on historical data, but the real world doesn’t stand still. Over time, data drift and concept drift can erode performance. In some cases, retraining may be needed weekly or even daily; in others, updates may be less frequent but still essential. The right schedule depends on the business context, the volatility of your data, and the cost of retraining. Continuous training ensures that models:

- Stay aligned with current data patterns
- Adapt to new customer behaviour or market trends
- Maintain performance on key business metrics

High-quality retraining data is the foundation for accurate models. If the new data is noisy, biased, or inconsistent, retraining can make performance worse, not better. Best practices include:
- Validating input data for completeness and accuracy before retraining
- Using feature engineering pipelines that are consistent across training and production
- Checking for changes in schema or data definitions that could break the model

For example, if a customer churn model is retrained with incomplete transaction data due to an upstream system outage, it may learn the wrong patterns and degrade prediction accuracy.

### Best Practices for Model deployment 
***remember this for your DBT model!
- Embedding monitoring, retraining, and versioning into standard operating procedures
- Using A/B testing to compare new and old models before committing to full deployment
- Documenting every model’s purpose, assumptions, and known limitations for future teams
- Building governance processes to ensure compliance with evolving regulations
