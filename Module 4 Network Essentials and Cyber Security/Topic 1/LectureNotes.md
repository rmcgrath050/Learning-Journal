# Introduction to Networks

- Networking talking and listening though protocols, what language we speaking, make sure its a secure and making sure its targeted , 

## Basic Principles of networks
- routing and switching 
- security applications and firewalls
- wireless 
- VoIP and unified Communications

## Tools needed for networking
- hub (Too open for large business) 
- switch (Mainly used in large businesses, groups devices together like a middleman , distributes data, helps with collision domain , connects devices on same network) 
- Router (Helps connect one network to another network, uses a gateway ) 
- Firewall (What you allow and don't allow , can configure what traffic you want, etc) 
- VPN Concentrator 


### Networking Models
- Peer to peer (equal , no device is a controller, no centralised admin, all shared, not much security) 
- Client to domain/server ( server is the services client is using, server is the controller, security is key here ) 


## Network Components 
- Topology is a network map 
- IP address is given to you because you are part of a network
- Router will read which network is data coming from and where it needs to go 


#### Class of IP Address
<br>
<img width="466" height="422" alt="image" src="https://github.com/user-attachments/assets/eb7b0320-b0ee-427d-9b40-4a15b2e932cb" />


To look at the class of IP look at first number. This depends on network, number of devices etc. 
A new device announces its presence, and this special address will reach the DHCP. IP addresses are self assigned when the computer asks for an ip address and nobody responds.
- 127.0.0.0 (loopback addresss, used for testing the local TCP/IP installation)


### TCP/ UDP 
- TCP uses the IP address 
- TCP concentrates on how much can be carried at a time, speed, seeks a response , however this can become a bottleneck as it needs a confirmed delivery. 
- UDP assumes you have received it 
- OSI model is how data moves from top to bottom

<br>
<img width="396" height="354" alt="image" src="https://github.com/user-attachments/assets/7a8445d4-2a3b-4ba7-8503-18a4d9f3adcc" />
<br>
<br>
These layers are useful for troubleshooting and works from 7 down to physical level 
Encapsulation happens at level 2. 


<img width="534" height="278" alt="image" src="https://github.com/user-attachments/assets/c53c799f-abf2-429b-9ef6-aaae4f172e13" />

<br>
<br>

## Lan Infrastructure Architecture

We are all access here, so the distribution is the storage 
and the core is the backbone of the entire network. 
We are tapping into the data centre (cloud- AWS, Azure, GCP ) and from here we have all the users. 

The two tier system has distribution and core combined. Small businesses would use this.
 
## Data centre Equipment

<img width="488" height="502" alt="image" src="https://github.com/user-attachments/assets/fa61ca0a-a06c-483f-8617-b29f072ed350" />

## Disturbed Architecture

<img width="730" height="502" alt="image" src="https://github.com/user-attachments/assets/afbc06b0-7935-4e85-bc40-714598cf28aa" />

This is known as a cluster. 
CPU will work to best of its strength so sometimes could crash. So how do we know its capacity? of course by the memory. With big data there is continuous flow of data. How do we know the breakpoint? That's how distribution begins. Master node recruits as many workers in a cluster, and coordinates the load amongst workers. When one of the workers is not available , another worker is on standby to receive this. 

The master gives the task based on the capacity of the worker.
<br>
<br>

<img width="590" height="416" alt="image" src="https://github.com/user-attachments/assets/77496f64-378e-4220-9f3f-b41370ab7129"/>

The master gives the task based on the capacity of the worker.

Metadata ensures all servers know everything going on. Clients will not know this. The failover controller (another server) monitors status of traffic and will assign server 2 if any issues. Syncity amongst all of them. 

## DMZ
DMZ is a system to separate the distribution from the access layer, acts as a barrier. Can position it between lan and core. Can also position it with the router, two options! This protects core and protects distribution.

Distribution means we have a cluster of computers working together (servers and workers). High availability is important 

## Network Segmentation
Can not put everything in one area! Subnet masks are used.
Helps traffic move quicker on a network and if not broken down in segments , security risk is higher. 
Network can ensure bandwidth is increased in these segments. 












