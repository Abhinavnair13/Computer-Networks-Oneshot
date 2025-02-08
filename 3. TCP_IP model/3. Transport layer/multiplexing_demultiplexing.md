# Multiplexing and Demultiplexing in the Transport Layer

## What is Multiplexing?
**Multiplexing** is the process of allowing multiple applications or services on a device to send data over the network simultaneously using a **single transport layer protocol (TCP/UDP)**.

### How It Works:
- A computer runs multiple applications at the same time (e.g., a web browser, email client, and a game).
- Each application sends data that needs to be transmitted over the network.
- The transport layer **adds unique port numbers** to differentiate between different application data.
- These multiple streams of data are then combined and sent over the network.

### Example:
Imagine a computer is:
- Browsing a website (`port 80` for HTTP),
- Sending an email (`port 25` for SMTP),
- Streaming a video (`port 443` for HTTPS).

The transport layer **multiplexes** all three data streams and sends them through the network using TCP/UDP.

---

## What is Demultiplexing?
**Demultiplexing** is the process of receiving incoming data and delivering it to the correct application based on its **port number**.

### How It Works:
- When data reaches the receiving computer, the transport layer **checks the port number**.
- It then **forwards the data** to the correct application using the port number mapping.

### Example:
When a server receives network data:
- If it’s for **port 80**, it is sent to the web server.
- If it’s for **port 25**, it is sent to the mail server.
- If it’s for **port 443**, it is sent to a secure web application.

---

## Multiplexing vs. Demultiplexing

| Feature         | Multiplexing | Demultiplexing |
|---------------|-------------|---------------|
| Function      | Combines data from multiple applications and sends it over the network | Separates received data and delivers it to the correct application |
| Uses         | Assigns **unique port numbers** to data from different applications | Uses **port numbers** to direct data to the right application |
| Example     | Sending web, email, and streaming data over TCP/UDP | Receiving data and sending it to the correct app |

---

## Summary:
- **Multiplexing** allows multiple applications to share a single network connection.
- **Demultiplexing** ensures incoming data reaches the correct application.
- **Port numbers** play a key role in differentiating application data.
