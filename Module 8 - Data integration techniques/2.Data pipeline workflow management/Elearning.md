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
- Parrallelism and concurrency, can run tasks parrall without increasing complexity. Eg Downloading five files in sequence might take 10 minutes. In parallel, it could take 2–3 minutes depending on bandwidth. (Better use of CPU)
- Caching Intermediate Results , if parts of workflow dont change can cache results rather than regenerating each time, speeds up pipeline and avoids redundant computation. Can use task decorators or checkpints  ( availble in conposer tools like prefect) to reuse cached outputs when input data hasnt changed
- 


