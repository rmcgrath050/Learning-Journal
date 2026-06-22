# L5DE 8.2 - Workflow management for data pipelines

## L1. Principles of workflow management

You need to manage the how, when, and what, including:
- How are tasks connected and ordered?
- When do they run? On a schedule, in response to a trigger, or manually?
- What if something fails? Can it recover? Will someone be notified?

As pipelines grow the stakes grow including:
- 1 missed run could lead to outdated reports
- 1 fail might block downstream processes
- poor scehduling may overload systems at peak times

Workflow management prevents this by enfotcing visability, control and resillance! Key benefits include:
- dependancy tracking, tasks in correct order!
- error handling and retries
- logging and observability
- modularity and reusability
<br>

<br>

<img width="1039" height="556" alt="image" src="https://github.com/user-attachments/assets/0204414b-4739-4bad-87b7-7cc942c51790" />


## L2. Creating and manging data pipeline workflows

Most flows contains following blocks:
1. Tasks - individual units of work eg a query, api call etc
2. Dependancies - rules that define order of scheudle
3. Triggers / schedules - define when workflow starts , a specifc time, a file arrives etc
4. State - wether a task success fails or needes retying
5. Obserability - tracks logs execution times, failures and success metrics


There are several common workflow patterns in data pipelines:
- Linear Chains – Simple A → B → C sequences. Easy to follow, common in batch processing.
- Fan-out/Fan-in – A single task splits into parallel tasks (e.g., processing multiple datasets), which then merge back into a single task.
- Conditional Branching – The path changes based on task outputs (e.g., only clean data if the file exists).
- Sensor-Driven – Workflows that wait for an external event, like a new file or a message.

<br>
<br>
<img width="969" height="499" alt="image" src="https://github.com/user-attachments/assets/7315bc99-0bcf-4c3b-8aee-146a2f12d228" />

<br>

These tools take the logic, timing, and tracking of your pipeline and wrap them in a controllable system. They’re like a mission control centre for your data jobs: monitoring execution, handling dependencies, retrying failed tasks, and visualising the flow of operations. They don’t just run jobs - they manage workflows as code.


Here are the key capabilities shared by most orchestration tools:
- Define workflows using code or configuration (usually Python or YAML).
- Schedule tasks to run at specific times or when triggered by an event.
- Manage dependencies so tasks run only when prerequisites are complete.
- Retry on failure or send alerts if things go wrong.
- Provide visual dashboards for monitoring task status, logs, and history.
- Track state, so workflows resume gracefully if interrupted.


##### Apache airflow
- Industry standard in many organisations, with a strong community and plugin support.
- Workflows are defined as Directed Acyclic Graphs (DAGs) in Python.
- Well-suited to batch processing and ETL-style pipelines.
- Built-in UI for tracking and retrying tasks.
- Can feel heavyweight or complex for smaller pipelines.


## L.3 Techniques for optimising data workflows

##### Question : how to optomise a late dahboard? 
- first step understanding where the delay occurs
- could be due to single slow task, waiting on a dependancy, are tasks running in sequence when they should be parallel?


##### 3 Key techniques for workflow optimisation 
- Parrallelism and concurrency, can run tasks parrall without increasing complexity. Eg Downloading five files in sequence might take 10 minutes. In parallel, it could take 2–3 minutes depending on bandwidth. (Better use of CPU).
- Caching Intermediate Results , if parts of workflow dont change can cache results rather than regenerating each time, speeds up pipeline and avoids redundant computation. Can use task decorators or checkpints  ( availble in conposer tools like prefect) to reuse cached outputs when input data hasnt changed. Tradeoff here includes data staleness if not managed correctly. 
- Scaling Resources Strategically , Some tasks may be CPU-bound (like sorting or joining large tables), while others may be IO-bound (like pulling from a remote API). Optimising your workflow might mean increasing parallel workers, switching to more powerful compute, or offloading to scalable infrastructure like cloud functions. Tradeoff here inclues scaling compute = increased cost! 

The goal isn’t to make everything “as fast as possible” - it’s to make workflows efficient, reliable, and right-sized for their purpose!
<br>

## L.5 Automation strategies for repetitive tasks

Automation adds most value to 
- Routine Scheduling
- Event Driven Triggers, Tools like Prefect, Dagster, and cloud-native platforms (AWS Lambda, Azure Functions) support sensor-based or webhook triggers, allowing workflows to start precisely when needed - no sooner, no later.
- Reuabale workflow template, creating workflow templates reduces duplication and onboarding time.

In reality, automation must be observed and maintained. This is why logging, monitoring, and alerting systems are essential companions to automation. It’s also good practice to keep automation code
- version controlled
- Documented with clear instuctions
- Modular enough to be reused and extended

## L.6 Monitoring and maintaining workflow efficiency

In real-world data engineering, pipelines fail for many reasons - API outages, schema changes, network issues, or just plain old logic errors. What separates resilient systems from fragile ones is how early and clearly those failures are detected. That’s where monitoring comes in!
<br>
<br>
What should you monitor?
- Taks success/ failure rates
- Execution times, are thes increasing? a sign of scale issues/ downstream lag eg data volume scaling issues, indexes no longer fit entirely into the server's RAM (memory).
- Resource usage , CPU, memory, disk - especially important in cloud deployments.
- Queue backlogs, delays here can point to upstream bottlenecks


Most orchestration tools provide a UI or dashboard that visualises this information and lets you drill into logs. If you’re using cloud-native tools, you can integrate with services like CloudWatch, Datadog, or Grafana for deeper insights.

<br>
<img width="834" height="584" alt="image" src="https://github.com/user-attachments/assets/be10eb08-cf72-41d6-b015-2b483f586418" />
<br>

- dont relay on dahsboards alone, make sure to set up alerts or if a runtime exceeds expectations
- Make sure to check logs as a habit, espically after updates or infrastucture changes
- Clean up, Retire old workflows that no longer run. Consolidate duplicated logic. Archive logs and intermediate files to avoid clutter and storage bloat.
- Test changes in isolation, Use test environments or sandbox DAGs to trial updates before promoting them to production.


## Summary 

- Workflows in data engineering are structured sequences of dependent tasks that manage how data is moved and transformed.
- Effective workflow design involves clear task boundaries, defined dependencies, and scheduled execution using tools or code.
- Workflow orchestration tools like Apache Airflow and Prefect allow engineers to schedule, monitor, and automate complex pipelines.
- Optimisation techniques such as parallelism, caching, and resource tuning improve the speed and efficiency of data workflows.
- Automation reduces manual repetition by using time-based or event-driven triggers and reusable workflow templates.
- Monitoring and maintenance involve tracking workflow performance, setting alerts, and regularly reviewing logs to ensure reliability.
