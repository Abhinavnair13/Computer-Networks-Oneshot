# Address Resolution Protocol (ARP) and ARP Cache

## What is ARP?
ARP (Address Resolution Protocol) is a network protocol used to find the **MAC (Media Access Control) address** of a device when only its **IP address** is known. It operates at the **Network Layer** of the OSI model but interacts directly with the **Data Link Layer**.

---

##  How ARP Works (Example)
### Scenario:
- A computer wants to send data to another device in the same network.
- It knows the destination **IP address** but not the **MAC address**.

### ARP Request-Reply Process:
```
Device A (192.168.1.2) → Device B (192.168.1.3)
```

1️⃣  **Device A** sends a broadcast ARP request:
   - _"Who has IP 192.168.1.3? Tell me your MAC address!"_
   - Sent to `FF:FF:FF:FF:FF:FF` (broadcast MAC address).

2️⃣ **Device B** responds with its MAC address:
   - _"I have IP 192.168.1.3. My MAC address is AA:BB:CC:DD:EE:FF"._

3️⃣ **Device A** saves the MAC address in its **ARP cache** and uses it for communication.

---

## ARP Cache
- The **ARP cache** is a table stored in a computer that keeps recently resolved IP-to-MAC mappings.
- It prevents frequent ARP requests, improving network performance.

### Example ARP Cache:
| IP Address    | MAC Address           | Expiry Time |
|--------------|----------------------|-------------|
| 192.168.1.3  | AA:BB:CC:DD:EE:FF    | 5 min       |
| 192.168.1.4  | 11:22:33:44:55:66    | 5 min       |

- Entries expire after a short time (typically **minutes**) and are refreshed when needed.

---

##  Viewing ARP Cache
- **Windows:** Run `arp -a` in Command Prompt.
- **Linux/macOS:** Run `arp -n` or `ip neigh show`.

---

## Types of ARP
1. **Static ARP**: Manually configured, does not expire.
2. **Dynamic ARP**: Learned through ARP requests, expires after a time.
3. **Proxy ARP**: A router answers ARP requests on behalf of another device.
4. **Gratuitous ARP**: Sent by a device to update other devices' ARP tables (used in failover setups).

---

## Conclusion
- ARP is essential for mapping **IP addresses** to **MAC addresses**.
- The **ARP cache** speeds up communication but can be vulnerable to attacks like **ARP spoofing**.
- ARP works only in **local networks**; routers use different methods for external communication.
