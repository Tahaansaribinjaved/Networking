# Enterprise NTP (Network Time Protocol) Synchronization Lab

## 📌 Project Overview
This project demonstrates the implementation of Network Time Protocol (NTP) in a Cisco Packet Tracer simulation environment. Accurate time synchronization across all network devices is critical for centralized logging, security auditing, troubleshooting, and cryptographic certificate validation in enterprise infrastructures.

---

## 🏗️ Architecture & Topology
* **NTP Server:** Dedicated Server (`192.168.10.10`) acting as the master time reference source.
* **Core Switch:** Cisco 2960 Switch connecting the server and routing devices.
* **Routers (R1, R2, R3):** Multiple Cisco routers configured to synchronize their system clocks with the central NTP server.

---

## ⚙️ Configuration & Implementation

### 1. NTP Server Setup
* Configured a dedicated server on the local subnet (`192.168.10.10`) with NTP services enabled and configured with the master system time.

### 2. Router NTP Peer Configuration
Configured all downstream routers (`R1`, `R2`, `R3`) to point to the central clock source:
```text
enable
configure terminal
ntp server 192.168.10.10
clock timezone PKT 5 0

```

---

## 🧪 Verification & Troubleshooting

* **Checking Reachability & Association:**
```text
show ntp associations

```


*Verified that the reachability register (reach) increases and the router establishes communication with the server (handling large offsets using initial manual synchronization if required).*
* **Checking Synchronization Status:**
```text
show ntp status

```


*Confirmed that the router clock is successfully synchronized with the reference clock.*
* **Validating System Time:**
```text
show clock

```


*Ensured all routers match the exact time zone and timestamp provided by the HQ NTP server.*

---

🤝 **Collaborative Project** | Built as part of our CCNA Hands-On Networking Series.
