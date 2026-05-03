# Responsibilities and Benefits of Protocols in Networking

## What are the responsibilities or benefits of using a protocol in networking?

### 1. Logical Channel Separation

Even though the communication channel is shared among multiple computers, a protocol creates an **illusion of a dedicated communication channel** between two communicating systems.

- The protocol **logically divides the communication channel**
- Prevents **data collision** between multiple users
- Ensures that data sent by the sender is **received intact** by the receiver

---

### 2. Guaranteed Delivery to Intended Receiver

When a sender transmits data over the network:

- Multiple computers may be connected to the same network
- However, the protocol ensures that **only the intended receiver** gets the data
- This guarantees **accurate and secure delivery**

---

## Conclusion

From the above points, we understand that:

- Protocols are essential for enabling communication between computers and programs over a network
- They ensure **reliability, correctness, and proper data delivery**

---

## Diagram - Protocol
<img width="3568" height="4172" alt="04-AUG-2021-PRO" src="https://github.com/user-attachments/assets/1cc4ab8d-4843-4ec4-9a3e-6db6279f8f0c" />


## OSI Model Introduction

To standardize and manage communication across networks, the **OSI (Open Systems Interconnection) Model** was introduced.

- It defines **layers of communication**

## Types of Protocols

There are 2 types of protocols:

### 1. Application Protocol
These protocols are used by end-to-end applications that exchange data between them. They define the **message structure** and **semantics** for how data should be exchanged, so that both applications can easily understand the data.

### 2. Transport Protocol
These define the rules for transmitting the physical bits of data over the network.

---

## OSI Model Layer

The **International Organization for Standardization (ISO)** introduced the **OSI Model (1984)** to define rules for exchanging data between computers/applications over a network.

**OSI** stands for **Open Systems Interconnection**. Using this model, any two computers/applications running on different platforms can communicate over a network.

The OSI model consists of **7 layers**, which represent stages of data transfer. These layers must be executed in sequential order:

- **Top → Bottom**: Sender  
- **Bottom → Top**: Receiver  

### OSI Layers
1. Application Layer  
2. Presentation Layer  
3. Session Layer  
4. Transport Layer  
5. Network Layer  
6. Data Link Layer  
7. Physical Layer  

---

## 1. Application Layer

The Application Layer defines the rules/guidelines that applications must follow to exchange data in an understandable format.

### Types of Programs

Programs communicating over a network can be classified into:

1. Client Program  
2. Server Program  

A **client program** sends data to a **server program**, requesting it to perform an operation and return the result.

### Problem Without Protocol

Example data sent by client:
```

938310/09/2021availability

```

Here, the client intends to send:
- Train Number  
- Travel Date  
- Operation (availability)  

However, the server cannot interpret this data because it lacks a defined structure.

### Solution

To make communication effective, both client and server must define rules in terms of:

1. Message Structure  
2. Semantics  

These rules are called **Application Layer Protocols**.

---

## Requirements for Network Communication

If we build a program that communicates over a network, it must have:

1. Port Number  
2. Application Protocol (message structure and semantics)

---

## Standard Application Layer Protocols

Standard protocols exist because many common applications are widely used on the internet, such as:

1. Email Exchange  
2. File Transfer  
3. Web Browsing  

### Email Exchange Protocols

To ensure interoperability across different email clients and providers, standard protocols are defined:

- **SMTP (Simple Mail Transfer Protocol)**  
- **POP (Post Office Protocol)**  
- **IMAP (Internet Message Access Protocol)**  

All mail servers are designed based on these protocols, enabling users to send and receive emails regardless of their service provider, since all servers follow the same protocol standards.


### Diagram - 1: OSI Model 
<img width="3568" height="4172" alt="06-AUG-2021-PROTOCOLS" src="https://github.com/user-attachments/assets/bad6fd63-e854-4a98-bad3-4229afe8d62b" />

### Diagram - 2: OSI Model - Application Layer Protocol
<img width="3568" height="4172" alt="07-AUG-2021-MAIL-PROTOCOLS" src="https://github.com/user-attachments/assets/8200e550-0190-4dca-9c1c-1b288de83c8c" />
