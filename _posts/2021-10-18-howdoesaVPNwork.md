---
published: true
title: How does a VPN work?
layout: post
---
## Basics of VPNs

A VPN does one basic thing. It extends an internal, private network to connect to remote devices over the open internet. It does this by creating an tunnel by way of encryption to hide your packets over the internet, there by adding that device to the private network, no matter how far it is geographically or how many routers it has to jump through. Your private network logically thinks that the device is directly connected to the network. 

For a VPN to work, you need to have a program set up on the private network side and on the device side to connect the two together. This gives the cloud user access to all of their resources securely from anywhere in the world. You can even use a VPN connection to create a hybrid cloud environment, where some of your resources are at a physical premesis, and some of your resources are based in the cloud provider's environment, but all the resources see each other on the same network.

This article talks about the protocols used for VPNs and the types of VPNs: [https://www.geeksforgeeks.org/types-of-virtual-private-network-vpn-and-its-protocols/](https://www.geeksforgeeks.org/types-of-virtual-private-network-vpn-and-its-protocols/). You'll use different types of protocols to create VPNs depending on the information you need to store, your security risk level, and any laws, rules, regulations, or contracts you need to adhere to.

Protocols: 

IPSec, Layer 2 Tunneling Protocol, Point to Point Tunneling Protocol, SSL and TLS, OpenVPN, and SSH are all protocols used, which I'll talk about later.  

Types: 

Remote access - one device accesses a network, either physical or cloud based. What's commonly used by remote workers to access a network 

Site-to-Site: - connects two or more geographically separated, or cloud based, networks over the internet
