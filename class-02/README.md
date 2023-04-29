# Network Scanning with NMAP

## Overview

The network mapping tool Nmap is an open source, command line utility commonly used in network discovery ("enumeration" in offensive terms), security auditing, and pentesting. Nmap can audit whether ports are open or closed on a target host.

Today you will perform a series of basic scanning operations using Nmap and learning more about network ports and protocols. 

## Class Outline

- Course Overview
- Review Previous Lab
- Review Previous Ops Challenge
- Demo Today's Ops Challenge
- Lecture Today's Lab Topic
- Demo Today's Lab Topic
- Lab

## Learning Objectives

- Port and Protocols

### Students will be able to

#### Describe and Define

- Network Enumeration
  - Network Enumeration is the process of gathering information about a computer network or system, such as the number and types of devices on the network, the IP addresses of those devices, and the services and applications running on them.
    - The purpose of network enumeration is to create a map or inventory of the network, which can be used for various purposes, including security auditing, troubleshooting, and network management.
- Nmap
  - Nmap is a network scanner and is used to discover hosts and services on a computer network by sending packets and analyzing the responses.
    - Nmap provides a number of features for probing computer networks, including host discovery and service and operating system detection.
- Service Fingerprinting is the process of identifying the specific types and versions of services or applications running on a network or system by analyzing the responses to network traffic sent to those services or applications.
  - Service fingerprinting is commonly used for security auditing and penetration testing to identify vulnerabilities in services or applications running on a network or system. By identifying the specific types and versions of services or applications running on a network or system, security professionals can determine whether those services or applications have known vulnerabilities or are susceptible to attacks.
- Network port is a communication endpoint in a computer's operating system that is used to identify a specific process or service running on that computer.
- Port scanning looking for ports that are open or closed.
- Protocol analyzers 
  - also known as network analyzers or packet sniffers, are tools used to capture, analyze, and interpret network traffic in real-time. Protocol analyzers allow network administrators and security professionals to monitor network traffic and diagnose network problems, as well as identify and troubleshoot security issues.
  - The Protocol Hierarchy tool in Wireshark is a feature that allows users to view a summary of the protocols used in a network capture. The Protocol Hierarchy tool provides a hierarchical view of all the protocols used in the captured packets, organized by the number of packets and bytes associated with each protocol.
    - To access the Protocol Hierarchy tool in Wireshark, users can navigate to the Statistics menu and select Protocol Hierarchy. The Protocol Hierarchy window displays a table that lists all the protocols detected in the capture, along with the number of packets and bytes associated with each protocol. Users can click on a protocol to expand its details and view additional information, such as the protocol's transport layer, application layer, and specific sub-protocols.
    - [Wireshark Docs on the "Protocol Hierarchy" Window](https://www.wireshark.org/docs/wsug_html_chunked/ChStatHierarchy.html#:~:text=This%20is%20a%20tree%20of,be%20shown%20at%20the%20bottom.)

#### Notes

1. What ports and protocols do I need to know to pass CompTIA Net+?
  - Telnet
  - SSH
  - DNS
  - SMTP
  - HTTP
  - HTTPS
  - RDP
  - Ping

1. What types of protocol are there?
  - ICMP: Internet Control Message Protocol is typically used by network devices, such as routers and switches, to communicate with each other and report errors, such as unreachable destinations, network congestion, or packet loss.
  - UDP: User Datagram Protocol is a connectionless protocol, which means that it does not establish a dedicated end-to-end connection between the sender and receiver before sending data. Instead, it simply sends data packets to the destination address without waiting for an acknowledgement or confirmation of receipt.
  - TCP: Transmission Control Protocol is a connection-oriented protocol, which means that it establishes a dedicated end-to-end connection between the sender and receiver before sending data. This connection is maintained throughout the duration of the communication, allowing for reliable, ordered, and error-checked transmission of data.
  - IP: Internet Protocol is a fundamental protocol that allows devices on a network to communicate with each other by providing logical addressing and routing of data packets between devices.
  - Connection-oriented vs. connectionless
    - Connection-oriented and connectionless are two communication models that describe how data is transmitted over a network.
      - The main difference between connection-oriented and connectionless communication models is that connection-oriented protocols provide reliability and ordering guarantees, while connectionless protocols prioritize speed and efficiency over reliability.
      - Connection-oriented protocols are suitable for applications that require the accurate and complete transmission of data, such as file transfer, email, and web browsing, while connectionless protocols are suitable for applications that prioritize speed and responsiveness over reliability, such as online gaming, video streaming, and real-time voice and video conferencing.

#### Execute

- Perform port scans using Nmap.
