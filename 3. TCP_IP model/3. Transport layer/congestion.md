# Congestion Control in the Transport Layer

## What is Congestion?
**Congestion** occurs in a network when too many packets are sent at the same time, causing delays, packet loss, and reduced performance.

## What is Congestion Control?
**Congestion control** is a mechanism used to **prevent or reduce congestion** by managing the rate at which data is sent over a network.

### Why is Congestion Control Important?
- Prevents **packet loss** and **retransmissions**.
- Ensures **fair bandwidth allocation** among users.
- Improves **network performance** and **reduces delays**.

---

## Types of Congestion Control Algorithms

### 1. **Open-Loop Congestion Control** (Prevention)
- Tries to prevent congestion **before** it happens.
- Methods:
  - **Traffic Shaping** – Controls how data is sent (e.g., Leaky Bucket, Token Bucket algorithms).
  - **Admission Control** – Limits new connections when the network is busy.

### 2. **Closed-Loop Congestion Control** (Recovery)
- Reacts to congestion **after** it occurs.
- Methods:
  - **Packet Dropping** – Drops packets when congestion is detected.
  - **Window Adjustment** – Adjusts the sender’s data rate dynamically.

---

# Congestion Control Algorithms with Simple Examples

## 1. **TCP Tahoe** – "Start slow, stop completely if needed"
- **Concept**: Uses **Slow Start**, then increases speed, but **drops to the minimum** when congestion (packet loss) happens.
- **Example**: A **cautious driver** who starts slow, **speeds up gradually**, but **brakes completely** if they see a red light (packet loss). Then, they start slow again.

## 2. **TCP Reno** – "Slow down instead of stopping completely"
- **Concept**: Similar to Tahoe, but instead of starting from zero, **reduces speed by half** and continues.
- **Example**: A **smarter driver** who **slows down** instead of stopping completely when they see congestion (packet loss), making recovery faster.

## 3. **TCP Vegas** – "Predict and adjust before congestion"
- **Concept**: Detects congestion **before** packet loss by measuring **Round Trip Time (RTT)** and adjusting speed accordingly.
- **Example**: A **predictive driver** who **watches traffic ahead** (measures delay) and adjusts speed **before** getting stuck in traffic.

## 4. **RED (Random Early Detection)** – "Randomly drop packets to avoid full congestion"
- **Concept**: Instead of waiting for congestion, it **randomly drops packets** to signal senders to slow down.
- **Example**: A **traffic police officer** who **randomly stops some cars** at intersections to **prevent** a traffic jam.

## 5. **ECN (Explicit Congestion Notification)** – "Mark packets instead of dropping them"
- **Concept**: Instead of dropping packets, the router **marks them** to notify the sender about congestion.
- **Example**: A **smart traffic system** that **flashes warning signs** to drivers when congestion is ahead, instead of stopping cars.

---

## Summary:
- **TCP Tahoe**: Stop completely on congestion → Restart slow.
- **TCP Reno**: Reduce speed instead of stopping.
- **TCP Vegas**: Predict congestion before it happens.
- **RED**: Randomly drop packets to prevent overload.
- **ECN**: Mark packets instead of dropping them.
- **Congestion Control** prevents network overload and packet loss.
- It is divided into **Open-Loop (prevention)** and **Closed-Loop (reaction)** methods.
