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
- Network access models
- NAT
- IPv4 vs IPv6
- IP address exhaustion

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