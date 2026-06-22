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


