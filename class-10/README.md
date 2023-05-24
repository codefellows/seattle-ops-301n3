# Cloud Networking

## Overview

Networking in the AWS cloud differs substantially from traditional on-prem LANs. Understanding how to build efficient and resilient network infrastructure on a cloud platform is an important skill.

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

- VPC
  - Private subnets, and what services live within
  - Public subnets, and what services live within
- Security Groups
- Internet gateways
- NAT gateways

#### Execute

- Create a VPC
- Create both a public and a private subnet within your VPC
- Create two EC2 instances, one in each of your subnets
- Create an Internet Gateway
- Depict the topology in a diagram

## Helpful Resources

- [What is Amazon VPC?](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html){:target="_blank"}
- [Default VPC and default subnets](https://docs.aws.amazon.com/vpc/latest/userguide/default-vpc.html){:target="_blank"}
- [VPC with public and private subnets (NAT)](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Scenario2.html){:target="_blank"}

# Notes
- Sam: a good note for the questions regarding cables: the only type of connection that uses straight through is host to switch, switch to router, etc. crossover is for similar devices, straight through is for dissimilar devices.

- In this lab, you might expect the following AWS charges:
    - Amazon EC2 Instances will incur charges based on the instance type, usage hours, and any additional services or resources associated with the instances.
    - Amazon VPC itself is free, however you may incur charges for additional resources or services associated with the VPC, such as NAT gateways, VPN connections, or VPC peering.
    - Amazon VPC Subnets within your VPC does not incur additional charges.
    - The creation and attachment Amazon Internet Gateway (IGW) to your VPC do not incur additional charges. However, data transfer costs may apply if there is inbound or outbound traffic through the Internet Gateway.
    - Amazon Route Table does not incur additional charges. However, data transfer costs may apply if there is traffic routing through the route table.
    - Amazon Security Groups within your VPC does not incur additional charges.
    - If there is data transfer between your EC2 instances and the internet, data transfer costs may apply. This includes inbound and outbound data transfer through the internet gateway.

# CompTIA Questions
- When are you most likely to see a Request Timed Out message?
  - You are most likely to see a Request Timed Out message when (if) a packet is lost on the way back to the originating host for an unknown error. Remember, if the error occurs because of a known issue, you are likely to see a Destination Unreachable message.
- A company has two 100BaseTX hubs, Hub A and Hub B. The hubs are connected by a 3-meter (9.84-foot) straight-through patch cable. The hosts on Hub A are unable to communicate with the hosts on Hub B. What can you do to correct the problem?
  - Although option A is a preferred solution, the patch cable between the devices will always require a crossover cable because the two devices are pinned the same way for transmission. This makes option C the best answer.
- You install new switches in your server room and are now experiencing network instability and other issues across all servers in the rack. Which device would be used to alert you of a system overheating?
  - This is indication that when you plugged in the switch you exceeded the voltage available in the rack as all of the other equipment began to have issues.
- What is the decimal value for the binary number 11101000?
  - The 128, 64, 32, and 8 bits are on, so just add the values: 128 + 64 + 32 + 8 = 232.
- You connect two switches together using a crossover cable and your whole network goes down. What is the problem?
  - If you have two switches connected together and do not have a loop-avoidance scheme implemented, you will cause broadcast storms and multiple unicast frames to be retransmitted in your network, which brings down the network. Enable STP.
- Which of the following addresses is not allowed on the Internet?
  - The addresses in the range 172.16.0.0 through 172.31.255.255 are all considered private, based on RFC 1918. Use of these addresses on the Internet is prohibited so that they can be used simultaneously in different administrative domains without concern for conflict. Some experts in the industry believe these addresses are not routable, which is not true.
- Your host needs to send a packet to a remote network. What is the destination address in the frame?
  - Packets specifically have to be carried to a router (default gateway) in order to be routed through a network.
- You are the network administrator. A user calls you complaining that the performance of the intranet web server is sluggish. When you try to ping the server, it takes several seconds for the server to respond. You suspect that the problem is related to a router that is seriously overloaded. Which workstation utility could you use to find out which router is causing this problem?
  - The tracert utility will tell you which router is having the performance problem and how long it takes to move between each host. Tracert can be used to locate problem areas in a network.
- What is the decimal equivalent of this binary number: 11000000.10101000.00110000.11110000?
  - 11000000 is 192, 10101000 is 168, 00110000 is 48, and 11110000 is 240.