# Telnet Protocol
- **Purpose**: Provides remote access to devices using a command-line interface. It allows users to connect to a remote computer or server and execute commands as if they were directly accessing it via a terminal.
Telnet operates over TCP
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
