# 🏢 **University Campus Network Design**

## 📖 Introduction

This repository contains the design and implementation details for a **segmented university campus network**. The goal is to create a **robust, scalable, and secure** network infrastructure by dividing the campus IP address space into smaller subnets.

The design ensures each building has its own **Local Area Network (LAN)** while maintaining **interconnectivity** for communication across departments and the outside world.

---
## 🔗 Live Review

[**Live Campus Network Simulation**](https://hashimthepassionate.github.io/Campus-Network-Design-Subnetting-For-Five-Buildings/network.html)


---

## 🎯 Design Principles

Our network design follows key principles to ensure efficiency, security, and performance:

* **Improved Performance:**
  By segmenting the network into smaller subnets, broadcast traffic stays within each building, reducing overall network congestion.

* **Enhanced Security:**
  Separate subnets allow implementation of building-specific security policies and access control measures.

* **Efficient IP Management:**
  No wastage of IP addresses; subnets are sized precisely for current and future requirements.

---

## 🛠️ Implementation Details

Each building requires at least **50 PCs** and **1 router**. To accommodate this, we used a **`/26` subnet mask** (255.255.255.192), which provides:

* **64 total IPs** per subnet
* **62 usable IPs** (for PCs, routers, and future growth)

Each router uses the **first usable IP** of its subnet as the **default gateway**.

---

## 🗂️ IP Address Allocation

| Building   | Department             | Network ID       | Router IP (Gateway) | Usable IP Range               | Broadcast Address |
| ---------- | ---------------------- | ---------------- | ------------------- | ----------------------------- | ----------------- |
| Building 1 | Computer Science       | 192.168.1.0/26   | 192.168.1.1         | 192.168.1.1 – 192.168.1.62    | 192.168.1.63      |
| Building 2 | Electrical Engineering | 192.168.1.64/26  | 192.168.1.65        | 192.168.1.65 – 192.168.1.126  | 192.168.1.127     |
| Building 3 | Mechanical Engineering | 192.168.1.128/26 | 192.168.1.129       | 192.168.1.129 – 192.168.1.190 | 192.168.1.191     |
| Building 4 | Administration         | 192.168.1.192/26 | 192.168.1.193       | 192.168.1.193 – 192.168.1.254 | 192.168.1.255     |
| Building 5 | Library                | 192.168.2.0/26   | 192.168.2.1         | 192.168.2.1 – 192.168.2.62    | 192.168.2.63      |

---

## 🖧 Network Topology

The network follows a **star topology**:

* Each building connects to a **central Layer 3 switch or core router**.
* The core router handles:

  * **Inter-building communication**
  * **Internet access**
  * **Campus-wide security policies**

This centralized design simplifies **network management** and ensures **efficient routing**.

---


## ✅ Conclusion

This subnetted campus network design provides:

* **Scalability:** Easy to add more buildings or devices in the future.
* **Security:** Separate subnets for each department with centralized control.
* **Efficiency:** Reduced congestion and optimized IP usage.

