# Framing and Error Detection in the Data Link Layer

## What is Framing?
- Framing is the process of dividing a stream of data into manageable units called **frames** before transmission over the network.
- It ensures that the receiving system can properly interpret the data.
- Frames are the smallest units of transmission at the Data Link Laye
### Example:
Imagine sending a letter inside an envelope. The **envelope** acts as a **frame**, separating different letters (data units) for proper delivery.

### Types of Framing:
1. **Character Count**: A field in the frame header specifies the number of bytes in the frame.
2. **Byte Stuffing (Character Stuffing)**: Special control characters (`FLAG`, `ESC`) are added to mark frame boundaries.
3. **Bit Stuffing**: Extra bits are added to prevent confusion with frame delimiters.
4. **Physical Layer Framing**: Uses signals to define frame boundaries (e.g., Ethernet uses a preamble).

---

## Error Detection in the Data Link Layer
Error detection ensures data integrity by identifying corrupted frames during transmission.

### Common Error Detection Techniques:

1️⃣ **Parity Bit**:
   - Adds an extra bit to maintain even or odd parity.
   - Example: `1010001` → Add `1` for even parity → `10100011`.

2️⃣ **Checksum**:
   - A sum of all data bytes is computed and sent with the frame.
   - The receiver calculates the checksum and verifies the data.

3️⃣ **Cyclic Redundancy Check (CRC)**:
   - Uses polynomial division to generate a **checksum**.
   - Example: **Ethernet** uses CRC-32 for error detection.

---

## How Framing & Error Detection Work Together
1. Data is divided into **frames**.
2. An **error detection code** (e.g., CRC) is added to the frame.
3. The frame is transmitted.
4. The receiver:
   - Uses the error detection code to check for corruption.
   - If no error is found, it processes the data.
   - If an error is detected, it **requests retransmission** for the frame.

---

## 🔹 Summary
- **Framing** organizes data for reliable transmission.
- **Error detection** ensures data integrity.
- Common techniques include **Parity, Checksum, and CRC**.
- Used in protocols like **Ethernet, PPP, and Wi-Fi**.

Let me know if you need more details!
