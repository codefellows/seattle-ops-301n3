# VPN Tunnel

## Overview

The VPN protocol can be used in several ways; everyday computer users are likely familiar with client VPN services that claim to grant privacy to their customers. Another way to use VPN is to establish a private network connection between two computers (client-server VPN). Today you'll join two separate networks using IPsec Site-to-Site VPN Tunnelling via pfSense's built-in IPsec tunnelling capabilities.

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

- VPN
- VPN Tunnel
- Site-to-site VPN tunnel
- Split tunnel
- Client-server VPN
- IPsec VPN protocols
  - AH
  - ESP
  - SA
    - IKE

#### Execute

- Deploy a site-to-site VPN tunnel

## Helpful Resources

- [Configuring a Site-to-Site IPsec VPN](https://docs.netgate.com/pfsense/en/latest/recipes/ipsec-s2s-psk.html){:target="_blank"}
- [Troubleshooting IPsec VPNs](https://docs.netgate.com/pfsense/en/latest/troubleshooting/ipsec.html){:target="_blank"}


## CompTIA Net+ Practice Exam Questions

- You plug a new host into a switch port and now are unable to access any server resources on the network from the new host. Which of the following are the two probable reasons this is happening? (Choose two.)
  - STP has shut down the port.
  - The port has the wrong VLAN membership.
  - The Spanning Tree Protocol (STP) can shut down a port if there is a possible loop issue. Also, if you have the port in the wrong VLAN membership, you will not be able to connect to your workgroup resources.
- Switches transmit ________________ out all ports so that all links between switches can be found.
  - Switches transmit Bridge Protocol Data Units (BPDUs) out all ports so that all links between switches can be found.
    - BPDUs are used in the Spanning Tree Protocol (STP) to prevent loops in a network topology. They help switches to learn about the network topology, elect a root bridge, and determine the best path to the root bridge. This way, STP ensures there is only one active path between network nodes, thus avoiding loops.
  - Why not MAC Address?
- What type of topology gives you a direct connection between two routers so that there is one communication path?
  - As its name implies, in a point-to-point topology you have a direct connection between two routers, giving you one communication path. The routers in a point-to-point topology can either be linked by a serial cable, making it a physical network, or be far away and only connected by a circuit within a Frame Relay network, making it a logical network.
- Users are complaining that their 802.11g network is going up and down and, when it does work, it has slow response time. What could the problem be?
  - 802.11b and 802.11g networks can receive interference from microwave ovens and cordless phones.
- How many non-overlapping channels are available with 802.11a?
  - The IEEE 802.11a standard provides up to 12 non-overlapping channels, or up to 23 if you add the 802.11h standard.
- ATM uses which type of switching?
  - ATM uses cell-switching technology.
  - Why not packet switching?
- Which of the following are not considered hybrid routing protocols? (Choose all that apply.)
  - RIP and RIPv2 are distance-vector routing protocols. OSPF and IS-IS are link state. BGP is typically used for connecting external networks but can now be used internally, and CompTIA considers BGP a hybrid routing protocol. EIGRP uses qualities from both distance-vector and-link state protocols to create a hybrid routing protocol.

