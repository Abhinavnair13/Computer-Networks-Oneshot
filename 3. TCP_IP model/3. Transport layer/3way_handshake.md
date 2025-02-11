# TCP 3-Way Handshake

## What is the 3-Way Handshake?
The **3-Way Handshake** is a process used by **TCP** to **establish a reliable connection** between a client and a server **before** data transmission begins.

### **Why is it needed?**
- Ensures **both sides are ready** to communicate.
- Synchronizes **sequence numbers** to track data.
- Prevents **connection errors**.

---

## **Steps in the 3-Way Handshake**

1. **SYN (Synchronize)** – The client starts the connection
   - The client sends a **SYN** message to the server.
   - It includes an **initial sequence number (ISN)** to start communication.

   📩 **Client → Server**: *"Hey, I want to connect! My sequence number is X."*

2. **SYN-ACK (Synchronize + Acknowledge)** – The server responds
   - The server replies with a **SYN-ACK** message.
   - It acknowledges the client's request and sends its own **ISN**.

   📩 **Server → Client**: *"Got it! My sequence number is Y, and I acknowledge your X."*

3. **ACK (Acknowledge)** – The client confirms
   - The client sends an **ACK** message to confirm.
   - The connection is now **established**, and data transfer can begin.

   **Client → Server**: *"Great! Let's start sending data."*

---

## **Example: Opening a Website**
Imagine you're opening **www.example.com** in a browser.

1. Your computer sends a **SYN** to the web server.
2. The web server responds with a **SYN-ACK**.
3. Your computer sends an **ACK**, and the connection is ready!

---


---

## **Summary**
- The **3-way handshake** ensures **both devices are ready** before sending data.
- It uses **SYN, SYN-ACK, and ACK** messages.
- It helps prevent **connection issues and lost data**.

**Think of it like a phone call:**
1. You call someone (**SYN**).
2. They pick up and say "Hello" (**SYN-ACK**).
3. You say "Hi" back (**ACK**), and you start talking! 📞
