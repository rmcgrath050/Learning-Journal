## Consider the architecture, performance, isolation, scalability, and overhead.

### When would you use containers?

When scalability, portability and speed are desired
CI/DV Pipelines, for example using containers to run code and test, could use containers to imitate the testing/production servers 
Ideal for distributed, cloud-native applications
Minimal overhead: shared kernel + lightweight runtime significantly reduce storage, memory, and CPU use


### When would you use virtual machines?

Legacy software systems, old financial systems that require a specific version of OS cannot be put into a container 
Financial or healthcare sectors could hold highly confidential data - data isolated on a virtual machine would be better to meet compliance as Virtual machines provide strong isolation at the hardware and operating system level, which improves security
Resource intensive workloads, such as enterprise applications would work better on a virtual machine , as can offer better performance consistency because they can be allocated dedicated CPU, RAM, and storage resources rather than sharing them with other workloads.
