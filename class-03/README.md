# Network Segmentation

## Overview

By designing a network to control how traffic flows among its parts, we can achieve network segmentation. Benefits of segmentation include improvements to operational performance, reduction of cyber attack surface, additional protection for vulnerable devices, and a reduction in scope of regulatory compliance. Today you will practice designing a network to achieve a specified segmentation requirement.

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

- Subnet
  - short for subnetworks
  - used to divide a larger network into smaller, more manageable sub-networks or segments
- Subnet mask/netmask
  - a 32-bit number that is used to divide an IP address into network and host portions.
  - used in conjunction with the IP address to determine which part of the address identifies the network and which part identifies the host.
- CIDR
  - Classless Inter-Domain Routing
  - a method of IP address allocation and route aggregation used in Internet Protocol (IP) networking.
- CIDR block notation
  - also known as CIDR notation
  - A CIDR block is a range of IP addresses that have been assigned to a network or organization, and is represented by an IP address and a number that indicates the size of the block.
  - is a way of representing a network address and its associated subnet mask as a single value
  - allows for a more flexible allocation of IP addresses and more efficient use of available address space, which is especially important in today's internet, where IPv4 addresses are becoming scarce.
- Network address
  - is a unique identifier that is assigned to a network or subnet within an IP network. It is used to identify the specific network to which a device belongs and to route packets of data to the correct destination.
- Network segmentation
  - Logical segmentation is a virtual division of the network that separates traffic based on criteria such as IP addresses, protocols, or applications. Logical segmentation is achieved through network devices like routers, switches, and firewalls, which can be configured to route traffic between different logical segments. Logical segmentation allows for more granular control over traffic flows and can improve network security by isolating sensitive or critical resources from the rest of the network.
  - Physical segmentation, on the other hand, involves physically separating the network into different parts using devices such as switches or routers. Physical segmentation can be achieved by physically isolating devices or by connecting them to different network devices that are not connected to each other. Physical segmentation is often used to improve network performance by reducing network congestion and increasing network availability.
- Interface 
  - is a physical or logical connection point on a router where data can be sent or received. The number and type of interfaces a router has will vary depending on the model and purpose of the router
- Microsegmentation is a security technique that involves dividing a network into smaller, logical segments, and applying security policies to each segment. Each segment is isolated from other segments, and access to resources within the segment is strictly controlled based on the policies that have been set.
- Virtual LANs (VLANs)
  - Virtual Local Area Network is a logical grouping of devices on a network, regardless of their physical location. VLANs allow network administrators to group devices together based on their function, department, or other criteria, rather than their physical location or connection to a specific switch or router.
  - With VLANs, devices can communicate with each other as if they were on the same physical network, even if they are located in different parts of a building or on different floors.

#### Notes

1. What does the final digit after the “/” represent in an IPv4 address?
  - An IPv4 address is made up of 4 octets (8-bit binary numbers) separated by periods, for a total of 32 bits. Each octet can represent a decimal value between 0 and 255, inclusive. So, an example of an IPv4 address would be 192.0.2.1, where 192, 0, 2, and 1 are the decimal values of the four octets.

#### Execute

- Configure isolated subnets using VLANs and ASA Firewall in Packet Tracer

## Helpful Resources

  - [Subnet Practice](https://subnetipv4.com/){:target="_blank"}
  - [Subnetting Implementation in Cisco Packet Tracer](https://www.geeksforgeeks.org/subnetting-implementation-in-cisco-packet-tracer/){:target="_blank"}
  - [What is VLAN?](https://www.guru99.com/vlan-definition-types-advantages.html#9){:target="_blank"}
  - [Configuring VLANs and Trunking](https://sites.radford.edu/~hlee3/classes/backup/itec451_spring2017/Cisco/CCNA2_RSE_spring2017/Lab%20Source%20Files_solutions/6.2.2.5%20Lab%20-%20Configuring%20VLANs%20and%20Trunking%20-%20solution.pdf){:target="_blank"}
  - [Basic VLAN Configuration](https://courses.cs.ut.ee/2012/NT/juh/3_1.pdf){:target="_blank"}

### CompTIA Flash Cards

- Which WAN technology uses 32 64 Kbps channels?
  - E1
- Which two protocols allow secure access to a VPN?
  - PPTP and IPSec
- What is the version or name of OSPF that is used with IPv6?
  - OSPFv3
- A network device that is used to connect multiple devices without segmenting a network is a ___________________.
  - Hub
- True/False: SDSL means that your download and upload speeds on the line are different.
  - False
- The following output is from what diagnostic tool?
```
Router 1 (192.162.0.1) 2.0 ms 1.0 ms 2.0 ms
Server.net.com(4.150.6.3) 18.0 ms 12.0 ms 32.0ms
Lammle.com (2.12.14.1) 240 ms 120 ms 300 ms
```
  - traceroute/tracert
- What is a security zone that allows public traffic but is isolated from the private network called?
  - Screened subnet or DMZ
