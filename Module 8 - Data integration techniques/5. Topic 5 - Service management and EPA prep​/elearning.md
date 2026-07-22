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

Batch favours runtime distribution, queue wait, and freshness at deadlines (e.g., “by 09:00”). Streaming prioritises end-to-end latency (event time to serving), consumer lag, and backpressure. In both cases, correlate user-facing SLIs with cause indicators: if lag rises while consumer CPU is idle, the bottleneck is upstream or in I/O; if CPU and GC time spike during a shuffle, the constraint is compute or memory.

Design a top row that answers “Are we meeting our SLOs right now?” with single-stat cards for p95 latency, freshness, and error rate. The middle row explains why (lag, queue depth, stage time, GC). The bottom row shows resources (CPU, memory, I/O, concurrency). Keep units consistent and add deploy/incident annotation.

Don’t page on vanity metrics (e.g., any single error). Don’t add high-cardinality labels (like user_id) to time-series metrics-they explode storage and slow queries. And don’t set unattainable SLOs; start with what you already achieve, then ratchet up.

Why it matters: In software, tiny temporary glitches happen constantly (like a single user losing Wi-Fi for a split second). If your system alerts a human for every single error, engineers will experience alert fatigue. They will start ignoring notifications, causing them to miss real, massive system crashes.

Why it matters: Monitoring databases (like Prometheus) store metrics by creating a separate timeline for every unique label combination. If you attach a unique user_id to a metric, the database has to create millions of separate timelines. This explodes your storage costs and makes your dashboards incredibly slow or completely broken.The fix: Keep time-series labels broad (like region: us-east or status: 500). If you need to investigate a specific user's path, look at your system logs or traces, not your metrics.

The two Service Level Indicators (SLIs) you should show in the top row are Pipeline Freshness and 95th Percentile (p95) Latency/Runtime.

1.  Pipeline Freshness (The Direct Impact) : his is your primary user-facing symptom. The business does not care how fast the pipeline runs; they care that the daily sales data is missing at 09:00. Because freshness has breached its target, it immediately flags to an engineer that the business commitment is broken
2.  p95 Latency / Runtime : is reveals where the system is failing. The scenario notes that average runtime is stable, meaning 90%+ of the pipeline steps or historical runs look perfectly normal. However, the surge in p95 latency shows that a specific, heavy edge case—such as an unindexed table, a massive batch of month-end data, or a stalled upstream dependency—is bottlenecking the entire system.

#### things to understand for interview
1. "I understand that looking at averages can hide major glitches that ruin a user's experience.
2. Show you care about efficiency. (e.g., "I know that tracking too much unnecessary data can slow down systems and waste company money.")
3. Instead of "Vanity Metrics": Show you care about real impact. (e.g., "I believe data engineering should focus on solving actual business problems, not just tracking numbers that look good on paper."

Your monthly SLO is 99.0% ‘fresh by 09:00’. How much budget do you have in a 30-day month? 30 days × 24 × 60 = 43,200 minutes. 1% allowed impact = 432 minutes.

#### Lession summary

In this lesson you explored the signals that matter in production: the golden signals (latency, traffic, errors, saturation) plus data-platform essentials like freshness, completeness, schema health, and cost per successful outcome. You saw why tail behaviour (p95/p99) tells a truer story than averages and how to turn measurements into SLIs with realistic SLOs and, where needed, SLAs. We walked through practical formulas for computing key KPIs and used error budgets and burn rates to judge when a problem is significant.


## L2. Dashboards & Visualisation Tools

Dashboards should answer one question at a glance: Are users getting value right now, and if not, where should I look first? This lesson shows how to design outcome-first dashboards that are readable at 2am, reusable across services, and fast enough to trust.

#### Objectives
1. Arrange dashboards so one audience sees one story at a glance.
2. Use Grafana for outcome-focused time-series and Kibana for searchable explanations.
3. Link panels so context (service, environment, time) follows the user into logs and traces.

Put outcomes at the top: a small set of SLIs with their SLO context, such as p95 latency, error rate, and data freshness. In the middle, show explanations: signals that hint at causes, for example consumer lag for a stream or stage time for a batch job. At the bottom, show resources and dependencies - CPU, memory, I/O, and the health of things you rely on like your warehouse or message broker. This layout means a learner can glance at the top row to see if users are impacted, and then scan downwards to understand why.

Queue dept: how many tasks, this can increase due to: 
- Not enough compute resources.
- A slow processing step.
- A downstream system is delayed

<i>
An SLI (Service level indicator)  is simply a measurement. How is the system actually performing?
An SLO (service level objective) is the target you want the SLI to meet.
SLI = What happened.
SLO = What should happen.
</i>

<br>

indicators that explain change:
- Consumer lag
- Queue depth
- Transformation stage time
- GC %
- Cache hit rate
- Top error types


Think of your system as a play. Metrics are the applause meter - numbers over time that tell you if the audience is happy (latency, error rate, freshness, lag). Logs are the script - what was said and where it went wrong (messages, exceptions, validation failures). Traces are the stage map - who moved where and which scene dragged (spans across services). When all three share the same identifiers and time window, you can follow the story cleanly from symptom to cause.


#### Grafana

Grafana is where you show the state of the world. Start with a single dashboard for one pipeline or service. At the top, place a few outcome cards-p95 latency, error rate, and freshness-with each card labelled in plain language and with units. Plot p50, p95, and p99 on the same graph so tail pain is visible. 



## L3 . Analysing Performance Trends & Identifying Bottlenecks

Learning objectives:
1. Describe a sensible baseline for a service or pipeline
2. Separate seasonality from drift
3. Use paired signals (latency, lag, saturation) to locate a likely bottleneck
4. Validate your diagnosis with a small, safe experiment

To find the cause of an issue, begin with a baseline period when things were healthy. Best place to start is to capture p50 and p95 latency, error rate, and - if relevant - data freshness over that time.

For pipelines, you can also create baselines per stage (ingest, transform, load) so a change in one phase is visible even if the end-to-end number looks flat.


Performance metrics explainations:

- If latency rises and consumer lag grows while CPU is low, the constraint is probably upstream I/O or the source system, not compute.
- If lag grows and CPU/GC time saturate, compute is your bottleneck.
- If throughput is steady but queue wait increases, the queue is under-provisioned or a downstream limit is throttling you

Keep Little’s Law in mind (items in system ≈ arrival rate × time in system): when arrival stays the same but time increases, the queue length must grow - so look for the step that slowed. Align time axes on your dashboard so these relationships are easy to see at a glance

<br>

### Identify the type of bottleneck

 - Upstream : Upstream bottlenecks show up as idle consumers with growing wait times (slow source! network, or storage).
 - Compute : Compute, or midstream, bottlenecks show saturated CPU, long GC, skewed partitions, or expensive joins that inflate stage time
 - Downstream : Downstream bottlenecks appear when writes stall - warehouse concurrency is maxed, object store errors spike, or a rate limit kicks in.

For <b>batch</b>, focus on stage-level runtime and queue delay before the deadline (e.g., “fresh by 09:00”). For <b>streaming</b>, watch end-to-end latency and consumer lag together; short spikes in lag that self-heal may be harmless, but sustained lag plus rising service time points to a real limit.

#### Prove it with a small change

- Doubling consumers without reducing lag suggests the bottleneck isn’t compute.
- Reducing a heavy shuffle or adding a missing index that cuts p95 stage time is strong evidence of a compute constraint.
- Raising warehouse concurrency that clears queue wait confirms a downstream limit.

## L4. Incident Response Essentials

- define what an incident is, assign clear roles, restore service first, and communicate in a way that lowers stress for everyone involved.
- Define incidents in plain language and grade severity by impact and urgency.
- Run the first 15 minutes with clear roles - Incident Commander, Comms Lead, Scribe, Resolvers - and a restore-first approach.
- Use simple, consistent communication and documentation so decisions, actions, and next steps are always visible


An incident is any unplanned event that degrades service or data quality for users or downstream teams. By declaring early, you can downgrade the severity later. It’s best to keep a short, unambiguous scale tied to impact and urgency. 

- Minute 0–2: declare, set severity, assign roles, create the channel/ticket.
- Minute 2–7: verify impact on SLIs, choose the fastest safe mitigation (rollback, toggle feature, scale fallback).
- Minute 7–15: confirm recovery, schedule a deeper diagnosis if impact remains, and set the next update time.

#### Example

Number 1: 
- Pattern: “p95 ingest latency ↑ from 6m to 18m (+12m) and still rising.”
- Batch example: “Freshness breached: dashboard is 35m late (target: by 09:00).”
- Streaming example: “Event-to-serve p95 is 3.2s (baseline 900ms).”
<br>

Number 2: 
- Pinpoint the scope so the right people look in the right place. Include service/pipeline, environment, region, and (if known) the stage/component

<br>
Number 3: 
- Give a timestamp and any correlated change (deploy, feature flag, config). This anchors the timeline and speeds correlation.

<br>
You also learned a simple, repeatable way to communicate - one channel, predictable updates, and links to evidence - so everyone sees the same picture and moves in the same direction.

## L6 : Lesson 5 - Playbooks, Alerting & Real-Time Monitoring

When production misbehaves, you need steps you can actually run and alerts that wake people only for problems that matter. This lesson shows how to write playbooks that work under pressure, design SLO-aware alerts that reduce noise, and watch real-time health so you catch trouble early.

A playbook is a short, scenario-specific checklist that anyone on-call can run to restore service safely under pressure. It turns a known failure mode (e.g., “Kafka consumer lag spike”) into a single, executable path: how to confirm it’s really happening, what to try first, when to stop, how to roll back, and how to verify that users are healthy again.

A good playbook contains:
- trigger:
- prechecks
- first safe action
- decision points
- Rollback and exit
- verification
- context

  #### Playbook example


- Start with a trigger (“Kafka consumer lag > 50k for 10 min”), then pre-checks to confirm you’re solving the right failure (“is producer healthy?”, “network OK?”, “lag by partition?”).
- List first actions that are reversible - scaling consumers, pausing competing loads, or rolling back a change.
- Mark decision points (“if lag falls for 5 min, continue; if not, escalate to…”) and finish with rollback/exit and verification (“lag < 5k for 10 min; p95 back under SLO”).
- Keep one page per failure mode, store it in version control beside the service, and drill it occasionally so muscle memory forms. If a newcomer can’t run it end-to-end, it isn’t finished.


<img width="1300" height="604" alt="image" src="https://github.com/user-attachments/assets/b9981176-2603-417e-909f-eb6136ef0a6e" />

<br>

Real-time health checks buy you minutes when things go wrong. Heartbeats can assert liveness from the data’s point of view (a tiny record each minute that must appear at the sink). You can also track freshness as “now minus newest good event time,” not ingestion time, so late data shows up as a real risk. (I did consider dbt freshness but didnt want alerts for late data appearing as unrpedicable load via FCA)

## L6. Lesson 6 - Post-Incident Learning, RCA & SLAs

- Hold the review soon - while context is fresh - but not in the heat of response.
- Keep it short and consistent.
- Start with the timeline: a clear sequence of facts pulled from dashboards, alerts, and the incident channel.
- Follow with impact in user terms (SLO minutes burned, missed deadlines, customer tickets).
- Then discuss what helped and what made it harder (e.g., missing deploy annotation, noisy alert, undocumented failover).
- Make it blameless by treating actions as outcomes of system conditions - staffing, tools, processes - not personal failings.

<br>

- Prevent  : (reduce likelihood): e.g., add an index; fix a skewed join; add schema validation pre-ingest
- Contain : (reduce blast radius): e.g., automatic rollback on burn-rate breach; isolate load pool; circuit breaker on downstream.
- Detect : (reduce time to notice): e.g., deploy annotations; a freshness heartbeat; better alert routing.


-  Measure what users actually feel-tail latency and data freshness-and manage reliability through clear SLOs and error budgets.
- Make the dashboard a single story at a glance (outcomes → explanations → resources) and link Grafana outcomes to Kibana explanations with preserved context.
- Compare today to a baseline and read paired signals to hypothesise the constraint-then prove it with one small, reversible change.
- Declare early, assign roles, and run a restore-first rhythm with short, factual updates that keep everyone aligned.
- Use checklist-style playbooks and SLO/burn-rate paging, backed by simple heartbeats and freshness checks that lead straight to action.
- Run blameless reviews that produce specific prevent/contain/detect actions, and set SLAs as realistic subsets of your demonstrated SLO performance.
