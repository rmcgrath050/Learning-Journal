#### Plan

By the end of today you'll be able to:
- Work out which rules actually apply - and why "we're not in the EU" isn't the answer people think it is
- Turn a regulation into an action - and say which requirement justifies it
- Pick the right control for the right failure -not the tool with the best marketing
- Tell a director and an engineer the same bad news - two versions, both true
- Look at a dataset and say what's wrong with it - in language a regulator would recognise

Write a risk report someone acts on - the only kind worth writing
-----------------------------------------------
- What you will have by the end- 
- One finished risk report. Built from a real case study, in your own words. Good practice for your professional discussion.
- Compliance is the proof. Risk reporting is what you write when the proof isn't there!!!!



- GDPR tells you what u owe people
- ISO-21001 gives you the machinery needed to deliver it


** this diagram useful for activity 2:
<br>
<br>
<img width="672" height="572" alt="image" src="https://github.com/user-attachments/assets/446caac4-27fb-4ce6-b22d-3fc659688d9e" />
<br>

<img width="910" height="516" alt="image" src="https://github.com/user-attachments/assets/27e17f7c-c150-4429-a398-721d7ed5c796" />

#### Actvity 4 mapping :

<img width="1716" height="1086" alt="image" src="https://github.com/user-attachments/assets/67c39a2b-c843-4e2f-889a-5ded516a6aa2" />


<br>

### Activity 1 Answer:

1. What are the key compliance standards applicable in this scenario (e.g.,
GDPR, HIPAA, ISO 27001)?
GDPR - Cannot Delete/Access Data - Forms out of date, Transfer of data
HIPPA - Medical Data, Breach notification delayed, Transfer of data
ISO 27001 - Asia no encryption - Possibly the Transfer of data too.

2. How do the standards affect each role’s responsibilities and challenges?
Sophia - Her problem is organisation-wide governance, Different regions have different controls.
Emily - Make sure data is available and PII is not exposed between regions. Additional Training
Rajesh - Responsible for tech security, protect data, implement encryption, data anonymisation. Fix Vulnerabilities
Jake - Update consent forms to standard,

#### upgrade to distinction 
- rajesh should deploy SIEM specifically to close the delayed-breach-notification gap.
- HIPAA requires timely reporting, and you cannot report a breach that you have not detected -
- detection latency as the root cause, not the reporting process.
- The trade-off is alert volume- an under-tuned SIEM in a hospital would generate enough noise so people are going to ignore it. As a result, I'd tune against high-sensitivity access patterns before switiching it on fully 

4. What steps can the team take to align practices across regions while addressing local regulations?
5. How can Global HealthCorp rebuild patient trust and avoid further legal or reputational damage?


