# Topic 4 - Databases and Data Lakes

Data profiling
- Database archiving
- Query profiling
- Query optimisation
- Recovery
- Indexing
- Security
- Outages

## Data Profiling

<img width="492" height="344" alt="image" src="https://github.com/user-attachments/assets/024d50a2-ae31-4a61-8b70-d06f3985a96d" />

<br>
<br>
- Have to make the assumption we cant trust data , always assume bad and approach with that angle
- Metadata enriches our understanding, data about data


## Role of Metadata and Data Rules
- Must define what constitutes correct
- Traditional metadata is only part of definition
- Traditional metadata is often inaccurate and/or incomplete
- Data rules exist whether known or not
- Data rules exist whether enforced or not
- Profiling can validate metadata and known data rules
- Can be used to correct or enhance metadata and data rules
- Can be used to discover additional data rules
- Can test adherence to data rules

work example : think of a work example where something has went wrong with data and how it was corrected/resolved, fixes could include fluidatity and adaptability 

<br>
<br>

## why is Data profiling used?
 - Database qulity improvement program, following traditional 6 sigma like program
 - Support consolidation of databases after mergers and acquistions eg two companies combing together
 - Support data integration functions for data warehousing , eg develop processses to clean data in transit

## database Quality Program

3 steps - Discovery, Correction and Prevention 

<img width="766" height="410" alt="image" src="https://github.com/user-attachments/assets/6601e42b-4d73-456e-a86c-56ed77fe8e7c" />

<br>
1. Examples include  - data logic rules changing, etc


## Data profiling Functions

#### Column Examination
- Deterimine true data type - maybe wrong in data dictionary compared to BIX file , or a program like a phtyon program coverted the wrong data type
- encoding patterns eg. UTF-8/UTF-16, anything above is languages with more chars (asian languages etc)

other example include:  
- Row Examination
- Multitable Examination

types of problems can be identified:
- invalid values - can use comparsions to valid etc
- Valid values , too many of one or more values or too few of one or more values
- mutiple ways to express same value


## Data Profiling Functions
- Home grown - directed SQL, manual, easy algorithims , few surprises uncovered
- Vendor tools - includes forgein key discovery, third normal form discovery and more management of results

## why we have data profiling
- cost savings
- improved operations
- risk reduction
- 

