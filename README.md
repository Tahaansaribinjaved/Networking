# Cisco Packet Tracer Networking Labs

A hands-on networking lab series documenting my journey from networking fundamentals to advanced Cisco configurations using Cisco Packet Tracer.

---

## 🚀 About This Repository

This repository contains Cisco Packet Tracer lab files (.pkt) and accompanying notes where I build, configure, troubleshoot, and verify networking concepts and cybersecurity. Each lab focuses on a specific topic with practical implementation and verification.

---

## 📚 Table of Contents

- [About This Repository](#about-this-repository)
- [Labs (Day-by-day)](#-labs-day-by-day)
- [Learning Goals](#-learning-goals)
- [Tools & Technologies](#-tools--technologies)
- [How to Use These Labs](#-how-to-use-these-labs)
- [License & Contact](#-license--contact)

---

## 📚 Labs (Day-by-day)

| Day | Topic | Key Concepts | Link | Topology |
|-----|-------|--------------|------|----------|
| 01 | Static Routing | Routing tables, static routes, basic connectivity | [View Day 01](Day-01-static-routing/) | ![Day 01 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-01-static-routing/static route topology pic.jpeg) |
| 02 | EIGRP | Dynamic routing, neighbor establishment, metrics | [View Day 02](Day-02-EIGRP/) | ![Day 02 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-02-EIGRP/topology.png) |
| 03 | OSPF | Link-state routing, areas, LSAs | [View Day 03](Day-03-OSPF/) | ![Day 03 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-03-OSPF/topology.png) |
| 04 | RIP v2 | Distance-vector routing, timers, convergence | [View Day 04](Day-04-RIP/) | ![Day 04 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-04-RIP/topolgy.png) |
| 05 | VLSM | Subnetting, efficient IP addressing, route summarization | [View Day 05](Day-05-VLSM/) | ![Day 05 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-05-VLSM/topology.png) |
| 06 | VLAN | VLANs, access/trunk ports, inter-switch connectivity | [View Day 06](Day-06-VLAN/) | ![Day 06 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-06-VLAN/topology.png) |
| 07 | Inter-VLAN Routing (Layer 3 Switch) | SVIs, inter-VLAN routing, gateway of last resort | [View Day 07](Day-07-INTER_VLAN_ROUTING_USING_LAYER3_SWITCH/) | ![Day 07 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-07-INTER_VLAN_ROUTING_USING_LAYER3_SWITCH/topology.png) |
| 08 | STP vs RSTP | Spanning Tree basics, root bridge election, port states | [View Day 08](Day-08-STP_vs_RSTP/) | ![Day 08 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-08-STP_vs_RSTP/af_topology.png) |
| 09 | EtherChannel (LACP), CDP & LLDP | Link aggregation, neighbor discovery, port-channels | [View Day 09](Day-09-Etherchannel%20_LACP_CDP_LLDP/) | ![Day 09 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-09-Etherchannel%20_LACP_CDP_LLDP/topology.png) |
| 10 | DHCP & DHCP Relay | DHCP server, DHCP relay (ip helper-address), client addressing | [View Day 10](Day-10-DHCP%26DHCP_RELAY/) | ![Day 10 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-10-DHCP%26DHCP_RELAY/DHCP_topology.png) |
| 11 | P1 — Small Office Network | Practical small office topology, addressing & services | [View Day 11](Day-11-P1_an%20_small_office%20_network/) | ![Day 11 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-11-P1_an%20_small_office%20_network/topology.png) |
| 12 | DNS Server | DNS configuration, name resolution, client setup | [View Day 12](Day-12-DNS_server/) | ![Day 12 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-12-DNS_server/topology.png) |
| 13 | NTP | Network Time Protocol, clock synchronization | [View Day 13](Day-13-NTP/) | ![Day 13 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-13-NTP/topology.png) |
| 14 | Syslog | Centralized logging, device monitoring | [View Day 14](Day-14-SYSLOG/) | ![Day 14 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-14-SYSLOG/topology.png) |
| 15 | SNMP | Network monitoring, MIB queries, trap management | [View Day 15](Day-15-SNMP/) | ![Day 15 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-15-SNMP/topology.png) |

> Note: Lab files are stored in each day's folder. Open `.pkt` files with Cisco Packet Tracer. Many labs include topology images and notes — open the day folder and review the included files.

---

## 🎯 Learning Goals

- Build strong networking fundamentals
- Practice Cisco IOS configuration and syntax
- Improve subnetting and IP addressing skills (VLSM)
- Understand and compare routing protocols (Static, RIP, EIGRP, OSPF)
- Configure VLANs and inter-VLAN routing
- Develop troubleshooting workflows and verification commands
- Implement network services (DHCP, DNS, NTP, Syslog, SNMP)
- Build practical cybersecurity awareness

---

## 🛠️ Tools & Technologies

- Cisco Packet Tracer (topology + simulation)
- Cisco IOS CLI (Router/Switch configuration)
- IPv4 (primary), IPv6 (where applicable)
- Bash / Markdown for documentation

---

## 🔎 How to Use These Labs

1. Install Cisco Packet Tracer (recommended version may be noted per-lab).
2. Clone or download this repository.
3. Open the `.pkt` file for the desired lab in Packet Tracer.
4. Review the included notes (if any) and follow configuration steps in simulation or CLI mode.
5. Use `show` and `ping/traceroute` commands to verify connectivity and routing.

Suggested verification commands:
- `show ip route`
- `show ip interface brief`
- `show running-config`
- `ping <ip>`
- `traceroute <ip>`

---

## License & Contact

- License: MIT
- Contact: @Tahaansaribinjaved (GitHub)

---
