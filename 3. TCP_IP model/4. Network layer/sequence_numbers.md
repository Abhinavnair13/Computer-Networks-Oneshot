# Sequence Number in Networking

## What is a Sequence Number?
A **sequence number** is a unique number assigned to each data packet in a communication process. It helps in **tracking the order of packets** and ensuring **reliable data transfer**.

---

## Why is a Sequence Number Needed?
1. **Ensures Correct Order**: Prevents out-of-order delivery.
2. **Detects Lost Packets**: Helps in retransmitting missing data.
3. **Avoids Duplicate Data**: Ensures no duplicate packets are processed.

---

## Real-World Example 📦
Imagine you order **3 books** online, and the seller ships them separately:

1️⃣ The books are sent in **three separate packages**.
2️⃣ Each package has a **tracking number (sequence number)**: `#1`, `#2`, `#3`.
3️⃣ If package **#2 arrives before #1**, you **wait for #1** to come first.
4️⃣ If package **#3 is missing**, you **ask the seller to resend it**.

This is exactly how **sequence numbers** help computers **reassemble data packets in the right order** and request missing ones.

---

## How Sequence Numbers Work in TCP
### **Sender**:
- Breaks data into small packets.
- Assigns a **sequence number** to each packet.
- Sends packets to the receiver.

### **Receiver**:
- Checks the sequence numbers.
- If all packets arrive **in order**, it processes the data.
- If a packet is **missing**, it requests retransmission.
- If packets arrive **out of order**, it waits for missing packets before processing.

---

## Example of TCP Sequence Numbers
A sender wants to send `"HELLO"`, which is divided into **3 packets**:

| Packet | Data | Sequence Number |
|--------|------|----------------|
| 1| "HE" | **100** |
| 2| "LL" | **102** |
| 3| "O"  | **104** |

### Scenario 1: Normal Delivery
📬 Receiver gets packets `100 → 102 → 104`, assembles `"HELLO"`, and acknowledges.

### Scenario 2: Out-of-Order Delivery
📬 Receiver gets `100 → 104` (missing **102**).
📩 It **requests a resend** for `102`, ensuring no missing data.

---

## Summary
- **Sequence numbers** help track the order of packets.
- They prevent **data loss, duplication, and reordering issues**.
- **TCP uses sequence numbers** to ensure **reliable communication**.
