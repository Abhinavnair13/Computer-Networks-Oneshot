# Transport Layer in the TCP/IP Model

## What is the Transport Layer?
The **Transport Layer** is responsible for communication between the network layer to the application within the device.

### Key Responsibilities of the Transport Layer:
1. **Segmentation & Reassembly** – Breaks large messages into smaller chunks (segments) and reassembles them at the destination.
2. **End-to-End Communication** – Ensures data is delivered between the correct applications on different devices.
3. **Error Detection & Correction** – Detects lost or corrupted data and requests retransmission if needed.
4. **Flow Control** – Manages data transfer rate to prevent overwhelming the receiver.
5. **Multiplexing & Demultiplexing** – Allows multiple applications to send/receive data over the network simultaneously.

---

## Transport Layer Protocols

The two main protocols in the Transport Layer of the **TCP/IP model** are:

### 1. **Transmission Control Protocol (TCP)**
   - **Reliable, connection-oriented protocol.**
   - Ensures data is delivered **accurately** and **in order**.
   - Uses **three-way handshake** to establish a connection.
   - Provides **error checking** and **retransmission** if packets are lost.
   - Supports **flow control** to manage data transfer speed.

   **Example:**
   - Used for web browsing (`HTTP/HTTPS`), email (`SMTP, IMAP, POP3`), file transfer (`FTP`).

---

### 2. **User Datagram Protocol (UDP)**
   - **Unreliable, connectionless protocol.**
   - Faster than TCP because it **does not establish a connection** or guarantee delivery.
   - No retransmission or ordering of data packets.
   - Suitable for real-time applications where speed is more important than reliability.

   **Example:**
   - Used for **video streaming (YouTube, Netflix)**, **online gaming**, **VoIP (WhatsApp calls, Zoom)**, and **DNS queries**.
