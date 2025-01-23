# Networking Devices

## 1. Repeater
### Introduction
A repeater is a network device used to regenerate and amplify signals in a network. It ensures that the signal can travel longer distances without degradation.

### Key Features
- Operates at **Layer 1 (Physical Layer)** of the OSI model.
- Regenerates the incoming signal and retransmits it but doesn't amplify it.
- Used in both wired and wireless networks.
- 2 port device

### Advantages
- Extends the range of a network.
- Improves signal strength.

### Limitations
- Does not filter traffic.
- Does not understand network protocols.

---

## 2. Hub
### Introduction
A hub is a basic network device that connects multiple computers or devices in a Local Area Network (LAN). It broadcasts incoming data packets to all connected devices.
It is like a multiport repeater.

### Key Features
- Operates at **Layer 1 (Physical Layer)** of the OSI model.
- All connected devices share the same bandwidth.

### Types of Hubs
1. **Passive Hub**:
   - Only connects devices and forwards signals.
   - Does not amplify or regenerate the signal.
2. **Active Hub**:
   - Amplifies and regenerates signals before broadcasting them.
3. **Intelligent Hub**:
   - Includes management features for monitoring and managing the network.

### Advantages
- Simple and cost-effective.
- Easy to install.

### Limitations
- Does not reduce network congestion.
- Inefficient as it sends data to all connected devices.

---

## 3. Bridge
### Introduction
A bridge is a repeater, with add on functionality of filtering content by reading MAC addresses of source and destination. It operates at the **Data Link Layer (Layer 2)** of the OSI model.
It is also used for interconnecting two LANs working on the same protocol. It has single input and single output, making it a 2 port device.

### Key Features
- Filters traffic based on MAC addresses.
- Reduces collisions by dividing the network into segments.

### Types of Bridges
1. **Transparent Bridge**:
   - Operates without modifying data.
   - Devices are unaware of its presence.
2. **Source Routing Bridge**:
   - Determines the route based on the source address.
3. **Translational Bridge**:
   - Connects two networks with different protocols, e.g., Ethernet and Token Ring.

### Advantages
- Improves network performance by segmenting traffic.
- Reduces collision domains.

### Limitations
- Limited scalability compared to switches.

---

## 4. Switch
### Introduction
A switch is a multiport bridge with a buffer and a design that can boost its efficiency(large number of ports implies less traffic) and performance. It operates at the **Data Link Layer (Layer 2)**.
Switch can perform error checking before forwarding data, that makes it very efficient as it does not forward packets that have errors and forward good packets selectively to correct port only. In other words, switch divides collision domain of hosts, but broadcast domain remains same.

### Key Features
- Uses MAC addresses to forward data frames.
- Creates a separate collision domain for each connected device.

### Advantages
- High-speed data transfer.
- Reduces network congestion.
- Supports VLANs (Virtual LANs).

### Limitations
- More expensive than hubs and bridges.
- Requires proper configuration for advanced features.

---

## 5. Router
### Introduction
A router is a network device that connects multiple networks and routes data between them. It operates at the **Network Layer (Layer 3)** of the OSI model.

### Key Features
- Uses IP addresses to forward data packets.
- Supports advanced features like Quality of Service (QoS) and firewalls.

### Advantages
- Enables communication between different networks.
- Provides security through packet filtering.
- Supports dynamic routing protocols like OSPF, RIP, and BGP.

### Limitations
- Expensive compared to switches.
- Requires complex configuration.

---

## 6. Gateway
### Introduction
A gateway is a network device that acts as an entry point and translator between two different networks using different protocols. It operates at all layers of the OSI model, depending on the implementation.

### Key Features
- Translates data formats, protocols, or network architectures.
- Acts as a protocol converter.

### Advantages
- Enables communication between heterogeneous networks.
- Provides security and traffic control.

### Limitations
- Can be a bottleneck if overloaded.
- High configuration complexity.

---

## 7. Brouter
### Introduction
A brouter (bridge router) is a hybrid device that combines the functionalities of both a bridge and a router. It operates at both **Layer 2 (Data Link)** and **Layer 3 (Network)** of the OSI model.

### Key Features
- Acts as a bridge for non-routable protocols.
- Acts as a router for routable protocols.
- Filters and forwards packets based on both MAC and IP addresses.

### Advantages
- Versatile as it supports both bridging and routing.
- Optimizes network performance by segregating traffic intelligently.

### Limitations
- Higher cost compared to standalone bridges or routers.
- Requires proper configuration to function effectively.

---
