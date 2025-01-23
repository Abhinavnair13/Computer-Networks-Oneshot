# TCP/IP Protocols

The **TCP/IP protocol suite** is the foundation of modern networking, providing rules for data transmission across the internet. It includes many protocols, each designed for specific purposes. Here are some commonly used ones:

---

## 1. HTTP (HyperText Transfer Protocol)
- **Purpose**: Used for transferring web pages, images, and other resources over the internet.
- **Port**: 80 (HTTP), 443 (HTTPS for secure communication).
- **How it works**: Clients (browsers) send requests to web servers, which respond with the requested content.

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

# Telnet Protocol
- **Purpose**: Provides remote access to devices using a command-line interface.
- **Port**: 23.
- **How it works**: Telnet sends data in plain text, which makes it insecure. It is largely replaced by SSH for secure communication.

---

## Key Differences Between Telnet and SSH:
| **Feature**        | **Telnet**                  | **SSH**                      |
|--------------------|----------------------------|-----------------------------|
| **Security**       | No encryption (insecure).  | Encrypted (secure).         |
| **Port**           | 23                         | 22                          |
| **Use Case**       | Legacy systems, debugging. | Secure remote access.       |

---

## Summary
- TCP/IP protocols are essential for various network services like web browsing, email, file transfer, and remote access.
- **Telnet** is a simple protocol for remote access but lacks security, making **SSH** the preferred choice in modern systems.
