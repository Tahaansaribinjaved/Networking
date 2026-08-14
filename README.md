# Cisco Packet Tracer Networking Labs

A hands-on networking lab series documenting my journey from networking fundamentals to advanced Cisco configurations using Cisco Packet Tracer.

---

## 🚀 About This Repository

This repository contains Cisco Packet Tracer lab files (.pkt) and accompanying notes I build, configure, troubleshoot, and verify while learning networking and cybersecurity. Each lab focuses on a hands-on topic and includes topology images, configuration steps, and verification commands.

---

## 📚 Table of Contents

- [About This Repository](#about-this-repository)
- [Labs (Day-by-day)](#-labs-day-by-day)
- [Learning Goals](#-learning-goals)
- [Tools & Technologies](#-tools--technologies)
- [Progress](#-progress)
- [Repository Structure](#-repository-structure)
- [How to Use These Labs](#-how-to-use-these-labs)
- [License & Contact](#-license--contact)
- [Appendix — Suggested Next Labs](#-appendix--suggested-next-labs)

---

## 📚 Labs (Day-by-day)

| Day | Topic | Key Concepts | Link | Topology |
|-----|-------|--------------|------|----------|
| 01 | Static Routing | Routing tables, static routes, basic connectivity | [View Day 01](Day-01-static-routing/) | ![Day 01 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-01-static-routing/static%20route%20topology%20pic.jpeg) |
| 02 | EIGRP | Dynamic routing, neighbor establishment, metrics | [View Day 02](Day-02-EIGRP/) | ![Day 02 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-02-EIGRP/topology.png) |
| 03 | OSPF | Link-state routing, areas, LSAs | [View Day 03](Day-03-OSPF/) | ![Day 03 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-03-OSPF/topology.png) |
| 04 | RIP v2 | Distance-vector routing, timers, simple convergence | [View Day 04](Day-04-RIP/) | ![Day 04 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-04-RIP/topology.png) |
| 05 | VLSM + RIP v2 | Subnetting, efficient IP addressing, route summarization | [View Day 05](Day-05-VLSM/) | ![Day 05 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-05-VLSM/topology.png) |
| 06 | VLAN | VLANs, access/trunk ports, inter-switch connectivity | [View Day 06](Day-06-VLAN/) | ![Day 06 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-06-VLAN/topology.png) |
| 07 | Inter-VLAN Routing (Layer 3 Switch) | SVIs, inter-VLAN routing, gateway of last resort | [View Day 07](Day-07-INTER_VLAN_ROUTING_USING_LAYER3_SWITCH/) | ![Day 07 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-07-INTER_VLAN_ROUTING_USING_LAYER3_SWITCH/topology.png) |
| 08 | STP vs RSTP | Spanning Tree basics, root bridge election, port states | [View Day 08](Day-08-STP_vs_RSTP/) | ![Day 08 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-08-STP_vs_RSTP/topology.png) |
| 09 | EtherChannel (LACP), CDP & LLDP | Link aggregation, neighbor discovery, port-channels | [View Day 09](Day-09-Etherchannel%20_LACP_CDP_LLDP/) | ![Day 09 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-09-Etherchannel%20_LACP_CDP_LLDP/topology.png) |
| 10 | DHCP & DHCP Relay | DHCP server, DHCP relay (ip helper-address), client addressing | [View Day 10](Day-10-DHCP%26DHCP_RELAY/) | ![Day 10 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-10-DHCP%26DHCP_RELAY/topology.png) |
| 11 | P1 — Small Office Network | Practical small office topology, addressing & services | [View Day 11](Day-11-P1_an%20_small_office%20_network/) | ![Day 11 Topology](https://github.com/Tahaansaribinjaved/Networking/blob/master/Day-11-P1_an%20_small_office%20_network/topology.png) |

> Note: Lab files are stored in each day's folder. Open `.pkt` files with Cisco Packet Tracer. Many labs include topology images and notes — open the day folder and review the included files.

---

## 🎯 Learning Goals

- Build strong networking fundamentals
- Practice Cisco IOS configuration and syntax
- Improve subnetting and IP addressing skills (VLSM)
- Understand and compare routing protocols (Static, RIP, EIGRP, OSPF)
- Configure VLANs and inter-VLAN routing
- Develop troubleshooting workflows and verification commands
- Begin building practical cybersecurity awareness (ACLs, segmentation)

---

## 🛠️ Tools & Technologies

- Cisco Packet Tracer (topology + simulation)
- Cisco IOS CLI (Router/Switch configuration)
- IPv4 (primary), IPv6 (where applicable)
- Bash / Markdown for documentation

---

## ✅ Progress

- [x] Static Routing
- [x] EIGRP
- [x] OSPF
- [x] RIP v2
- [x] VLSM
- [x] VLAN
- [x] Inter-VLAN Routing
- [ ] STP
- [x] EtherChannel
- [x] DHCP
- [ ] NAT
- [ ] ACL
- [ ] IPv6

---

## 📂 Repository Structure

- Day-01-static-routing/
- Day-02-EIGRP/
- Day-03-OSPF/
- Day-04-RIP/
- Day-05-VLSM/
- Day-06-VLAN/
- Day-07-INTER_VLAN_ROUTING_USING_LAYER3_SWITCH/
- Day-08-STP_vs_RSTP/
- Day-09-Etherchannel _LACP_CDP_LLDP/
- Day-10-DHCP&DHCP_RELAY/
- Day-11-P1_an _small_office _network/
- README.md

Each Day folder typically contains:
- .pkt (Packet Tracer file)
- notes.md or configs.txt with CLI commands and verification output (when provided)

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

## Appendix — Suggested Next Labs

- STP basics and verification
- EtherChannel (LACP / PAgP) and verification
- DHCP (server & relay)
- NAT (static & PAT)
- ACLs for segmentation and basic security
- IPv6 addressing and routing
