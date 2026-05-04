# 4. Transport Layer

The **Transport Layer** is responsible for reliable data delivery between applications. It performs the following three key responsibilities:

---

## 4.1 Segmentation
- Takes data from the **Presentation Layer**.
- Breaks the data into smaller units called **segments (packets)**.
- Assigns:
  - **Port Number** → Identifies the destination application.
  - **Sequence Number** → Helps reassemble data in the correct order.

> **Segmentation** is the process of breaking data into smaller packets and assigning port numbers and sequence numbers.

---

## 4.2 Flow Control
- Regulates the speed of data transmission.
- Ensures the sender does not overwhelm the receiver.
- If the receiver has a slow network or processing speed, the sender is instructed to **slow down**.

---

## 4.3 Error Control
- Ensures data integrity during transmission.
- Adds **checksum bits** to each segment.
- Enables the receiver to:
  - Detect corrupted or lost segments.
  - Request retransmission of faulty data.

## Diagram - Transport Layer 
<img width="3568" height="4172" alt="11-AUG-2021-TRANSPORT-LAYER" src="https://github.com/user-attachments/assets/26457a64-4210-42e7-ae84-f46865cd0a1d" />

# 5. Network Layer

The **Network Layer** is responsible for transferring data from one network to another network. Devices such as **routers** operate at this layer.

---

## Responsibilities of the Network Layer

### 5.1 Logical Addressing
- Receives segments from the **Transport Layer**.
- Adds **IP addresses** of:
  - Source computer
  - Destination computer
- The resulting unit is called an **IP packet (Data Packet)**.

---

### 5.2 Routing
- Routing is the technique of moving data packets from one network to another.

#### Steps involved:
1. Identify the **destination IP address**.
2. Router computes the **network address** of the destination.
3. Based on the network address, the packet is forwarded to the appropriate **router/gateway**.

---

### 5.3 Path Determination
- Multiple intermediate devices exist between source and destination.
- The Network Layer determines the **shortest/optimal path** for faster delivery of data packets.

---

## Protocols at Network Layer

- **TCP (Transmission Control Protocol)**
  - Provides **reliability**
  - Sends feedback to the sender
  - Ensures data delivery

- **UDP (User Datagram Protocol)**
  - No feedback mechanism
  - Faster data transmission
  - Less reliable compared to TCP

## Diagram - Network Layer 
<img width="3568" height="4172" alt="12-AUG-2021-NETWORKLAYER" src="https://github.com/user-attachments/assets/c49e4a11-6c7f-4869-a0f4-c8aa1768926e" />

