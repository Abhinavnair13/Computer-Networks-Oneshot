# Network Address Translation (NAT)

## **What is NAT?**
Network Address Translation (NAT) is a technique used to modify IP addresses in packet headers as they pass through a router or firewall. It allows multiple devices on a local network to share a single public IP address.

---

## **Why is NAT Needed?**
- **IPv4 Address Shortage**: Since IPv4 addresses are limited, NAT allows many devices to use one public IP.
- **Security**: Hides private IP addresses from the internet, making it harder for attackers to directly reach devices.
- **Network Management**: Helps in organizing private networks without requiring public IPs for every device.

---

## **Types of NAT**
### **1. Static NAT**
- Maps one private IP to one public IP.
- **Use Case**: When a device (e.g., a server) needs to be accessible from the internet with a fixed public IP.
- **Example**: Mapping `192.168.1.100` to `203.0.113.5`.

###  **2. Dynamic NAT**
- Maps multiple private IPs to a **pool** of public IPs.
- **Use Case**: When a company has a limited number of public IPs and assigns them dynamically as needed.
- **Example**: If a company has 10 public IPs and 50 internal devices, only 10 can go online at a time.

###  **3. Port Address Translation (PAT) (a.k.a. NAT Overload)**
- Maps multiple private IPs to a **single public IP** by using different port numbers.
- **Use Case**: Home routers and corporate networks where multiple devices share the same public IP.
- **Example**:
  - `192.168.1.2:1050` → `203.0.113.1:5000`
  - `192.168.1.3:1060` → `203.0.113.1:5001`
  - The router modifies the source port to distinguish connections.

---

##  **How NAT Works?**
1. A device from a private network (e.g., `192.168.1.2`) requests a website.
2. The NAT router replaces the private IP with a public IP (e.g., `203.0.113.1`).
3. The server on the internet responds to the public IP.
4. The NAT router translates the response back to the original private IP.

---

## **Advantages of NAT**
- Saves IPv4 addresses
- Adds a layer of security by hiding private IPs
- Enables multiple devices to use a single public IP

---

##  **Disadvantages of NAT**
- Can break some applications that rely on end-to-end connectivity
-  Adds slight processing overhead in large-scale networks

---

##  **Conclusion**
- NAT helps manage IP addresses efficiently and provides security.
- **Home routers use NAT Overload (PAT)** to share a single IP.
- **Businesses use Static/Dynamic NAT** depending on their needs.

![nat](https://www.google.com/url?sa=i&url=https%3A%2F%2Fen.wikipedia.org%2Fwiki%2FNetwork_address_translation&psig=AOvVaw24tA7hSrY4a-aESQadQUlM&ust=1739354986434000&source=images&cd=vfe&opi=89978449&ved=0CBQQjRxqFwoTCODtnrOwu4sDFQAAAAAdAAAAABAE)
