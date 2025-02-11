## 2️⃣ **Firewalls**
A **firewall** is a security device that monitors and controls incoming and outgoing network traffic based on predefined security rules.

### **Types of Firewalls**
Firewalls can be classified into **Stateless** and **Stateful** firewalls.

### **Stateless Firewall**
- **How it Works**: Checks each packet individually, without keeping track of previous packets.
- **Pros**: Faster because it doesn’t track connection states.
- **Cons**: Less secure since it doesn't understand the context of a connection.
- **Example**:
  - A rule may allow all TCP packets on port `80` (HTTP) but won't check if they belong to an existing connection.

### **Stateful Firewall**
- **How it Works**: Keeps track of active connections and only allows packets that match an existing connection.
- **Pros**: More secure because it understands ongoing communication.
- **Cons**: Slightly slower due to tracking overhead.
- **Example**:
  - If a user starts a connection to `example.com`, a stateful firewall allows responses from that server but blocks unexpected packets.

---

## 3️⃣ **Comparison: Stateful vs Stateless Firewall**

| Feature        | Stateless Firewall | Stateful Firewall |
|---------------|-------------------|-------------------|
| **Tracks Connections** | ❌ No  | ✅ Yes  |
| **Security Level** | 🔽 Lower | 🔼 Higher |
| **Performance** | 🔼 Faster | 🔽 Slightly Slower |
| **Best Use Case** | Simple filtering | Protecting internal networks |

---

## 4️⃣ **How Firewalls Work in Practice**
1. You send a request to a website.
2. The firewall checks if the request follows the rules.
   - If allowed ✅ → The packet is forwarded.
   - If denied ❌ → The packet is dropped.
3. A **stateful firewall** remembers your request and allows only valid responses.
4. A **stateless firewall** checks each packet separately, without remembering the previous ones.

---
