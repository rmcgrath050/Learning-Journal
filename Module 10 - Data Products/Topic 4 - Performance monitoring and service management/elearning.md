## L1 : Lesson 1 - Advanced Metrics & KPIs for Production Systems

- Latency measures the time it takes for a request to travel from the client to the server and back. It's a critical indicator of the responsiveness of a system.
- Traffic measures the demand placed on your system and is typically measured in requests per second.
- Errors track the rate of failed requests, including HTTP 500 errors, timeouts, or other application-specific failures.
- Saturation measures how "full" your system is, reflecting the utilization of resources like CPU, memory, disk space, and network bandwidth.

(Not sure how any relate to my current role - need to investigate)

Start with the four “golden signals”: latency, traffic/throughput, errors, and saturation. For data engineering, add freshness (how old the most recent good data is), completeness (how much you received versus expected), schema health (drift or validation failures), and cost per successful outcome (for example, £ per million rows landed). Each signal should answer a user-facing question such as, “Will the dashboard have today’s data by 9am?” rather than a purely technical one like, “Is CPU above 70%?”

<br>
<img width="1820" height="1252" alt="image" src="https://github.com/user-attachments/assets/b123d390-796c-4e05-91a2-6574be2bea7f" />

<br>
<br>

### SLIs, SLOs, SLAs - and the error budget that keeps you honest

- Service Level Agreements (SLAs) is the agreement you make with your clients or users. You can think of it as the external promise with consequences
- Service Level Objectives (SLOs) are the objectives your team must hit to meet that agreement. They’re your internal target(s) (“p95 < 10 minutes, 99% of days”).
- Service Level Indicators (SLIs) is the numbers you base your performance on. It’s what you measure (e.g., “p95 pipeline end-to-end latency”)
- Error Budget is the permissible amount of unreliability or downtime that a service can experience over a defined period without negatively impacting user experience or breaching SLOs
- Burn Rate measures how quickly a company is spending its available capital over a specific period, typically a month. You could attribute this locally to a budget for a specific tool too.

From the SLO you get an error budget. Example: an availability SLO of 99.5% per 30-day month gives 0.5% × 43,200 min = 216 minutes of total permitted impact.

<br>

Batch vrs stream
<br>
Batch favours runtime distribution, queue wait, and freshness at deadlines (e.g., “by 09:00”). Streaming prioritises end-to-end latency (event time to serving), consumer lag, and backpressure.

#### metrics to look into regarding SLO :
- Tail latency (p95/p99) exposes rare but painful slowdowns; means hide them.
- 30 days × 24 HRS × 60 MIMS = 43,200 minutes. 1% allowed impact = 432 minutes.  - Add this in for agreed batch jobs
- You saw why tail behaviour (p95/p99) tells a truer story than averages and how to turn measurements into SLIs with realistic SLOs and, where needed, SLAs

## L2 : Dashboards & Visualisation Tools

Think of your system as a play. Metrics are the applause meter - numbers over time that tell you if the audience is happy (latency, error rate, freshness, lag). Logs are the script - what was said and where it went wrong (messages, exceptions, validation failures). Traces are the stage map - who moved where and which scene dragged (spans across services). When all three share the same identifiers and time window, you can follow the story cleanly from symptom to cause.

<br>
Connect metrics from your cloud monitor or Prometheus, and keep labels simple and stable - service, environment, region. High-detail identifiers (such as user IDs) belong in logs and traces, not in time-series labels, or your panels will become slow and noisy. Add variables for service and environment and use them in all panel queries and titles

eg ask rich about these type of metrics? 
When it breaches the SLO threshold or burns error budget faster than your chosen window (e.g., >2% in 1h).
- https://signoz.io/blog/kibana-vs-grafana/


## L3: Lesson 3 - Analysing Performance Trends & Identifying Bottlenecks

- Establish what “normal” looks like: To find the cause of an issue, begin with a baseline period when things were healthy. Best place to start is to capture p50 and p95 latency, error rate, and - if relevant - data freshness over that time


•• explain this further
- If latency rises and consumer lag grows while CPU is low, the constraint is probably upstream I/O or the source system, not compute
- If lag grows and CPU/GC time saturate, compute is your bottleneck
- If throughput is steady but queue wait increases, the queue is under-provisioned or a downstream limit is throttling you


#### Types of bottleneck 

<br>
<img width="960" height="662" alt="image" src="https://github.com/user-attachments/assets/07ccfa17-a388-44c4-9ac2-dcf600857f1b" />

For batch, focus on stage-level runtime and queue delay before the deadline (e.g., “fresh by 09:00”). For streaming, watch end-to-end latency and consumer lag together; short spikes in lag that self-heal may be harmless, but sustained lag plus rising service time points to a real limit.

#### Test with small change

- Doubling consumers without reducing lag suggests the bottleneck isn’t compute.
- Reducing a heavy shuffle or adding a missing index that cuts p95 stage time is strong evidence of a compute constraint.
- Raising warehouse concurrency that clears queue wait confirms a downstream limit


Keep experiments safe (feature flags, reversible config, or canary workloads), and record the before/after with annotations so the learning is preserved for the next person on call

## L4: Incident Response Essentials

<br>
<img width="802" height="760" alt="image" src="https://github.com/user-attachments/assets/455fb817-4d39-4c59-9fbd-d9199500eed8" />

An incident is any unplanned event that degrades service or data quality for users or downstream teams. By declaring early, you can downgrade the severity later. It’s best to keep a short, unambiguous scale tied to impact and urgency. For example:

<br>
<img width="866" height="746" alt="image" src="https://github.com/user-attachments/assets/c45dde8d-55da-4a02-b531-ba59c71ce110" />

<br>
<br>
<img width="812" height="646" alt="image" src="https://github.com/user-attachments/assets/cb749617-84a3-4a0f-8267-b6484d130a38" />
<br>
<br>
<img width="1618" height="622" alt="image" src="https://github.com/user-attachments/assets/ece16071-d31e-410b-adfa-0b9e4c06b745" />
