# Windows Server

## Overview

Microsoft Windows Server is an OS that facilitates the hosting of critical authoritative Windows services on the network, including Active Directory, DNS, DHCP, and Domain Controller roles. Microsoft's Evaluation Center allows for the use of Windows Server for 180 days free with full functionality. When deployed in tandem with Windows 10 Pro endpoints, once can establish a domained LAN with little more than VirtualBox and some relevant Microsoft documentation.

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

- ITIL Framework
- Agile Methodology
- Windows Server 2019
- Enhanced Security Configuration
- Workgroup
- Domain
- Client-server architecture
- Types of servers
- RAID configuration types

#### Execute

- Given a budget, select and recommend a physical server
- Install Windows Server 2019
- Set Windows Server to a static IP address
- Configure IE security settings
- Create a network topology diagram

## Helpful Resources

- [Windows Server 2019 ISO Download](https://www.microsoft.com/en-US/evalcenter/evaluate-windows-server-2019?filetype=ISO)
- [Windows 10 ISO Download](https://www.icloud.com/iclouddrive/01azgWsJOfzZaBbAj-G3sLWTg#Windows10)
- [AD DS Installation and Removal Wizard Page Descriptions](https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/deploy/ad-ds-installation-and-removal-wizard-page-descriptions)

##  Notes

- **CompTIA Project+**  is a beginner-friendly certification focused on project management skills specific to the IT industry. It covers project initiation, planning, execution, monitoring, and closure. It is particularly relevant for project management roles in networking and cybersecurity.
- [Wiki IT Process Maps](https://wiki.en.it-processmaps.com/index.php/Main_Page)
- **Agile 4 Core Values**
  - Individuals and Interactions over Processes and Tools
    - This value emphasizes the importance of valuing people and their interactions within the development process.
    - It recognizes that effective communication, collaboration, and teamwork are crucial for success.
    - While processes and tools are important, the focus should be on fostering effective human relationships and understanding.
  - Working Software over Comprehensive Documentation
    - This value emphasizes the primary importance of delivering working software.
    - While documentation is necessary, Agile prioritizes tangible results and values functional software that meets customer needs.
    - It encourages teams to focus on delivering valuable outcomes rather than spending excessive time on extensive documentation.
  - Customer Collaboration over Contract Negotiation
    - This value emphasizes the need for close collaboration and involvement of customers throughout the development process.
    - Agile recognizes that regular and direct interaction with customers leads to a better understanding of their needs and enables the development of solutions that truly address those needs.
    - Collaboration fosters trust, flexibility, and a shared sense of ownership between the development team and the customer.
  - Responding to Change over Following a Plan
    - This value recognizes that change is inevitable in software development and encourages teams to be adaptable and responsive.
      - Agile values the ability to embrace change and adjust plans accordingly, recognizing that requirements and priorities may evolve throughout the project.
      - Being responsive and flexible enables teams to deliver valuable software that meets the changing needs of the customer.

- **Agile Key Principles**
        - These principles guide Agile teams in their approach to development, encouraging collaboration, adaptability, customer focus, continuous improvement, and technical excellence.
        - Review the principles in the [Agile Manifesto](https://agilemanifesto.org/principles.html)

- What types of servers are there?
  - **Mainframe**
    - Large multifunctional equipment handling high volume traffic
    - Generally enterprises only
    - Millions of dollars
  - **High availability**
    - Failover components
    - E.g. NAS with multiple drives in RAID (redundant array of inexpensive disks)
  - **Cluster**
    - Multiple servers pooling their capabilities
  - **Virtual**
    - Server within a server

- What hardware specs should I look for in a server?
  - Similar to desktop components
  - Look for high CPU and RAM; redundant drives great to find
  - Depends on the purpose

## CompTIA Questions
- Which of the following IP addresses are not allowed on the Internet?
  - The addresses in the ranges 10.0.0.0 through 10.255.255.255 and 172.16.0.0 through 172.31.255.255 as well as 192.168.0.0 through 192.168.255.255 are all considered private, based on RFC 1918. Use of these addresses on the Internet is prohibited so that they can be used simultaneously in different administrative domains without concern for conflict. See Chapter 7 for more details on IP addressing and information on private IP addresses.
- You have one IP address provided from your ISP with a /30 mask. However, you have 300 users that need to access the Internet. What technology will you use to implement a solution?
  - Network address translation can allow up to 65,000 hosts to get onto the Internet with one IP address by using port address translation (PAT).
- How many non-overlapping channels are available with 802.11a?
  - The IEEE 802.11a standard provides up to 12 non-overlapping channels, or up to 23 if you add the 802.11h standard.
- You need to provide access to users in a small office. The users need to connect to the office servers from their cubicles and from the conference room. What device would be a good choice to install?
  - Wireless access points are used in many public areas like airports and coffee shops as well as in homes and small and large businesses.
- Which statements are true regarding ICMP packets? 
  - Internet Control Message Protocol (ICMP) is used to send error messages through the network, but ICMP does not work alone. Every segment or ICMP payload must be encapsulated within an IP datagram (or packet).
- When data is encapsulated, which is the correct order?
  - The encapsulation order is data, segment, packet, frame, bits.
- Which of the following is a hybrid routing protocol?
  - The only protocol you could select is Enhanced Interior Gateway Routing Protocol (EIGRP).
- How many access points can be placed within sight of each other and be configured to be non-overlapping frequencies when running the 802.11g standard?
  - The IEEE 802.11b and g standards provide three non-overlapping channels
  - Sam's Notes via ChatGPT: referring to the last question:
In practice, it is common to use a technique called channel planning to assign non-overlapping channels to neighboring access points. In the case of 802.11g, which operates in the 2.4 GHz frequency band, there are three non-overlapping channels: channels 1, 6, and 11. By deploying access points on these channels and maintaining a sufficient separation distance, you can minimize interference and maximize the number of access points in a given area. It's important to note that other factors such as physical obstructions, interference from other devices, and the number of connected clients can also impact the effective coverage and performance of the access points. Therefore, a comprehensive site survey and network planning are typically recommended to determine the optimal placement and configuration of access points in a specific environment. per gpt3.5
- Why use a proxy server in your network?
  - A proxy server is basically a type of server that handles its client-machine requests by forwarding them on to other servers while allowing granular control over the traffic between the local LAN and the Internet.
- Which two arp utility switches perform the same function?
  - The arp utility’s -a and -g switches perform the same function. They both show the current ARP cache. See Chapter 25 for more information.