# 5:3 Containers and Orchestration 

- Kubernetes is the container management
- EKS can be used to orchestrate containers
- Packing the app with the envrioment and containers are repeatable self contained environments
- Think of docker like a lunchbox, its a docker image that can be taken to another place, moment its open thats like running the container, the receipe for lunchbox is the docker file.
- Huge time difference between virtual machines and containers - containers for the win!
- Will be making a docker file in lab later!


<img width="555" height="366" alt="image" src="https://github.com/user-attachments/assets/dd365978-406e-477d-a6a2-68bf565f352a" />

<br>
Containers are created from a template called an image!
A container has everything a software application needs to run. 
<br>

- image is like the template and a container is a running instance of this!
- What file do u write to give docker instructions for building an image? Dockerfile! (Receipt card) 


<img width="738" height="600" alt="image" src="https://github.com/user-attachments/assets/6cf1cf94-3655-488b-923d-44230a00e416" />
<br>
Can cause latency issues if this is in differnet buildings/servers!
<br>


Docker engine inside the container area is like the house management! 
<br>

1. A container is a package of lightweight software
2. It solves the problem of overhead expenses and is more efficent to run
3. Different from virtual machine as virtual machine involves more processing power, less easy to manage/ maintain 

#### ECS
- ECS is a passive system , like routing decides where things go.
- Allocates resources eg with capicity
- orchestration brain of it all
- cluster is a combination of containers in EC2 ( empty floor of building)
- Self heals itself to move containers to an available EC2 instance in the same ECS cluster


#### Amazon ECS Cluster Options 
- need to be able to agrue for aor an against approach for different scenarions **EPA
- Amazon ECS customer involves management of docker engines and VM guest operating systems
- With fargate less control but faster to run
- EC2 needs to comply with FCA complaince guidelines,

- 


