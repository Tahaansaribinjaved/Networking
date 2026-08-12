# Day 09 — EtherChannel (LACP), CDP & LLDP

## 📌 Overview

A hands-on Cisco Packet Tracer lab combining three Layer 2 technologies:

- **EtherChannel using LACP**
- **CDP — Cisco Discovery Protocol**
- **LLDP — Link Layer Discovery Protocol**

The lab uses a Cisco switching environment connected to a generic **PT-Switch** to demonstrate link aggregation and neighbor discovery.

---

## 🌐 Topology

```text
                 SW1
              /       \
        LACP            LACP
        /                 \
      SW2               PT-Switch
       |                    |
      PC                  Printer
````

### Devices

* SW1 — Cisco Switch
* SW2 — Cisco Switch
* SW3 — PT-Switch
* PC
* Printer

---

## ⚙️ Configuration

### EtherChannel — LACP

Configured multiple physical links between switches as logical Port-Channels.

```cisco
interface range fa0/1 - 2
channel-group 1 mode active
exit

interface port-channel 1
switchport mode trunk
```

For the second EtherChannel:

```cisco
interface range fa0/3 - 4
channel-group 2 mode active
exit

interface port-channel 2
switchport mode trunk
```

> Adjust interface numbers according to the actual topology.

---

## 🔎 CDP

Enabled Cisco Discovery Protocol for Cisco neighbor discovery.

```cisco
cdp run
```

Verify:

```cisco
show cdp neighbors
show cdp neighbors detail
```

---

## 🌐 LLDP

Enabled LLDP for vendor-neutral neighbor discovery.

```cisco
lldp run
```

Verify:

```cisco
show lldp neighbors
show lldp neighbors detail
```

---

## 🧪 Verification

### EtherChannel

```cisco
show etherchannel summary
```

### CDP

```cisco
show cdp neighbors detail
```

### LLDP

```cisco
show lldp neighbors
```

---

## 📊 Technologies Compared

| Technology | Purpose                                             |
| ---------- | --------------------------------------------------- |
| LACP       | Combines physical links into a logical EtherChannel |
| CDP        | Discovers directly connected Cisco devices          |
| LLDP       | Vendor-neutral neighbor discovery                   |

---

## 🧠 Key Learning

This lab provided hands-on practice with:

* Layer 2 link aggregation
* LACP negotiation
* Port-Channel configuration
* Cisco neighbor discovery
* Vendor-neutral device discovery
* Network topology verification

---

## 🛠️ Tools

* Cisco Packet Tracer
* Cisco IOS
* Cisco Switches
* PT-Switch

