## UDP Packet Structure
A UDP packet is simple and contains **only 4 fields** (each **2 bytes = 16 bits**):

| Field Name        | Size (Bits) | Description |
|------------------|------------|-------------|
| **Source Port** | 16 | Port of the sender |
| **Destination Port** | 16 | Port of the receiver |
| **Length** | 16 | Total size of UDP packet (header + data) |
| **Checksum** | 16 | Used for error detection (optional) |
| **Data** | Variable | The actual message being sent |

### Total size of a UDP packet is 2^16 bytes. The size of the data will be 2^16- 8 = 65,527 bytes
---
