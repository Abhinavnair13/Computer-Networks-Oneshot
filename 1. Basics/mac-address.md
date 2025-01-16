# MAC Address (Media Access Control Address)

## What is a MAC Address?
- A **MAC address** is a unique identifier assigned to a network interface card (**NIC**) for communication within a local network. It operates at the **data link layer** (Layer 2) of the OSI model.
- It serves as a unique identification for an individual network interface on a machine.
- If a machine has multiple network interfaces (e.g., Ethernet, Wi-Fi, or Bluetooth), each interface will have its own unique MAC address .

---

## Characteristics of a MAC Address:
1. **Format:**
   - 12 hexadecimal digits, typically separated by colons (:) or hyphens (-).
   - Example: `00:1A:2B:3C:4D:5E` or `00-1A-2B-3C-4D-5E`.

2. **Length:**
   - A 48-bit address:
     - The **first 24 bits** (Organizationally Unique Identifier or OUI) identify the manufacturer.
     - The **last 24 bits** uniquely identify the device.

3. **Uniqueness:**
   - Each MAC address is globally unique to ensure no two devices on a network have the same address.

4. **Burned-In Address (BIA):**
   - MAC addresses are hard-coded into the NIC by the manufacturer but can sometimes be changed (or spoofed) by software.

---

## Types of MAC Addresses:
1. **Unicast:**
   - Identifies a single device on the network.

2. **Multicast:**
   - Targets a group of devices (e.g., for streaming media).

3. **Broadcast:**
   - Targets all devices on the local network.
   - Example: `FF:FF:FF:FF:FF:FF`.

---

## Uses of a MAC Address:
1. **Device Identification:**
   - Ensures devices are uniquely recognized within a local network.

2. **Network Communication:**
   - Used by Ethernet and Wi-Fi protocols for routing data frames within a LAN.

3. **Access Control:**
   - Helps implement whitelists/blacklists to control network access.

4. **Troubleshooting:**
   - Used by network administrators to identify devices and resolve network issues.

---

## How MAC Addresses Work:
When a device sends data over a network, it encapsulates the data into a **frame** that includes:
- **Source MAC Address:** Identifies the sender.
- **Destination MAC Address:** Identifies the intended recipient.

Switches in the network use MAC addresses to direct data to the correct recipient within the local area network (LAN).

---

## Example of a MAC Address Frame:
