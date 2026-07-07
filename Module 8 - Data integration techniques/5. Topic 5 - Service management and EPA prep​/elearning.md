# L5DE Performance Monitoring and Service Management

## L1. Advanced Metrics & KPIs for Production Systems

In production, the only meaningful metrics are the ones users feel. This lesson moves you beyond server dials to outcome signals such as tail latency, data freshness, and error-budget burn. You’ll learn how to define Service Level Indicators (SLIs), set realistic SLO targets, and pick a compact set of KPIs that keep your pipelines reliable!

#### Objectives:
- Define SLIs/SLOs for a data pipeline or service and explain why tail latency and freshness matter more than averages
- Calculate and interpret core pipeline KPIs-latency distributions, throughput, error rate, saturation, freshness, completeness, schema health, and cost per successful unit.
- Use error budgets and burn rates to decide when to act, and describe the different emphasis for batch versus streaming systems.

<img width="1166" height="616" alt="image" src="https://github.com/user-attachments/assets/23251500-e626-4ba0-8a04-d09164071159" />

- Latency - The time it takes to serve a request end-to-end. Track it as a distribution (p50/p95/p99), and treat “slow enough to violate the SLO” as an error. In data pipelines this can be job runtime or event-to-serving latency.
- Traffic - How much demand hits the system. Common units are requests/sec, queries/sec, rows or messages per second, or jobs/hour for batch.
- Errors - The rate of failed or incorrect results. Include explicit failures (5xx, exceptions), implicit ones (timeouts, SLO-breaching latency), and content errors (schema/quality failures in data jobs)
- Saturation - How “full” the service is relative to its limits. Watch sustained utilization of constrained resources (CPU, memory, I/O, thread/connection pools, queue depth, Kafka consumer lag) and how close you are to headroom.
- Start with the four “golden signals”: latency, traffic/throughput, errors, and saturation. For data engineering, add freshness (how old the most recent good data is), completeness (how much you received versus expected), schema health (drift or validation failures), and cost per successful outcome (for example, £ per million rows landed). Each signal should answer a user-facing question such as, “Will the dashboard have today’s data by 9am?” rather than a purely technical one like, “Is CPU above 70%?”

<br>
<br>
<img width="1282" height="904" alt="image" src="https://github.com/user-attachments/assets/49b3e800-7387-4886-8bc7-91158f024d68" />
<br>
<br>
<img width="894" height="786" alt="image" src="https://github.com/user-attachments/assets/7f6da108-2d62-4c08-9386-4a0da04794d8" />
<br>
<br>
Averages hide pain. Track latency as a distribution: p50 is typical, p95 and p99 expose the “long tail” that users notice. In a warehouse query or Spark job, a small number of very slow runs can break SLAs even when the mean looks fine. When visualising, place p95/p99 on the same graph as p50 so tail growth is obvious

#### Make the KPIs concrete (formulas you can implement)

- Freshness : now() − max(event_time of last successful partition). This should use event time, not ingestion time.
- Completeness : received_records / expected_records for the period, with a data-quality gate if it drops below a threshold
- Error rate: failed_runs / total_runs for batch, or failed_messages / total_messages for streaming.
- Throughput: rows or messages per second; for Kafka also watch consumer lag (difference between last produced and last consumed offsets)
- Saturation: sustained resource pressure that correlates with user-impacting metrics (e.g., memory pressure alongside soaring p95).
- Cost per success: (compute + storage + egress) / number_of_successful_outcomes. Use it to spot noisy retries or inefficient joins.


#### SLIs, SLOs, SLAs - and the error budget that keeps you honest

- SLA : Service Level Agreements (SLAs) is the agreement you make with your clients or users. You can think of it as the external promise with consequences.
- SLO : Service Level Objectives (SLOs) are the objectives your team must hit to meet that agreement. They’re your internal target(s) (“p95 < 10 minutes, 99% of days”).
- SLI : Service Level Indicators (SLIs) is the numbers you base your performance on. It’s what you measure (e.g., “p95 pipeline end-to-end latency”).
- Error Budget :  Error Budget is the permissible amount of unreliability or downtime that a service can experience over a defined period without negatively impacting user experience or breaching SLOs.
- Burn rate : Burn Rate measures how quickly a company is spending its available capital over a specific period, typically a month. You could attribute this locally to a budget for a specific tool too.

<i>From the SLO you get an error budget. Example: an availability SLO of 99.5% per 30-day month gives 0.5% × 43,200 min = 216 minutes of total permitted impact. Alerts should watch burn rate too: if you’re consuming budget far faster than the time window (e.g., 10% of the month’s budget in an hour), you have a real problem even if you’re not “down.”</i>

#### Batch versus streaming: what to emphasise


