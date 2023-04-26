# Network Traffic Analysis with Wireshark

## Overview

The Kali Linux distribution includes a plethora of offensive security software tools that you will find useful in this course. Wielded by pentesters, ethical hackers, forensics investigators, and enthusiasts, Kali Linux is the popular go-to weapon for performing all manner of cyber attacks. Today you will use one of its most infamous tools, Wireshark.

Wireshark is capable of network traffic analysis, and is generally regarded as a computer forensics tool for its ability to "zoom in" and scrutinize network traffic at the lowest level.

## Class Outline

- Guest Presentation: Implicit Bias
- Course Overview of Ops 301
- Discussion: Career Outcomes of Ops 301
- Lecture Today's Lab Topic
- Demo Today's Lab Topic
- Lab

## Learning Objectives

### Students will be able to

#### Describe and Define

- OSI model
  - Open Systems Interconnection Reference Model is a guide we use to help understand the flow of data as it moves across the network.
    - This model is not intended as a strict representation, but instead is an overall guide to understand exactly how the data is flowing.
  - The OSI model describes seven layers that computer systems use to communicate over a network:
    - #1. Physical Layer
      - Where everythig begins and ends on the network. It's the cables, fibers and connectors of the physical network.
      - This layer is not about protocols.
      - The physical layer is responsible for the physical cable or wireless connection between network nodes. It defines the connector, the electrical cable or wireless technology connecting the devices, and is responsible for transmission of the raw data, which is simply a series of 0s and 1s, while taking care of bit rate control.
    - #2 Data Link Layer
      - Data link control protocols.
      - On an ethernet network, the data link layer is referencing the MAC addresses that are communicating on the network.
      - If you are dealing with something that is switching or bridging, or having two devices communicate to each other using these MAC addresses, then we usually refer to this as being in an OSI layer 2.
      - The data link layer establishes and terminates a connection between two physically-connected nodes on a network. It breaks up packets into frames and sends them from source to destination. This layer is composed of two parts—Logical Link Control (LLC), which identifies network protocols, performs error checking and synchronizes frames, and Media Access Control (MAC) which uses MAC addresses to connect devices and define permissions to transmit and receive data.
    - #3 Network Layer
      - aka the routing layer / internet protocol layer
      - Dealing with any type of IP address
      - The network layer has two main functions. One is breaking up segments/fragments into network packets, and reassembling the packets on the receiving end. The other is routing packets by discovering the best path across a physical network. The network layer uses network addresses (typically Internet Protocol addresses) to route packets to a destination node.
      - Fragments are always in multiples of 8 because of the number of fragmentation offset bits in the IP header.
      - If you need to create smaller packets to get the data through the network, this is all occuring at the network layer.
    - #4 Transport Layer
      - The transport layer takes data transferred in the session layer and breaks it into “segments” on the transmitting end. It is responsible for reassembling the segments on the receiving end, turning it back into data that can be used by the session layer. The transport layer carries out flow control, sending data at a rate that matches the connection speed of the receiving device, and error control, checking if data was received incorrectly and if not, requesting it again.
      - Information that appears in our browser window doesn't appear at one time with one packet across the network. It usually takes many packets all put together to be able to build one screen in our browser. This happens in layer 4.
      - The most common protocols that accomplish this transferring of information across the network is the TCP (Transmission Control Protocol) or UDP (User Datagram Protocol).
    - #5 Session Layer
      - The session layer creates communication channels, called sessions, between devices. It is responsible for opening sessions, ensuring they remain open and functional while data is being transferred, and closing them when communication ends. The session layer can also set checkpoints during a data transfer—if the session is interrupted, devices can resume data transfer from the last checkpoint.
      - Many applications handle their own process of starting and ending a communication in layer 5.
      - Certain control protocols communicate between application end points.
      - Tunneling also occurs at this layer.
    - #6 Presentation Layer
      - The presentation layer prepares data for the application layer. It defines how two devices should encode, encrypt, and compress data so it is received correctly on the other end. The presentation layer takes any data transmitted by the application layer and prepares it for transmission over the session layer.
      - This is the layer just before you're able to see the application fully loaded.
      - Character encoding, data encryption/decryption happens at this layer.
      - Many applications also run at layer 7 simultaneously of layer 6.
    - #7 Application Layer
      - Layers 5, 6 and 7 are dealing with the way that applications communicate across the network.
      - The application layer is used by end-user software such as web browsers and email clients. It provides protocols that allow software to send and receive information and present meaningful data to users. A few examples of application layer protocols are the Hypertext Transfer Protocol (HTTP), File Transfer Protocol (FTP), Post Office Protocol (POP), Simple Mail Transfer Protocol (SMTP), and Domain Name System (DNS).
      - This is the layer we can see, like a broswer window.
  - Resources:
    - https://www.imperva.com/learn/application-security/osi-model/
    - [Professor Messer Understanding the OSI Model - CompTIA Network+ N10-007 - 1.2](Understanding the OSI Model - CompTIA Network+ N10-007 - 1.2)
- NTA
  - AKA "Network Traffic Analysis"
  - A method of monitoring network availability and activity to identify anomalies, including security and operational issues. Common use cases for NTA include: Collecting a real-time and historical record of what's happening on your network.
- SYN/ACK
  - SYN > SYN/ACK > ACK
    - SYNchronize
    - SYNchronize-ACKnowledgement
    - ACKnowledge
  - The three messages transmitted by TCP to negotiate and start a TCP session are nicknamed SYN, SYN-ACK, and ACK.
  - The three message mechanism is designed so that two computers that want to pass information back and forth to each other can negotiate the parameters of the connection before transmitting data such as HTTP browser requests.
- Kali Linux
  - Kali Linux (formerly known as BackTrack Linux) is an open-source, Debian-based Linux distribution aimed at advanced Penetration Testing and Security Auditing. It does this by providing common tools, configurations, and automations which allows the user to focus on the task that needs to be completed, not the surrounding activity.
  - Kali Linux contains industry specific modifications as well as several hundred tools targeted towards various Information Security tasks, such as Penetration Testing, Security Research, Computer Forensics, Reverse Engineering, Vulnerability Management and Red Team Testing.
  - Kali Linux is a multi-platform solution, accessible and freely available to information security professionals and hobbyists.
  - Resources:
    - https://www.kali.org/docs/introduction/what-is-kali-linux/
- Wireshark
  - Wireshark is a free and open-source network protocol/packet analyzer. It is used for network troubleshooting, analysis, software and communications protocol development, and education. It lets you see what’s happening on your network at a microscopic level.
  - Wireshark will grab packets from the network and display those details to you on the screen in a human-readable form.
  - Wireshark can capture traffic from many different network media types, including Ethernet, Wireless LAN, Bluetooth, USB, and more. The specific media types supported may be limited by several factors, including your hardware and operating system.
- PCAP
  - the name is an abbreviation of "packet capture"
  - a file with captured packet data from Wireshark.
  - is an API that captures live network packet data from OSI model Layers 2-7. Network analyzers like Wireshark create .pcap files to collect and record packet data from a network.
- Packet
  - In networking, a packet is a small segment of a larger message/data.
  - Data sent over computer networks, such as the Internet, is divided into packets. These packets are then recombined by the computer or device that receives them.

#### Execute

- Deploy a Kali Linux VM
- Capture network traffic using Wireshark
- Analyze network traffic and identify protocols of packets
- Analyze a packet and identify its components
- Export network traffic as a PCAP file


## Notes

1. What does a packet header consists of?
  - The header contains the source address, a destination address, protocol, and packet number. The protocol helps identify what type of packet is being transferred, whether it is an email, a web page, a video, etc.

1. What happens during the TCP Handshake?
  - The host, generally the browser, sends a TCP SYNchronize packet to the server. The server receives the SYN and sends back a SYNchronize-ACKnowledgement. The host receives the server's SYN-ACK and sends an ACKnowledge. The server receives ACK and the TCP socket connection is established.

1. What is an HTTP request?
  - An HTTP request is made by a client to a server for data, access or a service.
  - A method is a one-word command that tells the server what it should do with the resource.
    - Create request = `POST`
    - Read request = `GET`
    - Update request = `PUT`
    - Delete request = `DELETE`

1. What is an HTTP response?
  - An HTTP response is made by a server to a client. The aim of the response is to provide the client with the resource it requested, or inform the client that the action it requested has been carried out; or else to inform the client that an error occurred in processing its request.

1. What kind of information can be found in an HTTP header?
  - Request headers contain more information about the resource to be fetched, or about the client requesting the resource.
  - Response headers hold additional information about the response, like its location or about the server providing it.
  - Representation headers contain information about the body of the resource, like its MIME type, or encoding/compression applied.
  - Payload headers contain representation-independent information about payload data, including content length and the encoding used for transport.

1. What is so special about the [CERN](http://info.cern.ch/) website?
  - Cern is where the web was born.
  - Tim Berners-Lee, a British scientist at CERN, invented the World Wide Web (WWW) in 1989. The web was originally conceived and developed to meet the demand for automatic information-sharing between scientists in universities and institutes around the world.

## Helpful Resources

- [Wireshark](https://www.wireshark.org/)
- [Wireshark Cheat Sheet](https://www.comparitech.com/net-admin/wireshark-cheat-sheet/)
- [Kali Linux](https://www.kali.org/downloads/)
