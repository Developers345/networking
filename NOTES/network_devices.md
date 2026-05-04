# Network Devices

## What are Network Devices?

In a typical network, to interconnect multiple computers directly, we need to connect each computer with others using cables and NICs (Network Interface Cards).

- For example, to connect **10 computers**, we would need **n-1 (9) connections per computer**.
- This results in:
  - High setup cost  
  - More cabling  
  - Complex troubleshooting  

This type of setup is usually suitable only for **WAN (Wide Area Networks)**.

To overcome these problems, we use **Network Devices**.

### Definition

**Network Devices** are hardware devices (peripherals) used to establish and manage connections between computers in a network.

---

## Types of Network Devices

1. Repeater  
2. Hub  
3. Switch  
4. Bridge  
5. Router  
6. Firewall  
7. Modem  

---

## 1. Repeater

- A **Repeater** amplifies or regenerates signals.
- It is used to transmit data over long distances within a network.

---

## 2. Hub

- A **Hub** is used to interconnect computers and form a network (typically in **Star Topology**).
- It works at the **Physical Layer** of the OSI model.
- It receives data as signals and **broadcasts (copies) it to all ports**.

### Working

- Every connected computer receives the data.
- Each computer checks if the data belongs to it:
  - If yes → Accepts  
  - If no → Discards  

### Limitations

- High bandwidth consumption  
- Poor network performance  

### Types of Hub

1. **Passive Hub**
   - Does not require power  
   - Does not amplify signals  

2. **Active Hub**
   - Requires power  
   - Amplifies or regenerates signals before forwarding  

---

## 3. Switch

- A **Switch** is an intelligent version of a Hub.
- It works at the **Data Link Layer**.
- It forwards data based on **MAC addresses**.
- Used mainly in **LAN (Local Area Networks)**.

### Advantage

- Sends data only to the intended device → Improves performance  

---

## 4. Bridge

- A **Bridge** connects **two different networks**.
- It has **two ports**.
- It forwards data from one network to another.

---

## 5. Router

- A **Router** connects multiple networks together.
- Unlike a bridge, it has **multiple ports**.
- It works at the **Network Layer**.

### Working

- Uses **IP addresses** to forward data to the correct network  
- Maintains a **Routing Table** to decide paths  

### Advantages

- Controls and manages network traffic  
- Allows configuring routing rules  
- Enables communication between different networks  

---

## 6. Firewall

- A **Firewall** is used to **monitor, control, and restrict network traffic**.
- It tracks:
  - Programs  
  - Ports  
  - Network activity  

### Purpose

- Decides whether a program should be allowed to access the network  

### Types of Firewall

1. **Hardware Firewall**
   - Dedicated network device  
   - Protects the entire network  
   - Used in organizations  

2. **Software Firewall**
   - Built into operating systems  
   - Protects individual computers  

---

## 7. Modem

- A **Modem** performs:
  - **Modulation** (Digital → Analog)  
  - **Demodulation** (Analog → Digital)  

### Use

- Connects computers to the internet via **dial-up connections**

---

## Summary

| Device   | Layer           | Function                          |
|----------|----------------|----------------------------------|
| Repeater | Physical       | Signal regeneration              |
| Hub      | Physical       | Broadcast data to all devices    |
| Switch   | Data Link      | Forward data using MAC address   |
| Bridge   | Data Link      | Connect two networks             |
| Router   | Network        | Connect multiple networks        |
| Firewall | Network/Security | Control network traffic       |
| Modem    | Physical       | Convert signals (Digital/Analog) |

## Diagram - Network Devices -1 
<img width="3568" height="4172" alt="19-AUG-2021-NETWORK-DEVICES1" src="https://github.com/user-attachments/assets/7e6e4bd4-60a3-4904-b048-43271b578617" />

## Diagram - Network Devices -2
<img width="3568" height="4172" alt="20-AUG-2021-NETWORK-DEVICES2" src="https://github.com/user-attachments/assets/3176fbba-0545-43d0-be0b-9dca918f707e" />

## Diagram - Network Devices -3
<img width="3568" height="4172" alt="24-AUG-2021-FIREWALL" src="https://github.com/user-attachments/assets/7a37451a-4402-4267-ab77-31c1cc41d4e1" />

