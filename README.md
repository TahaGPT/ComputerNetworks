# 🌐 Computer Networks Project – Packet Tracer Simulation

> **Course:** CL-3001 Computer Networks  
> **Semester:** Fall 2025  
> **Tool Used:** Cisco Packet Tracer (Student Version 8.2.2+)  
> **Submission Deadline:** 7 December 2025  

---

## 📌 Project Overview

This project focuses on designing, configuring, and simulating a **large-scale enterprise network** using **Cisco Packet Tracer**.  
The network is built from scratch using **VLSM-based subnetting**, **multiple routing protocols**, **route redistribution**, **DHCP**, **NAT**, and **Access Control Lists (ACLs)**.

The goal is to demonstrate a strong understanding of **IP addressing**, **dynamic routing**, and **network security policies** while following strict academic integrity rules.

---

## 🧠 Key Concepts Implemented

- Variable Length Subnet Masking (**VLSM**)
- Dynamic Routing Protocols:
  - **OSPF (Area 1 & Area 2)**
  - **EIGRP (AS 11)**
  - **RIP**
- **Route Redistribution** between routing protocols
- **DHCP Server Configuration**
- **Network Address Translation (NAT)**
- **Access Control Lists (ACLs)**
- Enterprise-level network segmentation

---

## 🗺️ Network Topology Summary

The topology is divided into **multiple blocks and rows**, each using different routing protocols:

### 🔹 Routing Protocol Assignment

| Block | Routing Protocol |
|------|------------------|
| First Block | OSPF (Area 1) |
| Second Block | EIGRP (AS 11) |
| Third Block (First Row) | RIP |
| Second Row (First Block) | RIP |
| Second Row (Last Block) | OSPF (Area 2) |

---

## 🔁 Route Redistribution

Route redistribution is implemented to allow seamless communication between different routing domains:

| Router | Redistribution Type |
|------|---------------------|
| Router 1 | OSPF ↔ EIGRP |
| Router 2 | OSPF ↔ RIP |
| Router 3 | EIGRP ↔ RIP |
| Router 4 | OSPF Area 1 ↔ OSPF Area 2 |

---

## 🧮 IP Addressing & VLSM

- All networks use **VLSM**
- Host requirements are assigned **per subnet** based on the provided IP address file
- CIDR notation is **adjusted if host requirements exceed capacity**
- **Handwritten VLSM tree** is mandatory for submission and demo

📌 **Important:**  
Networks connected to **Routers 5–9** use available subnets from unused VLSM ranges.

---

## ⚙️ DHCP Configuration

| DHCP Server | Assigned Networks |
|------------|------------------|
| **DHCP 2** | EIGRP, OSPF Area 1, RIP (Top Row) |
| **DHCP 1** | OSPF Area 2 & RIP (Second Row) |

All hosts receive IP addresses **dynamically** via DHCP.

---

## 🌍 NAT Configuration

- **Router 10** implements **NAT**
- **Network G** is translated using the **private IP address** provided
- NAT allows internal hosts to communicate externally

---

## 🔐 Access Control Lists (ACLs)

ACLs are configured to restrict access to specific servers:

| Network | Restriction |
|-------|------------|
| Network L | One PC cannot access the **Web Server** |
| Network E | One PC cannot access the **Data Server** |
| Network A | All hosts blocked from **TFTP Server** |

📌 Servers are treated as **hosts only** (services not required).

---

## 🛠️ Tools & Technologies

- **Cisco Packet Tracer 8.2.2+**
- Dynamic Routing (OSPF, EIGRP, RIP)
- DHCP, NAT, ACL
- Manual VLSM planning

---


---

## 🚀 How to Run the Project

1. Install **Cisco Packet Tracer 8.2.2 or later**
2. Open the `.pkt` file from the `PacketTracer` folder
3. Verify:
   - Routing tables
   - DHCP bindings
   - NAT translations
   - ACL restrictions
4. Test connectivity using **ping** and **simulation mode**

---

## 📋 Submission Checklist

✔ Packet Tracer `.pkt` file  
✔ Handwritten VLSM Tree  
✔ Proper routing & redistribution  
✔ Working DHCP & NAT  
✔ ACL rules enforced  

---

## 🙌 Acknowledgements

This project was completed as part of the **CL-3001 Computer Networks course** to strengthen hands-on understanding of real-world networking concepts.

---

## 📬 Contact

For academic queries or clarifications, reach out via your official course communication channels.

---

**Good Luck & Happy Networking! 🌐**

