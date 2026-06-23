##### Copy of questions:
What does RQF stand for? values 1-8 here 
What do you need this data for?
Are you interested in all columns?
Do you require a history to be retained?
Does NA on the salary mean the person doesn’t have one or we don’t know this persons salary?
Are the favourite questions for secuirty or marketing purposes?
Do you require a history to be retained?

v good questions!
ok so....1 - RQF - u know this, we just dont relate to it as RQF - Regulated Qualifications Framework. 
It's the UK system that classifies qualifications by level  1 through 8 so you can compare them on a like-for-like basis. 
Level 3 is roughly A-level, Level 5 is your apprenticeship
Given it's always going to be one of a fixed set of values 1 to 8 — what does that suggest about how you should store it in your schema?
K3 (normalisation), K15 (schema design), S3 (fit-for-purpose design)

- So answers could include star schema, with dimensions included for futher details on RDF, 

That's the question I was hoping someone would ask. The business wants to do two things. 
- One, run customer segmentation analysis: favourite colour, animal, food, location, demographics : to target marketing campaigns. 
- Two, monitor login activity: understanding active versus dormant users, peak login times, abnormal patterns that might suggest account compromise
- Now: does knowing the purpose change anything about the schema you're designing?
- hint....segmentation....login monitoring.....purpose drives data retention


##### Two different kinds of history matter to us:
1: login history. We want every login event retained for 12 months for security monitoring and audit. That's what the audit CSV is giving you.
Two: user profile history. If a user changes their email, their address, their salary band: we want to know what it used to be, and when it changed. The marketing team wants to track customer movement; 
the compliance team needs it for audit. We don't want a database that quietly forgets the past
2. Now....that second one is the hard one. What does your schema need to look like to remember a user's history, not just their current state?

### Important bit

In this case  the 'na' is 'not applicable'. That's the youngest user in the dataset, an 11-year-old.
They don't have a salary because they don't have a job. It's not that we forgot to record it: it's that there isn't one to record.
but, rosie - you've just identified the most important question in data quality. Because if you treat 'not applicable' and 'unknown' the same way in your schema, you've lost information that the source actually preserved. 
The source went to the trouble of writing 'na' rather than leaving it blank, that's deliberate. What does that tell you?
save these, esp the questions. for your portfolio work!


hi guys, 
- so the RFQ,DOB, salary....
- points on the RHS, which you guys got and asked excellent questions - save these as they are portfolio-worthy. that's why i wanted u to ask the questions


### Conclusion 
- You've used Slowly Changing Dimension Type 2: that's a proper data-warehousing pattern, and it's the right answer for what we asked.
- The marketing and compliance teams will both be able to answer historical questions against this design. Well done, you've used SCD2 for customer profiles AND append-only for login events. 
That's Not a contradiction, that's correct. 
- Different data, different history pattern. That's the maturity step most people miss
- You've spotted that this needs a decision.
- Remember what we worked out about email earlier :can a user share an email? Can they change it? What does that mean for using it as the basis for your surrogate key?
- the data minimisation question. What's the business case for storing them? If the answer is 'segmentation analysis' -they're justified. If the answer is 'just in case' :they're not. What did I tell you the purpose was?
