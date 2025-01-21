# OSI Model: 7 Layers of Computer Networks

The **OSI (Open Systems Interconnection)** model is a conceptual framework used to understand and standardize network communication. It divides network communication into **7 distinct layers**, each responsible for a specific function.

---

## 1. Physical Layer (Layer 1)
- **Purpose**: Deals with the physical transmission of data.
- **Key Functions**:
  - Transmission and reception of raw binary data.
  - Defines hardware specifications like cables, switches, and voltages.
  - Ensures synchronization of bits.
- **Examples**:
  - Ethernet cables, fiber optics, hubs, and connectors.

---

## 2. Data Link Layer (Layer 2)
- **Purpose**: Responsible for node-to-node data transfer and error detection.
- **Key Functions**:
  - Framing: Divides data into frames for transmission.
  - Error detection and correction (via checksums or CRC).
  - Media Access Control (MAC) for addressing.
- **Sub-layers**:
  - **MAC (Media Access Control)**: Manages access to the physical medium.
  - **LLC (Logical Link Control)**: Manages data transmission rates between sender and receiver
  - Prevents overwhelming slower receivers with too much data
- **Examples**:
  - MAC addresses, Ethernet, Wi-Fi (IEEE 802.11).

---

## 3. Network Layer (Layer 3)
- **Purpose**: Facilitates routing and forwarding of data across networks.
- **Key Functions**:
  - Logical addressing using IP addresses.
  - Path determination (routing).
  - Packet forwarding between devices.
- **Examples**:
  - Routers, IP addresses (IPv4/IPv6).

---

## 4. Transport Layer (Layer 4)
- **Purpose**: Ensures end-to-end communication and reliable data delivery.
- **Key Functions**:
  - Segmentation and reassembly of data.
  - Flow control to prevent congestion.
  - Error recovery and acknowledgment mechanisms.
- **Protocols**:
  - **TCP (Transmission Control Protocol)**: Reliable, connection-oriented.
  - **UDP (User Datagram Protocol)**: Faster, connectionless.
- **Examples**:
  - TCP, UDP.

---

## 5. Session Layer (Layer 5)
- **Purpose**: Manages sessions between applications.
- **Key Functions**:
  - Establishes, maintains, and terminates communication sessions.
  - Synchronization and dialog control.
- **Examples**:
  - NetBIOS, PPTP, session management in APIs.

---

## 6. Presentation Layer (Layer 6)
- **Purpose**: Translates data between the application layer and the network.
- **Key Functions**:
  - Data translation, encryption, and compression.
  - Converts data formats (e.g., from ASCII to EBCDIC or vice versa).
- **Examples**:
  - SSL/TLS for encryption, data serialization formats (JSON, XML).

---

## 7. Application Layer (Layer 7)
- **Purpose**: Provides end-user services and interfaces.
- **Key Functions**:
  - Facilitates direct interaction with software applications.
  - Defines protocols for data exchange (e.g., HTTP, SMTP).
- **Examples**:
  - Web browsers, email clients, FTP.

---

## OSI Model in Brief
| Layer         | Function                                 | Examples                       |
|---------------|-----------------------------------------|--------------------------------|
| Application   | User interface and data exchange        | HTTP, SMTP, FTP               |
| Presentation  | Data translation, encryption, compression | SSL/TLS, JSON, XML            |
| Session       | Session management                     | NetBIOS, PPTP                 |
| Transport     | End-to-end communication                | TCP, UDP                      |
| Network       | Routing and logical addressing          | IP, Routers                   |
| Data Link     | Node-to-node communication, error detection | MAC addresses, Ethernet       |
| Physical      | Physical hardware and binary data       | Ethernet cables, hubs         |

---

## Key Takeaways
1. The OSI model helps standardize and troubleshoot network communication.
2. Each layer interacts with the one directly above and below it.
3. Understanding these layers aids in identifying where problems might occur in a network.
