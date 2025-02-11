# **Routers & Their Functioning**

Routers are network devices that **forward data packets** between different networks. They make decisions based on **forwarding tables** and **routing algorithms**.

---

## **1️⃣ Forwarding Table vs. Lookup Table**

🔹 **Forwarding Table**
- Stores information about **where to send packets** next.
- Used in the **data plane** (fast packet forwarding).
- Example entry:

```
Destination: 192.168.1.0/24 → Next Hop: 10.0.0.1, Interface: eth0
```
 **Lookup Table**
- Used to **match incoming packet headers** to forwarding rules.
- Helps the router decide **which entry** in the forwarding table to use.

---

## **2️⃣ Packet Forwarding & Hop-by-Hop Algorithm**

When a router receives a packet:
1. It checks the **destination IP address**.
2. It looks up the **best next-hop** in the **forwarding table**.
3. It sends the packet to the **next router (hop)**.
4. The process repeats until the packet reaches its destination.

 **Hop-by-Hop Algorithm**:
Each router makes an independent decision for forwarding, based on its own forwarding table.

---

## **3️⃣ Control Plane (Routing Decisions)**

-  The **Control Plane** manages the **routing table**, which is used to build the **forwarding table**.
-  It determines the **best paths** using routing protocols like:
 - **OSPF (Open Shortest Path First)** – Finds the shortest path.
 - **BGP (Border Gateway Protocol)** – Manages routes between ISPs.
- The control plane works **slower** than the data plane but ensures efficient routing.

---

# What happens when a new router is added to the network?
## **Static Routing vs. Dynamic Routing in Control Plane**

The **control plane** in networking is responsible for **making routing decisions** and updating routing tables. There are two main types of routing:

---

### **Static Routing**

- Routes are **manually configured** by a network administrator.
- The router follows a **fixed path** for packets, regardless of network changes.

**Example:**
A network admin sets a rule:
```
If destination is 192.168.1.0/24, forward to 10.0.0.1
```
The router will **always** send packets for `192.168.1.0/24` to `10.0.0.1`, even if a better route exists.

**Pros:**
✔ Simple and secure
✔ No extra CPU/memory usage

 **Cons:**
❌ Doesn't adapt to network failures
❌ Not scalable for large networks

---

## **Dynamic Routing**

- The router **automatically updates** routes using routing protocols.
- Routes change based on **network conditions** like congestion or failures.

**Example Routing Protocols:**
- **OSPF (Open Shortest Path First)** – Chooses the shortest path.
- **BGP (Border Gateway Protocol)** – Used for internet routing.
- **RIP (Routing Information Protocol)** – Shares routes with nearby routers.

**How It Works:**
1. A router detects a network failure.
2. It informs other routers using a routing protocol.
3. The routers find an **alternate path** and update the routing table.

 **Pros:**
✔ Adapts to network changes
✔ Efficient for large-scale networks

**Cons:**
❌ Uses more CPU and bandwidth
❌ Can be complex to configure

---

## ** Analogy: Static vs. Dynamic Routing**

 **Static Routing → A Pre-Planned Route**
- Like **following a printed map**—you **can't** change your route if there's traffic.

**Dynamic Routing → GPS Navigation**
- Like **Google Maps**—it **recalculates** the best path if a road is blocked.

---

## **When to Use?**
 **Use Static Routing** when the network is small and rarely changes.
 **Use Dynamic Routing** for large, complex networks that need flexibility.

---


## **4️⃣ Example: Packet Forwarding in Action**

1. You send a request to `www.example.com`.
2. Your router looks up the **destination IP** in its **forwarding table**.
3. It finds the **next hop** and sends the packet forward.
4. The process repeats **hop-by-hop** until the server receives the request.

🚀 **Think of it like a delivery truck**:
- The truck follows a **map** (forwarding table).
- At each city (router), it asks **where to go next** (lookup).
- It keeps moving **step-by-step (hop-by-hop)** until it reaches the destination.

---
