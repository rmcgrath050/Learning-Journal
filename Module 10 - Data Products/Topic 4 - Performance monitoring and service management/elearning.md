## L1 : Lesson 1 - Advanced Metrics & KPIs for Production Systems

- Latency measures the time it takes for a request to travel from the client to the server and back. It's a critical indicator of the responsiveness of a system.
- Traffic measures the demand placed on your system and is typically measured in requests per second.
- Errors track the rate of failed requests, including HTTP 500 errors, timeouts, or other application-specific failures.
- Saturation measures how "full" your system is, reflecting the utilization of resources like CPU, memory, disk space, and network bandwidth.

(Not sure how any relate to my current role - need to investigate)

Start with the four “golden signals”: latency, traffic/throughput, errors, and saturation. For data engineering, add freshness (how old the most recent good data is), completeness (how much you received versus expected), schema health (drift or validation failures), and cost per successful outcome (for example, £ per million rows landed). Each signal should answer a user-facing question such as, “Will the dashboard have today’s data by 9am?” rather than a purely technical one like, “Is CPU above 70%?”

<img width="1820" height="1252" alt="image" src="https://github.com/user-attachments/assets/b123d390-796c-4e05-91a2-6574be2bea7f" />

<br>
##### SLIs, SLOs, SLAs - and the error budget that keeps you honest

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
- 
