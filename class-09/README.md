# Traffic Mirroring

## Overview

Configuring the network for optimal visibility by security tools is essential in the modern era. One method involves duplicating or "mirroring" network traffic to a sniffing tool. This allows the tool to see all traffic passing through the mirrored interface.

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

- Span port
- Interface bridge
- Traffic mirroring
- Sniffing

#### Execute

- Configure traffic mirroring on pfSense 
- Use Wireshark to capture network traffic

## Helpful Resources

- [pfSense Docs - Interface Bridges](https://pfsense-docs.readthedocs.io/en/latest/interfaces/interface-bridges.html)

## CompTIA Questions
- You have an interface on a router with the IP address of 192.168.192.10/29. What is the broadcast address the hosts will use on this LAN?
  - A /29 (255.255.255.248) has a block size of 8 in the fourth octet. This means the subnets are 0, 8, 16, 24, and so on. 10 is in the 8 subnet. The next subnet is 16, so 15 is the broadcast address.
- Which layer of the OSI model provides an entry point for programs to access the network infrastructure?
  - The top layer of the OSI model gives applications access to the services that allow network access.
- What does the `nbtstat -R` utility switch do?
  - To purge and reload the remote NetBIOS name cache, you must use nbtstat -R. Remember that the R must be uppercase, and it will not work correctly without the hyphen.
- If a switch receives a frame and the destination hardware address is not in the forward/filter table, what will the switch do with this frame?
  - If a frame is received on a switch and the destination hardware address is not in the forward/filter table (also called the MAC address table), the frame will be forwarded out all ports except the port on which it was received.
- You have a Class A host of 10.0.0.110/25. It needs to communicate to a host with an IP address of 10.0.0.210/25. Which of the following devices do you need to use in order for these hosts to communicate?
  - Don’t freak because this is a Class A. What is your subnet mask? 255.255.255.128. Regardless of the class of address, this is a block size of 128 in the fourth octet. The subnets are 0 and 128. The 0 subnet host range is 1–126, with a broadcast address of 127. The 128 subnet host range is 129–254, with a broadcast address of 255. You need a router for these two hosts to communicate because they are in different subnets.
