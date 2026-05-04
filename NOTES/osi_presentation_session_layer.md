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
