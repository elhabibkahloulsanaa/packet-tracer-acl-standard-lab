# packet-tracer-acl-standard-lab
Cisco Packet Tracer Lab – Standard ACL Configuration to Block Specific Hosts

# Cisco Packet Tracer Lab – Standard ACL

## Objective
This lab demonstrates how to configure a **Standard Access Control List (ACL)** on a Cisco router to control network traffic based on source IP addresses.

**Goal:** Block PC1 (192.168.1.10) from accessing the server, while allowing PC2 (192.168.2.10).

----------------------------------------------------------------------------------------------------------------------------------------------

## Network Topology

![Topology](topology.png)

- **PC1:** 192.168.1.10 /24, Gateway 192.168.1.1
- **PC2:** 192.168.2.10 /24, Gateway 192.168.1.1
- **Server:** 192.168.3.10 /24, Gateway 192.168.3.1
- **Router R1:** 
  - G0/0/0 → Switch1 (PC1 + PC2) 192.168.1.1 /24
  - G0/0/1 → Switch2 (Server) 192.168.3.1 /24

----------------------------------------------------------------------------------------------------------------------------------------------


From PC1: ping 192.168.3.10 → ❌ Blocked

From PC2: ping 192.168.3.10 → ✅ Allowed
