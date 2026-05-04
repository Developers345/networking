# 2. Presentation Layer

The **Application Layer** is responsible for structuring/preparing data based on messaging standards agreed upon by communicating applications. However, the data at this stage is **not yet in a transmittable format**.

The **Presentation Layer** ensures that data is converted into a format suitable for transmission to lower layers in the network.

---

## Responsibilities of the Presentation Layer

### 2.1 Data Conversion
- Converts data into a standard format.
- Handles encoding/decoding (e.g., ASCII ↔ Unicode).
- Ensures compatibility between different systems.

---

### 2.2 Compression / Decompression
- Reduces the size of data before transmission.
- Improves bandwidth efficiency.
- Decompresses data at the receiver side.

---

### 2.3 Encryption / Decryption
- Encrypts data to ensure security during transmission.
- Decrypts data at the receiver side to restore original content.
- Protects data from unauthorized access.

### Diagram - Presentation Layer
<img width="3568" height="4172" alt="10-AUG-2021-PRESENTATION-LAYER" src="https://github.com/user-attachments/assets/b21149b9-c205-441c-9dee-10d4cd43b44d" />

# 3. Session Layer

The **Session Layer** is responsible for managing **end-to-end application communication**. It ensures that communication sessions between applications are properly established, maintained, and terminated.

---

## Key Responsibilities

### 3.1 Authentication / Authorization

#### Authentication
- Identifies the user attempting to access an application.
- Typically requires credentials such as **username and password**.
- The server validates these credentials before granting access.

#### Authorization
- Determines what actions a user is allowed to perform.
- Based on **roles and permissions** within the application.
- Not all users can perform all operations.

#### Role of Session Layer
- Stores authentication and authorization details at the **session level**.
- Prevents the need for users to repeatedly provide credentials during the same session.

---

### 3.2 Session Management

The Session Layer manages the communication session and ensures reliable data handling:

#### 3.2.1 Packet Identification & Routing
- Identifies received data packets.
- Routes them to the correct application at the destination.

#### 3.2.2 Data Re-sequencing
- Ensures packets are reassembled in the correct order.
- Reconstructs the original message from smaller packets.

#### 3.2.3 Session Tracking
- Keeps track of:
  - Number of packets sent
  - Number of packets received
  - Pending packets

---

## Why Data is Broken into Packets

During transmission, data is divided into smaller packets for the following reasons:

- **Avoid Network Congestion**
  - Prevents a single transmission from blocking the network.

- **Efficient Retransmission**
  - Only lost packets need to be resent, not the entire data.

---

## Note

The **Application, Presentation, and Session Layers** focus on **application-level functionality** and are **not directly involved in actual data transmission** over the network.

## Diagram - Session Layer
<img width="3568" height="4172" alt="10-AUG-2021-SESSION-LAYER" src="https://github.com/user-attachments/assets/e3bc5c4e-f455-46a9-a0f6-01554e80bf24" />



