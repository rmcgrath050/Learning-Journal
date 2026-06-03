
## First: Translate the Problem Into Components

First: Translate the Problem Into Components

You likely have something like:

Source system loads data
    ↓
Airflow DAG starts
    ↓
dbt model builds reporting table
    ↓
Quarterly report generated

#### Problem: 
But the issue is:
The source data does NOT arrive at a fixed predictable time.

So:
sometimes data is ready
sometimes not
but your DAG still runs on schedule


That creates:
incomplete tables
stale active records
incorrect quarterly outputs

### Why no airflow sensors?
- Your bank avoiding Airflow sensors is also common.

Classic Airflow sensors:
- poll repeatedly
- occupy workers
- can create scaling issues
- can become operationally messy



### Designs
- Control Tables / Metadata Tables (Upsteam tables update and dag checks these) 
- Event-Driven Triggers (using Pub/Sub, Kafka, webhooks)
- Batch Windowing (Quarterly DAG only allowed to run:6am–12pm after upstream completion SLA) , business-defined processing windows ,         avoids waiting 
- Could maybe do batch now as its quickest design , considering alot of learning already for GCP, this was a tradeoff
- dbt Freshness Checks - but data could be techincally the same as previous report Tom has confirmed!!

Yes — in many banking/reporting systems, a simple scheduled DAG is enough if the business process guarantees the data is finalized by a known reporting window.



Source load finishes
    ↓
Publishes event/message
    ↓
Triggers Airflow DAG

- 




### Design 
- Currently FDP is updated by upstream data from ODP - surely no update happens until the fresh load of ODP? Therefore could use DBT freshness?

- 
