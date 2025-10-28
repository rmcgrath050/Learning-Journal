
## Mod 2 Week 2 - Databases and Data Lakes

<br><b>Recap of assessments: </b> <br>
65 weeks to go though gateway , 12-13 weeks after start gateway when the assessment begins, professional discussion with industry experts and also project report 

- Profillio -  collection of work i have done, start answering questions about your way of working
- formative - take the feedback and put into the profillio piece
- big tasks but less of them
- 3 big tasks and collating that in one big  doc - is the proposed plan! **

**hang fire for now

### Benefits of breaking down Data: <br>
- Speed of exction, optimaisation , redunancy, sustainaility and net 0 goals
- label once, (identifier eg. dim numbers in warehouse)
- lossing valid by being too constrained with data when first looking at data, better going 1nf - 3nf slowly to make sure to retian data

suggogate key - is a dummy placeholder key 

<br>
<br>

<img width="814" height="648" alt="image" src="https://github.com/user-attachments/assets/dcb268d8-06df-4fac-9265-00760a23ff38" />

### OLAP 
- transactions fired into one table, need to ensure its fast eg. taking from ATM and changing customer balance
- busineed oritated

### OLAP 
- analtical , lots of value
- business data warehouse

Best data construct suits who uses the data the most!!!****
<br>
<br>

<img width="814" height="648" alt="image" src="https://github.com/user-attachments/assets/bf9ae959-d7f1-4946-82f7-e2ca14d3cf10" />
<br>
<br>
## Star and Snowflake schemas

<img width="814" height="648" alt="image" src="https://github.com/user-attachments/assets/b5e69633-383f-4609-931d-27530673739c" />
<br>
<br>

### Star Schema
- If you think of a star had points coming out of a central table (Fact table) and then points are dim tables 
- easier to update tables 


### Snowflake Schema
- Snowflake can have table in middle but with links but then linked tables can have further links
- simular to star schema but more dim tables involved! 

****listen back to 40 mins in , choking eposide 


### Data normalisation 
Data normalization is the process of organizing data in a database to reduce redundancy and improve data integrity
- streamlining dtaa to its most simple form 

<img width="814" height="648" alt="image" src="https://github.com/user-attachments/assets/56954f5f-b999-470a-bb19-820e9f929edc" />
<br>
<br>

- figure out your central table / transactional table
- data getting squashed into one column , not normalisation best practise (Column automany)


