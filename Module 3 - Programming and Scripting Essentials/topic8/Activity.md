## Consider the architecture, performance, isolation, scalability, and overhead.

### When would you use containers?

- When scalability, portability and speed are desired
- CI/DV Pipelines, for example using containers to run code and test, could use containers to imitate the testing/production servers 
- Ideal for distributed, cloud-native applications
- Minimal overhead: shared kernel + lightweight runtime significantly reduce storage, memory, and CPU use
- When you need a lightweight, efficient service. You can create them quickly on demand  i.e. for Black Friday promotions etc when resource    demand is much higher (giving scalability). Ability to run more containers for the same equivalent space/RAM etc a VM uses. 


### When would you use virtual machines?

- Legacy software systems, old financial systems that require a specific version of OS cannot be put into a container
- Financial or healthcare sectors could hold highly confidential data - data isolated on a virtual machine would be better to meet compliance as Virtual machines provide strong isolation at the hardware and operating system level, which improves security
- Resource intensive workloads, such as enterprise applications would work better on a virtual machine , as can offer better performance consistency because they can be allocated dedicated CPU, RAM, and storage resources rather than sharing them with other workloads.
- Virtual machines offer isolation which is ideal for when you need more control over things like security, compliance, data governance etc. They also give you full operating system flexibility, ideal for accommodating legacy software/systems. They're ideal longer running services.


<img width="793" height="519" alt="image" src="https://github.com/user-attachments/assets/89f9b5b0-0e85-4f88-8fc8-7756330c9b7e" />


