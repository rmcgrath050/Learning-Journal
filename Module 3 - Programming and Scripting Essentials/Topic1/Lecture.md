

## Distros

- The distros share the same Linux kernel (core system)
- Open-source code allows for easy bug review and fast issue resolution
- The distros share the same access model. Clear distinction between regular users and root enhances security
- sudo grants temporary privileges, reducing accidental changes
<br>
<br>

<img width="728" height="480" alt="image" src="https://github.com/user-attachments/assets/bce1134c-6f4e-4244-8048-15a76f0453ec" />
<br>
- can have a play with difffernet distros to see what u prefer!

## Understanding the Linux filesystem
/ - forward lash to go into root 

- Directories contain sub directories
- Can be an ordinary file, a directory (folder), a device or a link (pointer to other file)
  
## Special filesystem directories
-  /etc - Configuration Files - The /etc directory contains all the system-wide configuration files and shell scripts that are used to boot             and initialise system settings. This is where system administrators can configure the system's behaviour.
-  /dev – Devices
-   tmp – Temporary Files
-   /mnt – Mount Directory 
➢ /mnt – Mount Directory (like a cdrom , hard drive, floppy disc etc)
- /home - The /home directory is the default location for users' personal directories
- - /user - The /usr directory contains user utilities and applications that are not essential for the system to boot or operate in single-              user mode.



#### What Single-User Mode Is

Single-user mode is a minimal environment used for:
- System repair
- Password recovery
- File system checks
- Fixing boot problems

In this mode:
- Only the root user is active
- Networking is usually disabled
- Only the minimum required system programs are loaded
- The root filesystem is often mounted read-only

<b>user binaries:</b> <br>
These are all just programs stored as executable files (called binaries because the computer reads them in binary form).

## Commands

- /bin – User Binaries, binary executables eg  ps, ls, ping, grep, cp
- /sbin – System Binaries, eg iptables, reboot, fdisk, ifconfig
- /var – Variable Files. Content of the files that are expected to grow can be found under this directory eg ystem log files (/var/log);        packages and database files (/var/lib); emails (/var/mail); print queues (/var/spool); lock files (/var/lock); temp files needed across      reboots (/var/tmp)
- /boot – Boot Loader Files , uploading whatever we need
- /usr vs /home. /usr was where the home directories of the users were placed (that is to say, /usr/someone was then the directory now known    as /home/someone. So bascially on newer versions known as home!
- /opt – Optional add-on Applications
- /var (varaiable data) - The /var directory holds variable data files that are expected to grow in size over time. This includes system          logs, user data files, caches, and other transient and dynamic files. Purpose = store data that changes frequently, ensuring that the         filesystem layout is organised and prevents / from being cluttered with variable data.


<br>
<br>

<img width="736" height="716" alt="image" src="https://github.com/user-attachments/assets/a955f8c9-d8b8-440e-a82c-babcf3349968" />

<br>

- Remember /dev controls devices such as hard drvies
- /mnt owuld be relevant when importing additional storgae devices (external media )
- Rememer Linux also is case sensentive


<img width="710" height="356" alt="image" src="https://github.com/user-attachments/assets/b88c3c5e-ba22-4856-a560-481a571b11ab" />

### Key File Operations

Essential file operations include creating, deleting, moving, and copying files and directories. Mastering file operations is fundamental for automating data engineering workflows. In this section, we will explore key file operations that empower data engineers to automate workflows efficiently. This will include the following commands: touch, rm, mv, cp.

- The touch command is used to create an empty file or update the timestamp of an existing file.
- The rm command is used to remove files or directories. When applied to files, it deletes them permanently
- The mv command is used to move or rename files and directories.
- The cp command is used to copy files and directories. It creates a duplicate of the specified file or directory in the target location,      preserving the original. With appropriate options, it can also copy directories recursively.


In the next lesson, we will delve into the powerful capabilities Linux offers data engineers. 
From scripting to automation, we will unlock the tools you need for seamless data management! 


## Lession 3 - Key Linux utilities for data engineers

Utilities for manipulating and analysing text files, include tools such as grep, sed, and awk.
These tools are vital for parsing log files, transforming data, and extracting insights. Here is a brief overview of these tools: 

- Global regular expression print (grep): These search for patterns within files.
- Stream editor (sed): The stream editor is used for modifying file content
- awk: This is used for pattern scanning and processing language

Grep, for example, is integral to system administration toolkit, allows to search through massive log files for specific patterns that indicate errors or anomalies. Could search log files for common error keywords such as "error," "fail," and "exception." 

- To search for the keyword "error" in a log file named application.log, you would use: grep "error" application.log
- To search for "error" in a case-insensitive manner, which also captures "Error" and "ERROR": grep -i "error" application.log
- Search for multiple key words - grep -E "error|fail|exception" application.log
- Contextual Search, To display lines containing "error" along with 2 lines of context before and after each match:<i>grep -C 2 "error"       application.log</i>
- To count the number of lines that match the keyword "error": grep -c "error" application.log
- To display line numbers along with matching lines: grep -n "error" application.log

Data transfer and compression

Efficient data transfer and compression are crucial for managing large datasets across different systems. Tools for transferring and compressing data, such as rsync, scp, tar, and gzip. 
Explanation and examples include the following:
- rsync: Synchronizes files and directories between two locations
- tar and gzip: Archiving and compressing files

## Lession 4 - Job scheduling and automation

Often, we find ourselves dealing with repetitive tasks—such as data backups, ETL (Extract, Transform, Load) processes, and system maintenance—that need to be executed reliably and efficiently. This is where job scheduling and automation come into play.

<b>Why is this important? </b>
- Efficiency: Automating routine tasks frees up valuable time and allows us to focus on more complex challenges.
- Timeliness: Ensuring that critical processes run at specific times or intervals is essential for meeting deadlines and maintaining data     pipelines.

<br>
<br>
  <img width="912" height="588" alt="image" src="https://github.com/user-attachments/assets/dc9308f7-ce10-4ff3-9269-82e8d096d575"/>

### Technical Appliations of CRON
- Scheduling data backups: Automating regular backups of databases, files, or other critical data.
- Extract, transform, load (ETL) processes: Running data extraction, transformation, and loading tasks at specific intervals.
- System maintenance tasks: Performing system cleanup, log rotation, or other maintenance activities automatically.


      Airbnb uses sophisticated scheduling systems to manage its data pipeline jobs, ensuring timely data processing and reporting. 
      A critical component of this scheduling involves tools like Apache Airflow for orchestrating complex workflows. 
      These tools allow Airbnb to define, schedule, and monitor various tasks, ensuring data is processed accurately and on time.


1. In addition to advanced orchestration tools, Airbnb also uses cron, a standard Unix-like operating system utility, to schedule tasks.
2. These jobs are defined in the crontab (cron table) file.
3. crontab is a command-line utility used to schedule cron jobs. Each user can have their own crontab file, and there is also a system-wide crontab for tasks that need to be run by the system.

<img width="750" height="368" alt="image" src="https://github.com/user-attachments/assets/f5907356-a729-410f-9b0b-65ce13cc6cfc" />
<br>
<br>
<img width="762" height="260" alt="image" src="https://github.com/user-attachments/assets/6ae17cb0-27bc-496d-98ae-33fd63e060e6" />


4. To submit a cron job, you edit the crontab file by running: <i>crontab -e </i> : This opens the user's crontab file in a text editor,        where you can add, remove, or edit cron jobs.

Creating and executing scripts is a fundamental aspect of automating tasks in Linux. Scripting is essential for automating complex workflows and reducing manual intervention. 
<br>
Shell scripts are text files containing a series of commands executed by the shell. Scripts, typically saved with a .sh extension, contain a series of commands that the shell executes.


#### Redirection Operators
<br>

<img width="762" height="582" alt="image" src="https://github.com/user-attachments/assets/d55a717b-0118-4f58-ba34-8ebe431d2e9e"/>

<br>
Similar to redirects, pipes (|) are used in Unix-like systems to pass the output of one command as the input to another. 
Cron jobs are specifically designed for scheduling tasks to run periodically at specified intervals. 


## Lession 5: Advanced text processing and log management

- Global regular expression print (Grep) is a versatile tool that allows you to search for patterns, extract relevant information, and        manipulate text effortlessly
- Log management plays a pivotal role in maintaining system health, diagnosing issues, and ensuring compliance.
- Which Grep option inverts the match to exclude certain patterns? The -v option inverts the match, excluding specific patterns.


## Lession 6: Summary 

- Linux offers several utilities for data engineers. You can connect commands using pipes (|) to filter data, transform it, and channel it where needed

- Text processing tools like grep, sed, and awk are your Swiss Army knives. They allow you to slice, dice, and manipulate text like a pro

- Linux allows you to schedule tasks with precision. You can automate backups, ETL processes, and system maintenance using cron jobs

- Linux offers advanced text processing and log management tools. With grep, you can search, extract, and manipulate text effortlessly. You can detect patterns, filter logs, and count occurrences

- Log management in Linux allows you to manage logs like a seasoned wizard. You can understand log structures, monitor in real-time, and automate rotation
