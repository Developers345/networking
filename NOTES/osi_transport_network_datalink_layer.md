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

# 6. Data Link Layer

The **Data Link Layer** is typically implemented as software/firmware within the **Network Interface Card (NIC)**. It is programmed by the manufacturer and provided with the hardware.

- Responsible for making data **transmittable over the physical channel**.
- Operates when data is transferred **within the same network**.
- Does **not participate in routing between different networks**.

---

## Responsibilities of the Data Link Layer

### 6.1 Physical Addressing
- Takes the **data packet** as input.
- Adds:
  - **Source MAC address**
  - **Destination MAC address**
- Also adds **header and trailer bits**.
- Converts the packet into a **Data Frame**.

---

### 6.2 Media Access Control (MAC)
- Controls access to the physical transmission medium.
- Ensures data is properly transmitted across different communication channels.
- Handles **framing and unframing** of data.
- Makes data accessible to higher layers of the OSI model.

---

### 6.3 Error Control

#### 6.3.1 Collision Detection
- Monitors the network channel.
- Checks whether the communication line is **busy or free**.
- Prevents **data collisions** during transmission.

#### 6.3.2 Faulty Data Frames
- Frames may become corrupted due to hardware issues.
- Adds extra bits (e.g., error-detection bits) to identify corrupted frames.
- Requests **retransmission** when errors are detected.

---

# 7. Daigram - Datalink Layer
<img width="3568" height="4172" alt="14-AUG-2021-DATALINK-LAYER" src="https://github.com/user-attachments/assets/b7e75ba9-29ea-452e-aa9b-b87f73de951b" />


# 7. Physical Layer

The **Physical Layer** is responsible for actual data transmission.

- Converts data bits into signals based on transmission media:
  - **Wired** → Electrical signals  
  - **Fiber** → Light waves  
  - **Wireless** → Radio signals  

- Handles the **actual transfer of data over the communication channel**.


# Summary of OSI Layers (One Shot)
------------------------------

## 1. Application Layer
- Defines **message structure and semantics**.
- Enables applications to exchange data in an **understandable format**.

---

## 2. Presentation Layer
- At the **sender side**: Converts application data into a **transmittable format**.
- At the **receiver side**: Converts data back into an **application-readable format**.

### Responsibilities:
- **2.1 Data Conversion (Character Set)**
- **2.2 Data Compression / Decompression**
  - Reduces bits for faster data transfer
- **2.3 Data Encryption / Decryption**
  - Ensures data security

---

## 3. Session Layer
- Not directly involved in data transmission.
- Responsible for **session management between applications**.

### Responsibilities:
- **3.1 Authentication & Authorization**
  - Tracks user identity and permissions
  - Grants access to applications

- **3.2 Session Management**
  - Tracks transmitted data packets
  - Reorders received packets to reconstruct original message
  - Routes packets to the correct application at the destination

---

## 4. Transport Layer

### Responsibilities:
- **4.1 Segmentation**
  - Breaks data into smaller chunks (segments)
  - Adds **port number** and **sequence number**

- **4.2 Flow Control**
  - Slows down sender if receiver has a slower network

- **4.3 Error Control**
  - Adds **checksum bits**
  - Detects corrupted data at the receiver

---

## 5. Network Layer
- Responsible for **data transmission across networks**.

### Responsibilities:
- **5.1 Logical Addressing**
  - Adds **source and destination IP addresses**
  - Forms a **Data Packet**

- **5.2 Routing**
  - Transfers packets between networks

- **5.3 Path Determination**
  - Identifies the **shortest/optimal path**

---

## 6. Data Link Layer
- Responsible for **data transfer within the same network**.

### Responsibilities:
- **6.1 Physical Addressing**
  - Adds **MAC addresses** and header/trailer bits
  - Forms a **Data Frame**

- **6.2 Media Access Control**
  - Converts frames into a format suitable for transmission

- **6.3 Error Control**
  - **Collision Detection** → Avoids network collisions  
  - **Faulty Data Handling** → Detects corrupted frames and requests retransmission  

---

## 7. Physical Layer
- Converts **bits into signals**:
  - Electrical (wired)
  - Light (fiber)
  - Radio (wireless)
- Responsible for **actual data transmission over the medium**.



