## Notes on activity from last week 

#### Stakeholder Q&A


Brian's Questions (but everyone can benefit as they were good questions) 

1. Should the password be masked in the DB?
firstly, wat is your instinct? and why?
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

Melanie's Questions - Topic 3
1. Gender
 a value for 'prefer not to say', separate from missing? 
That's a sharp observation. 'Prefer not to say' is an answer; missing data is the absence of one. Good modelling keeps them distinct. This file doesn't contain it (only 0/1), so it's not today's job, but note it in your design. That's exactly the 'prepare for future formats' kind of thinking you want

2. 
Salary, all annual, or can frequency vary?
Treat them as annual,there's no pay-frequency column in the file, 

so they're all on the same basis (figures like $27,000 up to $170,900 read as annual)

note: notice the pattern: just like currency, an amount is meaningless without its period. If a future file mixed annual and monthly with no marker, what would you need to add?

3. Education 
 confirmed US-RQF mapping?
Yes, there's an agreed mapping - High School Diploma - A level (RQF 3), Foundation - HND (5), Bachelor - degree (6), Master's -7, Doctorate - 8. Use it But watch: your file also contains Associate Degree, and that one isn't on the standard table. When you hit it, don't guess silently - flag it and reason where it sits. That gap is deliberate

4. DOBs: all MM/DD, or does it vary? 
Inside the US file they're consistent: all month-first US style, e.g. 11/23/01. The catch isn't variation within the file; it's that the UK and France are day-first. So your parser has to know which country it's readin-same field, different rule on the way in. And one more: look at 6/5/45 with age 79: a two-digit year is ambiguous on the century. What other column tells you it's 1945, not 2045?

### Melanie's Scottish questions

2. How do SCQF levels map to RQF levels? Scotland runs its own qualifications framework, SCQF, and it does not line up one-to-one with the RQF that England, Wales and Northern Ireland use: the level numbers don't even match, so an SCQF level and an RQF level with the same number are not the same thing. There are broad equivalences published, but they're approximate, not a clean lookup. 

So my question back to you: if the two frameworks don't map cleanly, what does that mean for how you store education? Do you force Scottish qualifications into your existing RQF field and lose information: or does your schema need to hold the framework and the level? 

4. Invalid email handling - some spaces in the data, should we correct (assuming spaces should be removed), or flag somehow?
5. DOB ambiguity - data presents as DD/MM/YY - are we safe to use age to derive century like with French data?
   
