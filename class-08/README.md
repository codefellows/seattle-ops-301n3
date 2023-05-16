# RADIUS Authentication

## Overview

RADIUS (Remote Authentication Dial-In User Service) is a network management protocol facilitating AAA (Authentication, Authorization, and Accounting) management for network users. In this type of configuration, the NAS (Network Access Server) brokers authentication requests and acts as the network's gatekeeper.

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

- TACACS+
- RADIUS
- AAA
- NAS
- NAC
- Network level authentication

#### Execute

- Deploy wired network authentication

## Helpful Resources

- [How to Set Up a Radius Server on pfSense](https://turbofuture.com/internet/How-to-Set-Up-a-Radius-Server-on-pfSense-Using-the-FreeRadius-Package)
- [Professor Messer - TACACS and RADIUS](https://www.professormesser.com/network-plus/n10-006/tacacs-and-radius/)


## CompTIA Questions

- You connect a host to a switch port, but the new host cannot log into the server that is plugged into the same switch. What could the problem be?
  - The best answers are that the VLAN membership for the port is configured incorrectly and that STP shut down the port.
- In which of the following does the attacker (and his bots) send a small spoofed 8-byte UDP packet to vulnerable NTP servers that requests a large amount of data (megabytes worth of traffic) be sent to the DDoS’s target IP address?
  - The attackers use the monlist command, a remote command in older versions of NTP, that sends the requester a list of the last 600 hosts who have connected to that server. This attack can be prevented by using at least NTP version 4.2.7 (which was released in 2010).
- Which wireless LAN design ensures that a mobile wireless client will not lose connectivity when moving from one access point to another (roaming)?
  - If you are running an extended service set (meaning more than one AP with the same SSID), you need to overlap the cell coverage by 10 percent or more so clients will not drop out while roaming.
- How many bits is a MAC address?
  - A MAC, or hardware, address is a 48-bit (6-byte) address written in hexadecimal format.
- You have multiple departments all connected to switches, with crossover cables connecting the switches together. However, response time on the network is still very slow even though you have upgraded from hubs to switches. What technology should you implement to improve response time on the networks?
  - Switches break up collision domains by default, but the network is still one large broadcast domain. In order to break up broadcast domains in a layer 2 switched network, you need to create virtual LANs.
- Why use a proxy server in your network?
  - A proxy server is basically a type of server that handles its client-machine requests by forwarding them on to other servers while allowing granular control over the traffic between the local LAN and the Internet.