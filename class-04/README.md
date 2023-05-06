# Routing

## Overview

Enterprise network administrators use routing skills to handle large and complex multi-router topologies or connections. ISP backbone routers can and do malfunction on occasion, causing routing problems for everyday users. Routing issues can also arise when configuring VPN tunnelling between two complex LANs.

Routing is a fundamental mechanic in the overall operations of not only networks but the internet at large. In today's lab you'll practice configuring BGP on two routers.

## Class Outline

- Course Overview
- Review Previous Lab
- Review Previous Ops Challenge
- Demo Today's Ops Challenge
- Lecture Today's Lab Topic
- Demo Today's Lab Topic
- Lab

## Learning Objectives

### Students will be able to

#### Describe and Define

- Routing
  - It is the process of selecting the optimal path for data packets to travel from one network to another. It involves determining the most efficient route based on various factors, such as network congestion, available bandwidth, and the cost associated with each possible path.
- Routing protocols are sets of rules and algorithms that routers use to exchange information and make decisions about the best paths for forwarding network traffic. These protocols enable routers to communicate with each other, share network topology information, and update their routing tables accordingly.
  - OSPF (Open Shortest Path First) is a widely used link-state routing protocol that operates within an autonomous system (AS). It is designed to efficiently determine the shortest path for routing packets in IP networks. OSPF is an interior gateway protocol (IGP) and is commonly used in large enterprise networks, ISPs, and the internet backbone.
  - BGP (Border Gateway Protocol) is an exterior gateway protocol (EGP) used for routing between different autonomous systems (ASes) in large-scale networks, such as the internet. BGP is a critical component of the internet's routing infrastructure. It enables ISPs and network operators to exchange routing information, determine optimal paths, and maintain connectivity between autonomous systems.
  - Whats the difference?
    - OSPF is an interior routing protocol used within a single AS to determine the shortest paths for routing packets within a network. BGP, on the other hand, is an exterior routing protocol used to exchange routing information and route packets between different ASes (autonomous systems) in a network, particularly in large-scale environments like the internet.
- Routing table is a data structure stored in a router that contains information about the network topology and the paths to reach different network destinations. It guides the router in making decisions on how to forward incoming packets to their intended destinations.
- Static routing is a method of configuring network routes manually on a router or networking device. In static routing, network administrators manually define and maintain the routes in the router's routing table, specifying the next hop and outgoing interface for each destination network.
  - It can be useful for small networks, point-to-point connections, or specific network segments that require explicit routing paths. However, in larger networks or networks with dynamic changes, dynamic routing protocols like OSPF or BGP are typically preferred for their automatic route updates and adaptability.
- Default routing is a technique used in networking where a router is configured to send all packets with destinations outside of its directly connected networks to a specific router, known as the default gateway or default route.
  - Default routing is a simple and efficient method to handle traffic that does not match any specific routes. It allows routers to forward packets to a predefined gateway without the need for configuring individual routes for every destination. Default routing is widely used to provide internet connectivity to local networks and simplify routing configurations in various networking environments.
- Dynamic routing is a network routing technique in which routers exchange routing information with each other and dynamically update their routing tables based on network changes. Instead of manually configuring routes, dynamic routing protocols automate the process of route discovery, selection, and updates.
  - Dynamic routing provides benefits such as automated route updates, load balancing, redundancy, and the ability to adapt to network changes. It simplifies network administration, as administrators do not need to manually configure routes on each router.
  - However, dynamic routing also introduces additional overhead due to the continuous exchange of routing information and increased processing requirements on routers. It is commonly used in large-scale networks, where the benefits of automation and adaptability outweigh the overhead involved.
- What are the pros and cons of static routing, default routing and dynamic routing?
  - The choice between static routing, default routing, and dynamic routing depends on the specific requirements of the network.
    - Static routing is suitable for small networks with a stable topology.
    - Default routing simplifies routing configurations for non-specific destinations.
    - Dynamic routing offers scalability and adaptability for large and dynamic networks at the cost of increased complexity and overhead.

#### Execute

- Given two networks, configure BGP routing
- Access routing tables on various operating systems

## Helpful Resources

- [Cisco Packet Tracer](https://skillsforall.com/course/getting-started-cisco-packet-tracer){:target="_blank"}
- [Packet Tracer - BGP Configuration](https://www.packettracernetwork.com/tutorials/bgp.html#:~:text=BGP%20in%20Packet%20Tracer,network%20policies%20and%2For%20rulesets.){:target="_blank"}
- [Cisco IOS IP Routing: RIP Command Reference](https://www.cisco.com/c/en/us/td/docs/ios/iproute_rip/command/reference/irr_book/irr_rip.html){:target="_blank"}
- [Static Routing Configuration](https://www.computernetworkingnotes.com/ccna-study-guide/static-routing-configuration-guide-with-examples.html){:target="_blank"}


## CompTIA Questions

- You need to implement wireless but can’t use the 2.4 GHz range because of interference issues. What wireless standard can you implement at the 5 GHz range to get 54 Mbps?
  - 802.11ac
  - The IEEE 802.11a, n, ac, and ax are standards in in the 5 GHz range.
- When all routers in a network agree about the path from one point to another, the network is said to be what?
  - When the routing tables are complete because they include information about all networks in the internetwork, they are considered converged.
- You have a user who cannot resolve names on the local network and the Internet. All other users can do so without difficulty. Although there can be many issues causing this problem, which of the following is a possibility?
  - If you statically add a DNS configuration on a host, it will override the information provided to the host by the DHCP server. By using the ipconfig utility, you can verify that the DNS server addresses are the correct addresses.
- Simple Mail Transfer Protocol works at which layer of the OSI model?
  - HTTP, HTTPS, SMTP, SNMP, Telnet, and FTP, among others, all work at the Application layer of the OSI model.