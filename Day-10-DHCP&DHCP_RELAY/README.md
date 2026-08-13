# Day 10 — DHCP & DHCP Relay

## 📌 Overview

A hands-on Cisco Packet Tracer lab demonstrating:

- DHCP Server
- DHCP Client Configuration
- DHCP Relay
- Remote DHCP Server
- IP Address Assignment

The lab contains two scenarios to understand how DHCP works locally and across different networks.

---

## 🌐 Scenario 1 — DHCP

```text
DHCP Server
     |
   Switch
  /  |  \
 PC  PC  Printer
````

Clients receive their IP configuration from the DHCP server.

---

## 🌐 Scenario 2 — DHCP Relay

```text
Clients
   |
 Switch
   |
 Router
   |
   |  DHCP Relay
   |
Remote DHCP Server
```

The router forwards DHCP requests from the client network to the remote DHCP server.

---

## ⚙️ DHCP Server

Example DHCP pool:

```text
Network: 20.1.1.0/24
Gateway: 20.1.1.1
DNS:     8.8.8.8
```

Clients:

```cisco
ipconfig /renew
```

---

## 🔄 DHCP Relay

Configured on the router interface facing the client network:

```cisco
interface g0/0
ip helper-address 20.1.1.2
```

The `ip helper-address` forwards DHCP requests to the remote DHCP server.

---

## 🔍 Verification

Check client addressing:

```text
ipconfig
```

Check router interfaces:

```cisco
show ip interface brief
```

Verify DHCP operation:

```cisco
show ip dhcp binding
show ip dhcp pool
```

---

## 📊 DHCP vs DHCP Relay

| Feature            | DHCP                       | DHCP Relay                       |
| ------------------ | -------------------------- | -------------------------------- |
| Server location    | Local network              | Remote network                   |
| Client receives IP | Directly from DHCP server  | Through relay                    |
| Router required    | Not necessarily            | Yes                              |
| Main purpose       | Automatic IP configuration | Centralized DHCP across networks |

---

## 🧠 Key Learning

DHCP automatically provides network configuration to clients.

DHCP Relay allows a **central DHCP server** to provide addresses to clients located on different networks.

---

## 🛠️ Tools

* Cisco Packet Tracer
* Cisco IOS
* DHCP
* DHCP Relay
* IP Addressing
* Routing

