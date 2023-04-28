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
- Subnet mask/netmask
- CIDR
- CIDR block notation
- Network address
- Network segmentation
  - Logical
  - Physical
- Interface
- Microsegmentation
- Virtual LANs (VLANs)

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
