# Web Server Deployment

## Overview

Infrastructure deployment is an important role for the systems administrator. Public-facing infrastructure such as web servers present unique security and operational challenges compared to endpoints. Configuring a web server requires an understanding of firewall, networking design, network protocols, and security practices.

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

- Router
- Switch
- Hub
- Collision domain
- NGINX
- Apache
- Web server
- Web server ports

#### Execute

- Deploy a NGINX web server
- Configure firewall to allow web server traffic

## Helpful Resources

- [Ubuntu Official Documentation - Install NGINX](https://ubuntu.com/tutorials/install-and-configure-nginx#3-creating-our-own-website)

## Router Review

- Why are routers essential for the operation of networks and the internet?
  - Routers serve as the backbone of networks, enabling connectivity, efficient data transmission, network segmentation, security enforcement, and interconnection between networks.
  - They are essential for the reliable and effective operation of networks, supporting the functioning of the internet and enabling seamless communication between devices and systems across the globe.
  - A router acts as a bridge between a web server and its clients, providing connectivity, IP address management, port forwarding, load balancing, security, and other essential networking functionalities.
  - A router ensures that incoming requests reach the web server and that the responses are properly routed back to the requesting clients, enabling effective web server deployment and smooth website access for users.

- What is a router?
  - A router is a network device that operates at the network layer (Layer 3) of the OSI model.
  - Its primary function is to forward data packets between different networks, directing the packets along the most efficient paths towards their intended destinations.
  - Often sits at the edge of your network and therefore commonly bundled with firewall/network perimeter security.
  - A router connects multiple networks together, such as local area networks (LANs) or wide area networks (WANs), and enables communication between devices within these networks.
  - Routers receive incoming data packets, examine their destination IP addresses, and make decisions on how to forward them based on the information in their routing tables.
  - In addition to packet forwarding, routers often provide other network services such as network address translation (NAT), firewalling, virtual private network (VPN) support, and quality of service (QoS) management.
    > There are many more acronyms for various network sizes. Know them for CompTIA Network+!
  - Anytime you're configuring a router, leave comments and be consistent. Make sure your successor can make sense of your configurations.

- What is a switch?
  - OSI Layer 2 (data link layer) device that connect devices together on a LAN using ethernet
  - Switches receive incoming network packets and forward them to the appropriate destination based on the MAC addresses of the devices connected to the switch.
  - Splits collision domains
    - When a switch receives a packet, it buffers it temporarily and examines the destination MAC address. It then forwards the packet only to the port associated with the destination device, effectively isolating the transmission within that specific collision domain.
      - Here Host A is trying to send a packet to Host C
      - Hosts B and D don’t receive the packet from Host A

- What is a collision domain?
  - A portion of a network where packets go and collisions can occur
    - In Ethernet networks, collisions happen when two or more devices attempt to transmit data over a shared medium simultaneously. When collisions occur, the transmitted data gets corrupted and needs to be retransmitted, leading to reduced network performance and efficiency.
  - If all ports on a device share a collision domain, then all traffic will go to all ports. This is a hub.
  - If each port has its own collision domain, then traffic only goes to the destined port. This is a switch.
  - Switches are harder to sniff traffic because traffic is routed specifically to destination ports. One port doesn't see all traffic.

- What is a broadcast domain?
  - Contains all devices which can reach each other at the data link layer
  - Type of domain where traffic flows all over the network
  - All ports on a switch or a hub are in the same broadcast domain
  - Routers are the only devices that break up broadcast domains

## CompTIA Questions:
- Which of the following addresses is not allowed on the Internet?
  - The addresses in the range 172.16.0.0 through 172.31.255.255 are all considered private, based on RFC 1918. Use of these addresses on the Internet is prohibited so that they can be used simultaneously in different administrative domains without concern for conflict. Some experts in the industry believe these addresses are not routable, which is not true.
- The host address of 172.16.50.255/20 is in what subnet?
  - A Class B /20 mask is a block size of 16 in the third octet. Count by 16s until you pass the host address of 50: 0, 16, 32, 48, 64. The host is in the 48.0 subnet. The next subnet is 64, so the broadcast address is 63.255.
- Which 3 bytes of the Media Access Control (MAC) address F3-B2-CD-E4-F4-42 designate the unique station identifier?
  - The last 3 bytes of the Media Access Control (MAC) address designate the unique station identifier. The first 3 bytes are the organizationally unique identifier (OUI).
- When a wireless card that can run both 802.11b and 802.11g is running at 802.11g speeds, what modulation technique is the card using?
  - 802.11b runs the direct-sequence spread spectrum (DSSS) modulation technique, and 802.11g runs the OFDM modulation technique.
  - In June 2003, a third modulation standard was ratified: 802.11g. This works in the 2.4 GHz band (like 802.11b), but uses the same OFDM based transmission.
- End-to-end loss across an Ethernet cable is called___________________
  - End-to-end loss is referred to as attenuation. If the loss is too great across a cable, the received signal may be too weak to be demodulated.
- Which of the following services use UDP? (Choose three.)
  - DHCP, SNMP, and TFTP use UDP. SMTP, FTP, and HTTP use TCP.
- A junior network administrator adds a router to create a new subnet. What is the default gateway he must assign to the clients from the DHCP server for subnet 192.168.10.0/29, for the third subnet?
  - A /29 is a block size of 8. Starting with subnet zero, count by 8s. 0, 8, 16, 24. 192.168.10.16 is your third subnet and the fourth is 192.168.10.24, so 192.168.10.23 is the gateway for the third subnet.
- Which command captures traffic on all interfaces?
  - To capture traffic on all interfaces, use the any keyword with the -i (interface) switch.
  - `tcpdump -i any`
- Which of the following techniques would increase the bandwidth transmission by joining together multiple connections into one logical connection?
  - Bonding allows you to connect two or more physical connections and join them to create one logical connection. This provides more bandwidth on the connection.
- Which is a tool in the network scanner category? (Choose all that apply.)
  - The CompTIA Network+ objectives cover all three in regard to tools used to analyze today’s networks.
- What is one reason that WPA encryption is preferred over WEP?
  - WPA is cool because it is easy to configure and works great. Type in a passphrase (assuming you’re using a pre-shared key) and you’re done. Plus, you have great security because the keys change dynamically.
- A receiving host has failed to receive all the segments that it should acknowledge. What can the host do to improve the reliability of this communication session?
  - A receiving host can control the transmitter by using flow control (TCP uses windowing by default). By decreasing the window size, the receiving host can slow down the transmitting host so the receiving host does not overflow its buffers.