## Assessment possible questions

- 7:1 How did you approach event driven data collection? 


#### "Can you explain the principles of descriptive, predictive and prescriptive analytics and how they apply to your role?"

Descriptive → What happened?
Predictive → What might happen?
Prescriptive → What should we do?

The three types can be viewed as different levels of analytical decision-making. Descriptive analytics looks at what has happened, predictive analytics looks at what is likely to happen, and prescriptive analytics looks at what action should be taken.
In my role, the strongest example is descriptive analytics because I work extensively with batch reporting. For example, I use SQL to analyse completed or running processes, task statuses, file counts and outputs. During my LPI migration, I established a baseline of the tasks sending files to the existing location and then used SQL and Excel to validate the results after the changes. This helped me understand what had happened and whether the expected processing had occurred.
Predictive analytics would use historical data to identify patterns and estimate future outcomes. For example, historical operational data could potentially be used to predict whether a process is likely to fail or what future reporting demand might look like.
Prescriptive analytics goes another step further by recommending what should be done based on the analysis. For example, if a model predicted that a process was likely to fail, a prescriptive system could recommend or automatically initiate an appropriate action.
So, while my day-to-day batch reporting is primarily descriptive, I understand how descriptive reporting can provide the data and insight that supports predictive and prescriptive decision-making further up the analytical process."


10,000 files processed

↓ Descriptive
"10,000 files were processed yesterday, with 98% successfully completed."
↓
Predictive
"Based on historical volumes, approximately 12,000 files are expected tomorrow."
↓
Prescriptive
"Based on the expected volume and current processing capacity, an additional processing window should be scheduled."

“I designed a pipeline that ingests 500k daily transaction records into a SQL data store with a 20% reduction rate in duplicates. I will discuss how duplicate transactions and inconsistent formats were handled via SQL/ Python transformation layers. This met the SLA for near-real-time reporting. I evaluated a reporting  but discounted it due to unnecessary cost. From this I learned how to optimise batch ingestion and justify design trade-offs.”


