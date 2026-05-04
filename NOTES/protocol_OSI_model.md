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

# Application Protocol

Any two network applications that want to exchange data over a network must define a **standard message structure and semantics**. This ensures both applications can follow consistent rules and communicate in an understandable format. This is called an **Application Protocol**.

---

## Common Internet Applications & Protocols

In the internet world, many applications support our daily activities:

### 1. Web Browsing
- **HTTP (HyperText Transfer Protocol)**  
  Standard protocol used for accessing web pages over the World Wide Web.

---

### 2. Email Communication
Multiple protocols are used for email exchange between client and server:
- **SMTP (Simple Mail Transfer Protocol)** – Initial protocol with fewer features (used for sending emails)
- **POP3 (Post Office Protocol v3)** – Used to retrieve emails (downloads emails locally)
- **IMAP (Internet Message Access Protocol)** – Advanced protocol (syncs emails across devices)

---

### 3. File Transfer
- **FTP (File Transfer Protocol)** – Used to transfer files between a client and a server.

---

### 4. Remote Desktop Access
- **RDP (Remote Desktop Protocol)** – Used to connect and control another computer over a network.

---

## Standard Ports for Common Protocols

To ensure interoperability and ease of access, standard port numbers are predefined:

| Protocol | Port Number |
|----------|------------|
| FTP      | 20 / 21    |
| SSH      | 22         |
| SMTP     | 25         |
| HTTP     | 80         |
| HTTPS    | 443        |
| POP3     | 110        |
| IMAP     | 143        |
| RDP      | 3389       |

---

## Client-Server Communication

Any two programs communicating over a network must follow a standard application protocol.

### Types of Programs:
- **Server Program**
  - Runs on a specific port number
- **Client Program**
  - Connects to the server using `IP:Port`

---

## Why Application Protocols Are Needed

Different programs:
- Exchange different types of data
- Perform different operations

Therefore, each pair of communicating programs must define their own protocol. However, for commonly used applications, **standard protocols** are defined to ensure compatibility across vendors and platforms.

---

## Common Applications with Default Ports

- Web Browsing → HTTP (80)  
- Email:
  - SMTP (25)
  - POP3 (110)
  - IMAP (143)
- File Transfer → FTP (20/21)  
- Remote Desktop → RDP (3389)

---

## URL Format

To communicate with a server, the client uses a **URL**:

```

schema://ip:port/resource

```

### Components:
- **schema** → Protocol used (e.g., HTTP, FTP)
- **ip** → Server IP address
- **port** → Port number where the server is running
- **resource** → Specific resource on the server

### Note:
The client determines how to structure messages based on the **schema (protocol)** and sends them accordingly to the server.


### Diagram - Application Protocol
<img width="3568" height="4172" alt="09-AUG-2021-APP-PROTOCOLS" src="https://github.com/user-attachments/assets/6ce589ce-f14c-43b3-a400-72b55a4c0b30" />

