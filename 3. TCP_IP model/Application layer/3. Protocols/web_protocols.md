# TCP/IP Protocols

The **TCP/IP protocol suite** is a suite of protocols that includes both stateful and stateless components. It includes many protocols, each designed for specific purposes. Here are some commonly used ones:

---

## 1. HTTP (HyperText Transfer Protocol)
- **Purpose**: Used for transferring web pages, images, and other resources over the internet.
- **Port**: 80 (HTTP), 443 (HTTPS for secure communication).
- **How it works**: Clients (browsers) send requests to web servers, which respond with the requested content. Http uses tcp internally.

---

## 2. DHCP (Dynamic Host Configuration Protocol)
- **Purpose**: Automatically assigns IP addresses and other network configuration settings to devices.
- **Port**: 67 (server) and 68 (client).
- **How it works**: When a device connects to the network, the DHCP server assigns it an IP address.

---

## 3. FTP (File Transfer Protocol)
- **Purpose**: Transfers files between computers on a network.
- **Port**: 20 (data transfer), 21 (control connection).
- **How it works**: A client can upload/download files from an FTP server.

---

## 4. SMTP (Simple Mail Transfer Protocol)
- **Purpose**: Used to send emails from a client to a server or between servers.
- **Port**: 25, 465 (for secure communication).
- **How it works**: Handles outgoing emails and forwards them to the recipient's mail server.

---

## 5. POP3 (Post Office Protocol v3)
- **Purpose**: Downloads emails from a server to a local device and deletes them from the server.
- **Port**: 110, 995 (secure).
- **How it works**: Ideal for retrieving and managing emails offline.

---

## 6. IMAP (Internet Message Access Protocol)
- **Purpose**: Accesses and manages emails directly on the mail server without downloading them.
- **Port**: 143, 993 (secure).
- **How it works**: Ideal for accessing emails from multiple devices since messages remain on the server.

---

## 7. SSH (Secure Shell)
- **Purpose**: Provides secure, encrypted access to remote computers for management and file transfer.
Used to login to someone else's terminal
- **Port**: 22.
- **How it works**: Enables secure login sessions and file operations on remote systems.

---

## 8. VNC (Virtual Network Computing)
- **Purpose**: Allows remote access and control of another computer's graphical desktop.
- **Port**: Typically 5900.
- **How it works**: Displays the screen of a remote computer and lets the user control it as if sitting in front of it.

---
## 9. UDP (User Datagram Protocol)
- **Purpose**: A connectionless protocol used for fast data transmission where reliability is not a priority.
- **Port**: Commonly used with various ports, depending on the application (e.g., 53 for DNS, 67 for DHCP).
- **How it works**: UDP sends data packets (datagrams) without establishing a connection. It does not ensure that the data arrives or is received in the correct order, making it faster but less reliable than TCP.

### Key Characteristics:
- **Connectionless**: Does not establish or maintain a connection before data transmission.
- **Unreliable**: No guarantee of delivery, order, or error-checking.
- **Low Overhead**: Faster than TCP due to less error-checking and overhead.
- **Use Cases**:
  - **Streaming**: For real-time applications like video or audio streaming where speed is more important than reliability.
  - **Gaming**: Online multiplayer games use UDP for quick, low-latency communication.
  - **DNS**: Domain Name System queries, where speed is crucial and occasional lost packets are acceptable.
