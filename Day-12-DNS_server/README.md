# Dual-Site Enterprise Infrastructure: OSPF Routing, Centralized DNS/HTTP & Cross-Subnet DHCP Relay

## 📌 Project Overview
This project simulates a fully functional multi-site enterprise network in Cisco Packet Tracer. It highlights dynamic site-to-site connectivity using Single-Area OSPF (Area 0), cross-subnet IP address distribution via a centralized DHCP Relay, and internal corporate Web/DNS resolution.

---

## 🏗️ Architecture & Topologies

### **HQ Site (`192.168.20.0/24`):**
* **HQ-Router:** Cisco 2911 / 4321 ISR
* **HQ-Switch:** Cisco 2960 24-Port Switch
* **HQ-Server (`192.168.20.2`):** Centralized Server hosting HTTP, DNS, and multi-pool DHCP services.

### **Branch Site (`172.16.10.0/24`):**
* **Branch-Router:** Cisco 2911 / 4321 ISR
* **Branch-Switch:** Cisco 2960 24-Port Switch
* **Branch-PC:** Client node requesting dynamic IP addressing.

### **WAN Connection (`10.0.0.0/30`):**
* Point-to-Point link connecting HQ and Branch routers over GigabitEthernet interfaces.

---

## ⚙️ Core Technical Configurations

### 1. Dynamic Routing (Single-Area OSPF Area 0)
* Enabled OSPF process `1` on both routers to dynamically advertise internal subnets and WAN links:
  * **HQ Router:** Advertises WAN (`10.0.0.0/30`) & LAN (`192.168.20.0/24`).
  * **Branch Router:** Advertises WAN (`10.0.0.0/30`) & LAN (`172.16.10.0/24`).

### 2. Centralized Services (HQ-Server: `192.168.20.2`)
* **HTTP:** Custom Enterprise Portal hosted on port 80 (`portal.enterprise.com`).
* **DNS:** Local A-Record (`portal.enterprise.com` ➔ `192.168.20.2`) and CNAME Record (`www.enterprise.com` ➔ `portal.enterprise.com`).
* **DHCP Scope (`BranchPool`):** Formatted to issue IPs in range `172.16.10.0/24` with Gateway `172.16.10.1` and DNS `192.168.20.2`.

### 3. Cross-Subnet DHCP Relay
* Implemented `ip helper-address 192.168.20.2` on the Branch Router's LAN interface (`Gig0/0/1`).
* Unicasts Layer 2 DHCP broadcasts across the OSPF-routed WAN to the central HQ Server.

---

## 🧪 Verification & Testing Procedures

1. **Dynamic IP Assignment:** Switched `Branch-PC` to DHCP mode. Confirmed IP acquisition (`172.16.10.10`) along with correct Subnet, Gateway, and DNS details via `ip helper-address`.
2. **DNS & Web Hosting:** Opened `Branch-PC` Web Browser and navigated to `www.enterprise.com`. Confirmed successful DNS resolution and HTTP page rendering.
3. **End-to-End Connectivity:** Verified OSPF routes using `show ip route ospf` and executed successful ICMP pings across WAN to `192.168.20.2`.

---
🤝 **Collaborative Project** | Built as part of our CCNA Hands-On Networking Series.
