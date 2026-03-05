# packet-tracer-acl-standard-lab
Cisco Packet Tracer Lab – Standard ACL Configuration to Block Specific Hosts

# Cisco Packet Tracer Lab – Standard ACL

## Objective
This lab demonstrates how to configure a **Standard Access Control List (ACL)** on a Cisco router to control network traffic based on source IP addresses.

**Goal:** Block PC1 (192.168.1.10) from accessing the server, while allowing PC2 (192.168.2.10).

---------------------------------------------------------------------------------------------------------------------------------------------------

## Network Topology

![Topology](topology.png)

- **PC1:** 192.168.1.10 /24, Gateway 192.168.1.1
- **PC2:** 192.168.2.10 /24, Gateway 192.168.1.1
- **Server:** 192.168.3.10 /24, Gateway 192.168.3.1
- **Router R1:** 
  - G0/0 → Switch1 (PC1 + PC2) 192.168.1.1 /24
  - G0/1 → Switch2 (Server) 192.168.3.1 /24

--------------------------------------------------------------------------------------------------------------------------------------------------------
## Router Configuration Commands

### Configure Interfaces

```bash
enable
configure terminal

interface g0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
exit

interface g0/1
ip address 192.168.3.1 255.255.255.0
no shutdown
exit
