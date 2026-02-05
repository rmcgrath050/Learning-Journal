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




