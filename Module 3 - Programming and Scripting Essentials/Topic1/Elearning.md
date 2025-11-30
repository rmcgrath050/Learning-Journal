# Lession 3.1 Linux for Data Engineers

- Its an open source operating system
- X known as twitter uses Linux for massive data infrastructure
- <b>Data Driven Enterprise:</b> to help leverage vast amounts of data to make informed decisions and drive business strategies
- <b>Stability and reliability:</b> Data infrastucture must be robust, scable and secure to support its global user base and real time data processing needs
- <b>Secuirty and Privacy</b>: Linux secuirty features are crutical for protecting customer Data and maintaining privacy. Open source nature alows engineers to custom the system optimising it for their specific needs. Also allows developers to scruntinise code to discover vulnerabilities more easily 


### CLI 

- The command line interface (CLI) also known as hell in Linux plays a vital role in data manipulation and system monitoring.
- The shell is a powerful tool that allowes users to interact directly with OS with text-based commands
- <b>Data processing:</b> Engineers use CLI tools to process raw data with commands such as GREP, AWK, and SED help in filtering and transforming data, which is essential for extracting meaningful information from vast datasets.
- <b>System monitoring:</b> Monitoring the health and performance of computational clusters is critical. CLI tools like top, htop, and dstat provide real-time insights into system resource usage, helping engineers to maintain system stability and performance.
- <b>Automation:</b>Key to handling repetivite tasks and managing complex workloads


### Flexibility 

Flexibility is also a hallmark of Linux. It can be customised to meet specific needs, making it a versatile choice for various applications. From lightweight installations suitable for embedded systems to robust configurations designed for high-performance computing, Linux adapts to diverse requirements. This flexibility extends to the wide range of distributions available, such as Ubuntu, CentOS, and Debian, each offering unique features tailored to different use cases. 
Linux's compatibility with tools like Hadoop, Apache Spark, and TensorFlow makes it an invaluable asset in the data engineer's toolkit.


### Linux system structure

The structure of a Linux system includes the kernel, system libraries, system utilities, and application programs.

<img width="732" height="404" alt="image" src="https://github.com/user-attachments/assets/ebe4a3ec-f417-45cf-9b07-df14e4d35885" />
<br>

### Unpacking these terms:

- Kernel: The core part of Linux that manages system resources, such as drivers and power usage
- Shell: The interface that allows users to interact with the kernel and with user programs/applications
- Technical application: For example Using the terminal to execute commands


## Lession 2: Navigating the Linux filesystem

Imagine a world without a logical structure—a chaotic jumble of data strewn across storage devices. To address this, we turn to the filesystem hierarchy standard (FHS), a set of conventions that govern the layout of Unix-like systems.
Knowing FHS helps data engineers locate files and directories necessary for data processing tasks. 

### Unpacking FHS

Every general-purpose computer needs to store data of various types on a hard disk drive (HDD) or something equivalent. There are a couple reasons for this, but mostly because RAM loses its contents when the computer is switched off. 
here are non-volatile types of RAM that can maintain the data stored there after power is removed but they are pretty expensive. Therefore, we need a logical method of organising and storing large amounts of information in a way that makes it easy to manage. 

<br>

<img width="640" height="486" alt="image" src="https://github.com/user-attachments/assets/15aec409-a43b-4d71-ad11-beab8b983f52" />

<br>
- All data in Unix is organised into files. All files are organised into directories. These directories are organised into a tree-like
  structure called the “Filesystem”.
- The filesystem hierarchy standard (FHS) is a reference describing the conventions used for the layout of Unix-like systems.
- It has been made popular by its use in Linux distributions, but it is used by other Unix-like systems as well. It is maintained by the       Linux Foundation.


Lessions continued on Lecture notes.... 


