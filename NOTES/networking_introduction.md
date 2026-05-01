# Fundamentals of Networking

## 1. How does computers are connected over the network  
## 2. Machine identification on the network  
## 3. Program identification  
## 4. How does the data transfer takes places over the network  

---

## How does computers are connected over the network?

For any two computers to interconnect and communicate with each other, the computers should have a **Network Interface Card (NIC)** available.  

- It can be:
  - Inbuilt on the motherboard (default), or  
  - Purchased separately and added as a **Peripheral Component Interface (PCI)** card  

The NIC card allows us to plug in an **RJ45 socket port**, interconnecting both computers so that physical data can be transferred from one end to another.

---

## How many network interface cards can be attached to a computer?

A computer can have **one or more NICs**, allowing it to connect directly to multiple computers or networks.

---

## How does one computer communicate with another over the network?

Whenever a computer sends a **data packet** over the network, by default, the data is broadcast to all connected computers.  

To send data to a specific computer, we need a way to identify it.

Each computer in a network is identified using an **IP Address (Internet Protocol Address)**.

---

## IP Address

1. A computer can have **multiple IP addresses**, depending on the number of NICs.  
2. An IP address is a **32-bit number**, divided into **4 octets**  
   - Example: `10.1.34.23`  
3. IP addresses are **not fixed (dynamic)**  
   - Assigned when a computer connects to a network  
   - Released when it disconnects  
   - Hence, called a **logical address**

---

## Types of Addresses in a Network

### 1. Logical Address (IP Address)
- Assigned when a computer connects to a network  
- Can change over time  

### 2. Physical Address (MAC Address)
- Assigned by the hardware manufacturer  
- Unique for each NIC  
- Example:
  - If a computer has 2 NICs → it has 2 MAC addresses  
- **Static (does not change)**  
- Can be modified using software (MAC spoofing)

---

## Communication Requirement

To communicate between computers:
- **IP Address is required (primary)**  
- **MAC Address is used internally for actual data transmission**

## Diagram
<img width="1443" height="782" alt="image" src="https://github.com/user-attachments/assets/cb912d16-983a-45c2-a0cd-9da9dbe473b8" />
