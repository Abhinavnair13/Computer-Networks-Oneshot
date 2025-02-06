# Ephemeral Ports

## Ephemeral Ports
**Ephemeral ports** are a specific type of port used for short-lived, temporary connections. They are dynamically assigned by the operating system for the duration of a session and are typically used for client-side communication.

- They usually range from 49152 to 65535 (though this can vary depending on the system).
- When a client makes a request to a server, it uses an ephemeral port for the connection. Once the connection is closed, the port is released and can be reused by other connections.

### Example:
1. A client in chrome wants to connect to a server on port 80 (HTTP).
2. I have multiple chrome tabs opened
3. How does the server know which tab is communicating
4. The os assigns a temporary port to that client(54321)
5. The client sends a request from port 54321 to the server's IP address on port 80.
6. Once the communication ends, port 54321 is released and can be reused by another client.

## Key Differences
- **Ephemeral ports** are temporary and are used for short-lived client connections, while **regular ports** (well-known or registered) are often used for servers or long-term services.
- **Ephemeral ports** are dynamically assigned by the OS, and **regular ports** are generally fixed or pre-defined.
