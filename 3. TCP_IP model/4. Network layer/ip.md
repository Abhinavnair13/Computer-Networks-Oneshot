# Internet Protocol (IP)

The **Internet Protocol (IP)** defines the way devices send and receive data using unique IP addresses.

---

## 1️⃣ IPv4 vs. IPv6

### **IPv4 (Internet Protocol Version 4)**
- 32-bit address (e.g., `192.168.1.1`)
- Supports about **2^32** unique addresses
- Uses **dot-decimal notation** (e.g., `192.168.1.1`)
- Running out of available addresses due to internet growth

### **IPv6 (Internet Protocol Version 6)**
- 128-bit address (e.g., `2001:0db8:85a3::8a2e:0370:7334`)
- Supports **2^128** addresses (virtually unlimited)
- Uses **hexadecimal notation** (e.g., `fe80::1`)
- Improves security and efficiency

---

## 2️⃣ IP Address Classes (For IPv4)

IPv4 addresses are divided into **five classes**:

| Class | Address Range      | Default Subnet Mask | Used For |
|-------|-------------------|---------------------|----------|
| A     | 1.0.0.0 - 126.255.255.255  | 255.0.0.0   | Large networks (e.g., ISPs, big companies) |
| B     | 128.0.0.0 - 191.255.255.255 | 255.255.0.0 | Medium-sized networks |
| C     | 192.0.0.0 - 223.255.255.255 | 255.255.255.0 | Small networks (e.g., home, office) |
| D     | 224.0.0.0 - 239.255.255.255 | N/A         | Multicasting |
| E     | 240.0.0.0 - 255.255.255.255 | N/A         | Reserved for future use |

---

## 3️⃣ Subnetting


A **Subnet Mask** is used in networking to divide an IP address into **network** and **host** portions. It helps routers and devices determine which part of the IP address refers to the network and which part refers to a specific device (host) within that network.

---

## **What is a Subnet Mask?**

A **Subnet Mask** is a 32-bit number that accompanies an IP address to determine which part of the address is for the **network** and which part is for the **host**.

- For example, if the IP address is `192.168.1.10` and the subnet mask is `255.255.255.0`, the first 24 bits (`255.255.255`) represent the **network** portion, and the remaining 8 bits (`.10`) represent the **host** portion.
  Which means the first 24 bits are reserved and the last 8 bits can be anything.
---
Example:
- A company with `192.168.1.0/24` (256 IPs) can divide it into:
  - `192.168.1.0/26` (64 IPs)
  - `192.168.1.64/26` (64 IPs)
  - `192.168.1.128/26` (64 IPs)
  - `192.168.1.192/26` (64 IPs)

---

## 4️⃣ Allocation of IP Addresses

### **Public vs. Private IPs**
- **Public IP**: Assigned by **ISPs** (Internet Service Providers) and used for internet communication.
- **Private IP**: Used within a local network (`192.168.x.x`, `10.x.x.x`, `172.16.x.x - 172.31.x.x`).

---

## 5️⃣ Reserved Addresses

| Address Range       | Purpose |
|---------------------|---------|
| `0.0.0.0`          | Default route (all networks) |
| `127.0.0.0/8`      | Loopback (testing network stack) |
| `169.254.0.0/16`   | APIPA (automatic private addressing) |
| `192.168.x.x`      | Private networks |
| `10.x.x.x`         | Private networks |
| `172.16.0.0 - 172.31.255.255` | Private networks |

---

## 6️⃣ Loopback Address (`127.0.0.1`)

- Used to test a computer's **own network stack**.

- The loopback address is treated as if it's always reachable and it's used by the operating system to test network functionality.
- When you use the loopback address, the device sends packets to itself.
- If you ping `127.0.0.1`, it checks if TCP/IP is working **on your machine**.
