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
  - Terminal Access Controller Access Control System Plus is a network security protocol that helps control and manage access to devices on a network.
  - It verifies the identity of users, determines their permissions, and keeps track of their network usage.
    - AAA: authentication, authorization, and accounting
  - It offers separate authentication and authorization functions, allowing for more granular control over network access.
  - TACACS+ is commonly used in enterprise environments to manage access to network devices such as routers, switches, and firewalls.

- RADIUS
  - Remote Authentication Dial-In User Service is a networking protocol that provides a way to authenticate and authorize remote users who want to access a network.
  - It's often used by internet service providers and telecommunications companies.
  - RADIUS verifies the user's identity and allows or denies access to the network resources.

- AAA
  - AAA is a framework that ensures secure access to computer systems and networks.
    - Authentication: Verifies the identity of users or devices trying to connect to a network.
    - Authorization: Determines what actions or resources the authenticated users or devices are allowed to access.
    - Accounting: Keeps track of the usage of network resources by authenticated users or devices for auditing and billing purposes.

- NAS
  - Network Access Server is a device like a router or wireless access point that allows remote users to connect to a network.
  - It acts as a gateway and handles the authentication, authorization, and accounting functions for these users.

- NAC
  - Network Access Control technologies and policies are used to enforce security measures on network devices.
  - They ensure that only authorized and safe devices can connect to a network.
  - NAC systems often include features like device authentication, security checks, and control over network access.

- Network level authentication
  - NLA is a security feature used in Windows Remote Desktop Protocol (RDP).
  - It requires users to authenticate themselves before they can access a remote desktop or application.
  - NLA adds an extra layer of security by verifying the user's identity before allowing access, protecting against unauthorized access and potential attacks.

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