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

