## Sockets
- **Purpose**: Sockets provide a communication endpoint for sending and receiving data between devices over a network.
- **How it works**:
  - A socket is a combination of an **IP address** and a **port number**.
  - It enables communication between two devices over the internet or a local network by acting as an interface between the application and the transport layer (TCP/UDP).

---

### Types of Sockets:
1. **Stream Sockets (TCP)**:
   - Used for connection-oriented communication.
   - Ensures reliable data delivery.
   - Example: Web browsing, file downloads.

2. **Datagram Sockets (UDP)**:
   - Used for connectionless communication.
   - Focuses on speed rather than reliability.
   - Example: Online gaming, video streaming.

3. **Raw Sockets**:
   - Used for low-level network operations.
   - Provides direct access to the network layer.
   - Example: Network diagnostics and packet sniffing.

---

### Key Features:
- **Bidirectional Communication**: Allows data exchange between a server and a client.
- **Address Binding**: A socket binds to a specific IP address and port to enable communication.
- **Supports Multiple Protocols**: Works with both TCP (reliable) and UDP (fast).
- **Scalable**: Allows handling of multiple connections via techniques like multithreading or asynchronous programming.

---

### Use Cases:
1. **Web Servers and Browsers**: Sockets enable communication between a browser (client) and a server to load web pages.
2. **Chat Applications**: Real-time messaging apps like WhatsApp use sockets for data exchange.
3. **File Transfer**: FTP applications rely on sockets for uploading and downloading files.
4. **IoT Devices**: Smart devices use sockets to communicate with servers or other devices.

---

### Example Workflow:
1. **Server Side**:
   - Create a socket.
   - Bind it to an IP address and port.
   - Listen for incoming connections.
   - Accept connections and send/receive data.

2. **Client Side**:
   - Create a socket.
   - Connect it to the server's IP address and port.
   - Send and receive data through the socket.

---

### Summary:
Sockets are essential for network communication, enabling devices to send and receive data seamlessly over the internet or a local network. Whether it’s real-time applications like chat or streaming services, sockets play a vital role in modern networking.

---
