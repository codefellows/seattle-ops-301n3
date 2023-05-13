# Network Address Translation

## Overview

NAT (Network address translation) is a technique performed by routers whereby the IP address in a packet header is altered in transit so that the destination interprets the packet as coming from the new IP instead of the actual originating IP. NAT has played a vital role globally in delaying [IPv4 address exhaustion](https://en.wikipedia.org/wiki/IPv4_address_exhaustion), greatly reducing the need to transition at a large scale to IPv6.

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

- Network types
  - Networks can be categorized into different types based on their size, coverage, and purpose.
  - Geographical networks can be classified into different types based on their scope and technologies used, such as Wide Area Networks (WANs), Metropolitan Area Networks (MANs), or Campus Area Networks (CANs).
  -  "Intranet", "Internet," and "Extranet" describe network environments or concepts that have specific characteristics and purposes in terms of connectivity, security, and availability.

- Network access models
  - Refer to the different approaches and mechanisms used to control and manage access to a computer network.
  - These models define how users and devices are authenticated, authorized, and granted permission to access network resources.
  - In an **open access model**, there are no restrictions on who can access the network. Anyone within the network's physical range or connected to the network can freely access its resources.
    - Internet: Network resources available to the general public at large via ISP
  - In a **closed access model**, strict restrictions are enforced to control network access. Users and devices must authenticate themselves before they are granted access to the network.
    - Intranet: Network resources available only to internal employees
  - A **controlled access model** lies between open and closed access models. It provides a level of access control, but with fewer restrictions compared to closed access.
    - Extranet: Controlled private network resources only made available by hosting company to its partners, vendors/suppliers, or set of customers.

- NAT
  - NAT, which stands for Network Address Translation, is a technology commonly used in computer networking to enable multiple devices to share a single public IP address when accessing the internet.

- Types of NAT
  - **One-to-One** involves a direct mapping of IP addresses.
  - **One-to-Many** allows multiple devices to share a single public IP address.
  - **NAT traversal** facilitates communication across different NATs.
  - **Double NAT** occurs when a router is behind another router, resulting in two layers of address translation.

- IPv4 vs IPv6
  - IPv4 and IPv6 are two versions of the Internet Protocol, the set of rules governing how devices communicate over the internet.
  - IPv6 was developed to address the limitations of IPv4, particularly the exhaustion of address space.
  - Address Length:
    - IPv4 uses 32-bit addresses, allowing for a total of approximately 4.3 billion unique IP addresses.
    - IPv6 uses 128-bit addresses, providing an enormous address space of approximately 340 undecillion (3.4 × 10^38) unique IP addresses. This abundant address space ensures that every device can have a unique and globally routable IP address.
  - Address Format:
    - IPv4 addresses are represented in decimal format, such as 192.168.0.1.
    - IPv6 addresses are represented in hexadecimal format and are divided into eight groups of four hexadecimal digits, separated by colons.
      - For example, `2001:0db8:85a3:0000:0000:8a2e:0370:7334`.
  - Header Format:
    - IPv4 headers are 20 bytes long and contain fields for source and destination addresses, protocol information, and other control flags.
    - IPv6 headers are 40 bytes long and include enhanced features and capabilities, such as built-in support for encryption and quality of service (QoS).
  - Features:
    - IPv4 has been widely used since its inception and is supported by virtually all networking equipment and software. However, the limited address space and the need for workarounds like NAT have led to the development of IPv6.
    - IPv6 is designed to overcome the limitations of IPv4 and provides several advantages, including a vast address space, simplified network configuration through auto-configuration mechanisms, improved mobility support, and enhanced security features.

- IP address exhaustion
  - IP address exhaustion refers to the depletion of available unique IP addresses within a particular version of the Internet Protocol (IPv4). It occurs when the demand for IP addresses exceeds the supply of available addresses.
  - The rapid growth of the internet and the increasing number of connected devices have led to IPv4 address exhaustion. The limited address space has made necessary the use of techniques like NAT to enable multiple devices to share a single public IP address.
  - IPv6 adopts a hierarchical addressing structure, allowing for efficient and scalable address allocation.
  - IPv6 adoption has been gradual, and both IPv4 and IPv6 coexist on the internet. Various transition mechanisms and technologies, such as dual-stack, tunneling, and translation, facilitate the transition from IPv4 to IPv6.

- What is the main purpose for implementing NAT on a network?
  - The main purpose is to enable multiple devices within a private network to share a single public IP address when accessing the internet.
  - NAT plays a crucial role in managing and optimizing the use of IP addresses within a network, providing internet access, security, and flexibility for devices on private networks that share a single public IP address.

- At what layer of the OSI model does NAT happen?
  - Layer 3: Network Layer which is responsible for logical addressing, routing, and the movement of data packets across different networks.
  - NAT modifies the source and/or destination IP addresses within IP packets as they pass through the NAT device.

- What happens to packets when NAT runs out of addresses in the pool of available IPs?
  - This is called "NAT exhaustion".
    - If all the addresses in the pool are assigned to devices, and there are no more available addresses, NAT is said to be "exhausted".
  - The packets will be dropped and an Internet Control Message Protocol (ICMP) "host unreachable" packet is typically sent back to the source device or destination, indicating that the NAT device cannot process the packet.
  - By sending an ICMP host unreachable message, the NAT device provides feedback to the sender or the intended recipient that the packet cannot be delivered due to address exhaustion. This allows the sender or the source device to understand that there may be an issue with address availability and potentially take corrective measures.

- What disadvantage does using NAT pose for routers?
  - Translation results in switching path delays.
    - Complex or poorly implemented NAT configurations, resource limitations, or high traffic loads can potentially impact the overall performance of routers, leading to some delays.
  - Certain applications will not function while NAT is enabled.
    - Some peer-to-peer applications, such as certain online gaming or file-sharing applications, rely on direct communication between devices without intermediaries like NAT.
    - Applications that embed IP addresses within the data payload, rather than solely relying on IP headers, may encounter issues when passing through NAT.
    - Some VPN protocols may have difficulties operating correctly when NAT is involved. NAT can interfere with the encapsulation and decapsulation of VPN packets, causing connection issues or performance degradation.
  - Complicates tunneling protocols such as IPsec.
    - While NAT can introduce complications for tunneling protocols like IPsec, it's important to note that solutions and workarounds exist to address these challenges.
    - NAT traversal techniques, like NAT-T, and proper configuration can help mitigate the issues associated with NAT and tunneling protocols.
  - The router being a network layer device, should not tamper with port numbers(transport layer) but it has to do so because of NAT.
    -  The layered network architecture, as defined by the OSI model, separates networking functions into distinct layers.
      - Routers traditionally operate at the Network Layer (Layer 3), responsible for logical addressing and routing, while transport layer functions, including port numbers, are handled at the Transport Layer (Layer 4).
    - NAT modifies both the source and destination IP addresses as well as the source and destination port numbers of IP packets. This means that the router, acting as a network layer device, has to interfere with and modify transport layer information, which ideally should be left untouched.
    - Tampering with port numbers can potentially introduce compatibility issues with certain network protocols or applications that rely on specific port numbers for proper functionality. Some protocols may embed port numbers within their data payload or expect certain port numbers for communication.
    - The involvement of NAT in modifying port numbers adds complexity to network configurations. Port forwarding or port mapping rules must be configured to ensure that incoming traffic is correctly routed to the appropriate devices within the private network.
  - It's important to note that advancements in NAT traversal techniques and the increasing availability of IPv6 addresses are addressing many of these limitations.

#### Execute

- Implement NAT between two identical networks to facilitate communications

## Helpful Resources

- [Netgate Docs - 1:1 NAT](https://docs.netgate.com/pfsense/en/latest/nat/1-1.html)
- [AWS VPC - NAT](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat.html)

## CompTIA Q&A Study

- Most networks today use private IP addresses and translate the addresses to inside global addresses so packets can be sent out on the Internet. Where would you typically implement NAT to provide this service?
  - Network address translation (NAT) is typically configured on a router that connects to your ISP, and this is the best answer to this question. In larger networks, translation for inside local hosts occurs on the firewall inside of a screened subnet (formerly known as a DMZ).
- What protocol provides detailed information on traffic flows between endpoints?
  - The NetFlow standard provides session information including the source and destination addresses, applications, and traffic volume.
- What should you do when troubleshooting and you have determined that nothing has changed in the network?
  - Once you have established that nothing has changed in the network (part of step 1), the second step in the Network+ troubleshooting model is to establish the most probable cause.
- Which wireless protocol provides both data confidentiality and data integrity?
  - Advanced Encryption Standard (AES) is known as the Counter Mode Cipher Block Chaining-Message Authentication Code (CBC-MAC) protocol. This allows AES-CCMP to provide both data confidentiality (encryption) and data integrity.
- Which layer of the OSI model is responsible for converting data into signals appropriate for the transmission medium?
  - The Physical layer’s job is to convert data into impulses that are designed for the wired or wireless medium being used on the attached segment.