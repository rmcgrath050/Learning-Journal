## Notes on activity from last week 

Stakeholder Q&A

Brian's Questions (but everyone can benefit as they were good questions) 

1. Should the password be masked in the DB?
firstly, what is your instinct? and why?
Imagine this leaking, are you comfortable that the column is readable? 

mask, encrypt, hash

2. Is salary annual or does the frequency vary?
good, you're not assuming the unit. The French figures are per calendar month. So if some sources are monthly, and others are annual, what do you have to store so a report never compares a monthly figure against an annual one by accident?
(capture the period (and currency) as an indicator; normailise at report time, don't silently mix

3. In the UK, what does the RQF firld represent? 
 Regulated Qualifications Framework - UK's scale for levels of qualificaition. 
eg: Level 5 is this apprenticeship 

the thing you need to consider....how do you get the French BAC+ values onto that same scale so both countries are comparable

4. Age since last birthday', verification needed? UK has a DOB in 2025 but age 100.
remember to open the data in pandas or VS code; not Excel 
should a pipeline silently load a record that's internally impossible? What should it do instead?
you want to validate DOB-vs-age agreement,  flag/quarantine the contradictions rather than load them blindly.

you found this one by eye, what can you do to catch it across thousands of rows? this is a validation/monitoring point

5. Gender;  is there a set list / mapping to align UK & FR?
What values are in the French file, and what did you use in Part 1 for the UK? Put those side by side.....where do they line up?? where is the gap??

map the french labels onto the same domain as Part 1

6. Expected DOB format in FR, always dd/mm/yyyy or yy-mm-dd?
look at the actual file, what format do you see in the French DOB column? dont design for a format that isn't there, handle what the data gives you. 
what's the trap with the 2-digit year? 
parse the real format, remember the century problem?? 

7. I presume BAC+ is employment type?
Pause on this one - I want you to check this assumption. Look at the actual values in that column. Licence, Master, Doctorat.....does that seem like employment? This is good to remember when naming columns, to prevent corrupting things like education mapping in this case. Because we need to build mapping on these column names 
