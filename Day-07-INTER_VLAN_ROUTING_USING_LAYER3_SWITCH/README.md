# Day 07 — Inter‑VLAN Routing (Essentials)

## Overview
Simple Packet Tracer lab: enable inter‑VLAN routing on a Cisco 3560 multilayer switch using SVIs to route between VLAN 10 (Engineering) and VLAN 20 (Sales).

![Topology](topology.png)

## VLAN & IP Addressing

| VLAN | Name        | Network          | Gateway         |
|------|-------------|------------------|-----------------|
| 10   | Engineering | 192.168.10.0/24  | 192.168.10.1    |
| 20   | Sales       | 192.168.20.0/24  | 192.168.20.1    |

## Key Configuration (copy/paste)

Create VLANs:
```cisco
enable
configure terminal
vlan 10
 name Engineering
vlan 20
 name Sales
end
write memory
```

Access ports (example):
```cisco
interface FastEthernet0/1
 switchport mode access
 switchport access vlan 10
!
interface FastEthernet0/2
 switchport mode access
 switchport access vlan 20
```

Trunk (example):
```cisco
interface FastEthernet0/3
 switchport trunk encapsulation dot1q
 switchport mode trunk
 switchport trunk allowed vlan 10,20
```

Enable routing & SVIs (on 3560):
```cisco
enable
configure terminal
ip routing

interface Vlan10
 ip address 192.168.10.1 255.255.255.0
 no shutdown

interface Vlan20
 ip address 192.168.20.1 255.255.255.0
 no shutdown
end
write memory
```

## Verification (essential commands)
```cisco
show vlan brief
show interfaces trunk
show ip interface brief
show ip route
```

Quick host tests:
- From VLAN 10 host: ping 192.168.10.1 (gateway)
- From VLAN 10 host: ping 192.168.20.101 (other VLAN host)

## Troubleshooting (brief)
- SVIs down: `show ip interface brief` — ensure `no shutdown` and VLAN exists.
- No routing: ensure `ip routing` is enabled on the multilayer switch.
- Trunk issues: verify `show interfaces trunk` and allowed VLANs.

## Lab file
- inter-vlan-routing-using-layer3-switch.pkt
