# Home Network Documentation

This document provides an overview of my home network, including physical and logical topology, addressing information, configuration, and credential storage practices.

##  1. Physical & Logical Network Topology

The diagram below shows how devices are connected in my home network.  
It includes both the **physical connections** (Ethernet) and **logical wireless connections (Wi-Fi).**

![Home Network Topology](https://raw.githubusercontent.com/Wenyue989/Test/refs/heads/main/home-network-topology.png)

##  2. IP Addressing Documentation

> Notes: For privacy, IP addresses are generalized.

The full IP address list is stored in a separate documentation file:

 [Click to view IP addressing file]((IP%20addressing.txt))
| Device | Connection Type | IP Assignment | Notes |
|--------|----------------|--------------|--------|
| Wi-Fi Router | Wired to ISP Modem | 192.168.0.1 | DHCP Server |
| Smart TV | Wi-Fi | DHCP | Living room |
| Printer | Wi-Fi | Static (192.168.0.20) | For easy printing |
| Laptop 1 | Wi-Fi | DHCP | Primary laptop |
| Laptop 2 | Wi-Fi | DHCP | |
| iPhone x2 | Wi-Fi | DHCP | |
| iPad x2 | Wi-Fi | DHCP | |

##  3. Network Devices and Services

- **ISP Modem**
- **Wi-Fi Router**
  - DHCP enabled
  - Firewall enabled
- **Smart Devices**
  - Phones
  - Laptops
  - iPads
  - Smart TV
  - Printer
 
##  4. Device Configuration Summary

| Setting | Status |
|--------|--------|
| SSID Name | MyHome |
| Wi-Fi Security | WPA2/WPA3 |
| DHCP | Enabled |
| Guest Network | Optional |
| Firmware Updates | Automatically enabled |

##  5. Credential Storage Method

Passwords and login credentials are **not written down or stored in plain text.**

All login credentials are securely stored using the built-in Chrome Password Manager.  
No passwords are stored in plain text or written down.
