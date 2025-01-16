# Network Topologies

## 1. Bus Topology
### Overview:
Bus topology connects all devices via a single central cable (the bus). Data is transmitted in both directions along the bus.

### Pros:
- **Simple and Cost-Effective:** Requires less cabling compared to other topologies.
- **Easy to Extend:** New devices can be added to the bus without significant changes.

### Cons:
- **Limited Scalability:** Performance decreases as the number of devices increases.
- **Single Point of Failure:** A fault in the main cable halts the entire network.
- **Data Collisions:** Higher chance of collisions due to shared medium.

```
.          device1    device2
              |        |
----------------------------------------- central bus
      |           |           |
    device3     device4      device5
```
---

## 2. Star Topology
### Overview:


Star topology connects all devices to a central hub or switch. Communication passes through this central point.

### Pros:
- **High Performance:** No collisions as each device communicates via the central hub.
- **Easy Troubleshooting:** Faults in a device or connection do not affect others.
- **Scalability:** New devices can be easily added.

### Cons:
- **Dependency on Central Hub:** Failure of the hub disables the entire network.
- **Higher Cost:** Requires more cabling and hardware compared to bus topology.
```
 .                       device1
                            |
               device2 --  Hub -- device4
                            |
                          device3
```
---

## 3. Tree Topology
### Overview:
Tree topology is a combination of star and bus topologies, with a hierarchical structure where devices connect to a central node and then branch out.

### Pros:
- **Hierarchical Control:** Central node enables efficient management of the network.
- **Scalability:** Easy to expand by adding more branches.
- **Fault Isolation:** Problems in one branch do not affect others.

### Cons:
- **Complexity:** More difficult to configure and maintain.
- **Dependency on Root Node:** Failure of the central node affects the entire network.
```
.      device1     device2     device3
          \           |           /
           \          |          /
                    HUB1
                      |
---------------------------------------------------central bus
                              |
                            HUB2
                        /    |    \
                       /     |     \
                 device4  device5   device6


```
---

## 4. Mesh Topology
### Overview:
Mesh topology connects every device to every other device. Communication can take multiple paths.

### Pros:
- **Reliability:** High fault tolerance due to multiple paths for data.
- **Scalability:** Can handle high traffic and large networks.
- **No Single Point of Failure:** Network remains operational even if one connection fails.

### Cons:
- **High Cost:** Requires extensive cabling and hardware.
- **Complex Installation and Maintenance:** Challenging to set up and troubleshoot due to multiple connections.

```
.               device1
              /   |     \
        device2---|---- device3
              \   |     /
               device4


```

---

## 5. Ring Topology
### Overview:
Ring topology connects devices in a circular structure where data travels in one or both directions.

### Pros:
- **Efficient Data Flow:** Suitable for networks with predictable traffic.
- **No Collisions:** Data travels in an organized manner around the ring.
- **Moderate Cost:** Less cabling compared to mesh topology.

### Cons:
- **Single Point of Failure:** A fault in any device or connection disrupts the entire network.
- **Difficult Troubleshooting:** Fault isolation can be challenging.
- **Performance Issues:** Adding or removing devices may affect the network.
```
.              device1
             /          \
            /            \
         device2         device4
            \           /
             \         /
               device3
```
