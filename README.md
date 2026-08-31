# Enterprise Cisco Packet Tracer Network

## Project Overview

This project presents an enterprise network designed and implemented in Cisco Packet Tracer. The network connects multiple departments and provides VLAN segmentation, inter-VLAN routing, dynamic routing, redundancy, security, and connectivity testing.

## Network Topology

The topology contains two multilayer core switches, two edge routers, access switches, an ISP router, servers, computers, CCTV devices, and guest wireless clients.

## VLAN and IP Addressing Plan

| VLAN | Department | Network | Virtual Gateway |
|---:|---|---|---|
| 10 | HR | 192.168.10.0/24 | 192.168.10.1 |
| 20 | Accounting | 192.168.20.0/24 | 192.168.20.1 |
| 30 | IT | 192.168.30.0/24 | 192.168.30.1 |
| 40 | Sales | 192.168.40.0/24 | 192.168.40.1 |
| 50 | Server Room | 192.168.50.0/24 | 192.168.50.1 |
| 60 | CCTV | 192.168.60.0/24 | 192.168.60.1 |
| 70 | Guest WiFi | 192.168.70.0/24 | 192.168.70.1 |
| 99 | Management | 192.168.99.0/24 | 192.168.99.1 |

## Technologies Used

- **VLANs:** Separate departments and reduce broadcast domains.
- **Inter-VLAN Routing:** Enables controlled communication between VLANs through multilayer switches.
- **OSPF:** Provides dynamic route exchange and automatic path recalculation when a link fails.
- **HSRP:** Provides a virtual default gateway and failover between Core 1 and Core 2.
- **ACLs:** Restrict unauthorized communication between departments and protect the server network.
- **Trunk Links:** Carry multiple VLANs between access switches and core switches.

## Verification Commands

```text
show vlan brief
show interfaces trunk
show ip interface brief
show ip ospf neighbor
show ip ospf interface brief
show ip route
show standby brief
