
# Storing and querying data 

21/10/25

Don't have to instal data management software, with SQL lite. (Prebuild into command line).
Keeping things localised this way , can build connections to this neat SQL lite Package. However doesnt have the same natural way of partitioning the data
A lot of data we deal with is in structured format. 

## On Prem 
Pros - not tied into vendor, in charge of our equipment, good for confidential data
Cons - cost, support, limited accessibility, slow to scale 

## Data storage options

<img width="692" height="428" alt="image" src="https://github.com/user-attachments/assets/aaa6674b-90e3-4879-87a9-4948cb7dfa45" />

<br>
<br>

**add some notes here 20 mins in!!

<br> 

NoSQL - jsut means we dont only use SQL, use of other languages may be included

#### Powershell
- ls - to list folders
- d- means directory 
- cd - change directory 
- pwd - find path
- cd.. - go back
- mv - move files around
- rm - rename (i think) 


<img width="692" height="428"  alt="image" src="https://github.com/user-attachments/assets/2bc1474c-b5f4-4512-ad78-dab71f01bf1e" />
<br>
<br>
Pipe represents taking items from previous query and putting it into next 

Bash is like the command prompt (shell) of linux, can access the windows powershell CMD by searching on windows for 'Windows Powershell (x86)'

### Binary 

Binary files works in 8 digits which is 8 bits/ 1 byte 

<img width="692" height="428" alt="image" src="https://github.com/user-attachments/assets/1c47f374-cd13-4d54-ab92-13b60703161a" />
<br>

<img width="692" height="428" alt="image" src="https://github.com/user-attachments/assets/cdca74fd-b542-48ff-9926-4375ec50afb3" />
<br>
<br>


## MIME Types

A MIME type is a label used to identify a type of data. It is used so software can know how to handle the data. It serves the same purpose on the 
Internet that file extensions do on Microsoft Windows.

So if a server says "This is text/html" the client can go "Ah, this is an HTML document, I can render that internally", 
while if the server says "This is application/pdf" the client can go "Ah, I need to launch the FoxIt PDF Reader
plugin that the user has installed and that has registered itself as the application/pdf handler."


## From files to databases

- Files get messy
- A filesystem is not the most efficient structure for querying data
- Databases are a structured way of querying data


## Cloud Storage

<img width="692" height="428" alt="image" src="https://github.com/user-attachments/assets/99feeb95-f5fd-4344-8730-6d75a1a7c016" />
<br>
<br>
<b>Block storage </b>- stored data in chunks , good for databases <br>
<b>Object storage </b>-- objects, metadata, unique identifier 
<br>

### Cloud storage has evolved

Mainly focused on storage, however during the cloud transition era it was common to talk about Data Lakes. 
Post 2025 this evolved into data lakehouses , which benefit both from lakes and warehouses 

<img width="692" height="428" alt="image" src="https://github.com/user-attachments/assets/e5491c81-7b2d-4932-9f7c-cc3e2b1ed2b0" />
<br>
<br>


## Data Model

Consists of three parts:
- Structure of the data – what does it look like
- Operations on the data – what's available
- Constraints on the data – what's allowed


Components/tables are called entities, columns are attributes 

**Can relate about diving into SQL and not learning key concepts in working world! :) 

<img width="692" height="428" alt="image" src="https://github.com/user-attachments/assets/87b6d62e-f23d-4cd9-a9a3-ed4a4cca9b15" />
<br>
<br>

VARCHAR can have a character limit, while TEXT does not.
The main difference is that Char stores fixed-length character strings (storage), and Varchar stores character strings of variable lengths.


 ---domains/ data types -- CHECK diff here! edit!!!

<b>ON_CONFLICT </b> - SQL ignores duplicate rows and continues to insert into table ignoring these! 

automatic triggers- explore this in homework :) 
shadowing - talk though working, 


