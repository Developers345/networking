# IP Address Standards

## What is an IP Address?
An **IP (Internet Protocol) address** is a unique identifier assigned to each computer or device connected to a network.

## Why Do We Need an IP Address?
- To **identify** each device uniquely on a network  
- To enable **communication** between devices  
- To ensure data is sent to the **correct destination**

## Key Point
For every computer or device connected over a network, an **IP address is required** to:
- Identify the device  
- Establish communication  
- Transfer data across the network  

## Simple Definition
> An IP address is a unique logical address assigned to each device in a network for identification and communication.

# IP Addressing: Signed vs Unsigned

## Overview
An **IP (Internet Protocol) address** is a logical identifier assigned to each device on a network.  
IP addresses are used for **identification** and **communication** between devices.

> **Important Concept:**  
IP addresses are always treated as **unsigned values**.

---

## Why IP Addresses Are Unsigned

### 1. No Negative Values
- IP addresses represent **identifiers**, not quantities for arithmetic.
- Negative values (e.g., -1, -128) have **no meaning** in networking.
- Therefore, only **non-negative values (0 and above)** are valid.

---

### 2. Full Utilization of Bits
- In unsigned representation, **all bits are used for value**
- In signed representation, **1 bit is reserved for sign**

👉 Using unsigned allows **maximum range of values**

---

## IPv4 Addressing (32-bit)

### Structure
- IPv4 address = **32 bits (4 bytes)**
- Each byte is called an **octet**
- Each octet range: **0 to 255**

### Example
```

192.168.1.1

```

### Range
- Minimum: `0.0.0.0`
- Maximum: `255.255.255.255`

### Internal Representation
- Stored as a **32-bit unsigned integer**

---

### Why Not Signed?

| Type              | Range (8-bit)        | Valid for IP? |
|------------------|----------------------|---------------|
| Signed Integer    | -128 to 127          | ❌ No         |
| Unsigned Integer  | 0 to 255             | ✅ Yes        |

👉 IP requires **0–255**, which is only possible with **unsigned**

---

## IPv6 Addressing (128-bit)

### Structure
- IPv6 address = **128 bits**
- Represented in **hexadecimal format**

### Example
```

2001:0db8:85a3:0000:0000:8a2e:0370:7334

```

### Internal Representation
- Stored as a **128-bit unsigned value**

---

## Key Differences: Signed vs Unsigned (In Context of IP)

| Feature              | Signed Integer         | Unsigned Integer       | IP Address Usage |
|---------------------|------------------------|------------------------|------------------|
| Negative values      | Allowed                | Not allowed            | Not used         |
| Bit usage            | 1 bit for sign         | All bits for value     | Uses all bits    |
| Value range          | Smaller                | Larger                 | Needs larger     |
| Suitability for IP   | ❌ Not suitable        | ✅ Suitable            | ✔ Used           |

---

## Important Notes
- IP addresses are **not meant for arithmetic operations**
- They are treated as **logical identifiers**
- Internally handled as **unsigned binary numbers**
- Even if a programming language does not support unsigned types (e.g., Java), special handling is used

---

## Interview Summary (Short Answer)

> IP addresses are always **unsigned values** because they represent identifiers and cannot be negative. IPv4 uses 32-bit unsigned integers, while IPv6 uses 128-bit unsigned integers.

---

## Conclusion
- IP addressing uses **unsigned representation**
- This ensures:
  - No negative values  
  - Maximum usable range  
  - Proper identification of devices  



## Diagram - IP-Addressing
<img width="3568" height="4172" alt="27-AUG-2021-IPADDRESSING" src="https://github.com/user-attachments/assets/6d888335-aa6c-417e-91fe-6bbc88bd0aaa" />

## Diagram - IP-Addressing - divided hirachical 
<img width="3660" height="5764" alt="30-AUG-2021" src="https://github.com/user-attachments/assets/92342c98-9ad1-4e5d-b965-a0b157093e48" />

# IP Addressing

## Types of IP Addresses
There are **two types of IP addresses**:

1. **IPv4**
   - 32-bit in length  
   - Can accommodate approximately **4.2 billion devices**  

2. **IPv6**
   - 128-bit in length  
   - Written in **hexadecimal format**  
   - Can accommodate **2^128 - 2 addresses**, which is practically unlimited  

---

# IPv4 Addressing

## Structure
An IPv4 address is:
- **32 bits long**
- Divided into **4 octets (each 8 bits)**
- Separated by a dot (`.`)

Example:
```

192.168.1.1

```

---

## Hierarchical Addressing Model
IPv4 uses a **hierarchical addressing model** to organize networks efficiently.

We group related computers into a **network**, and manage each network separately.

An IP address consists of two parts:

### 1. Network Address
- Identifies the **network/group of computers**
- Formed using a portion of the IP address (some bits or octets)

### 2. Host Address
- Identifies a **specific computer within a network**
- Assigned as a unique number within that network

---

## Example: Network and Host Split

If:
- **3 octets** are used for the network  
- **1 octet** is used for hosts  

### Hosts per Network
```

2^8 = 256 addresses
Usable hosts = 254 (excluding network and broadcast)

```

### Number of Networks
```

255 × 255 × 255 networks

```

---

## Organizational Example

Suppose an organization wants to create **3 separate networks**:

- Finance Department → One network  
- HR Department → Another network  
- Employees → Separate network  

### Purpose
- Apply **security and traffic restrictions**
- Control access between departments

### Example Policies
- Finance → No access to public internet (confidentiality)  
- Finance & HR → Access to employee data  
- Employees → Limited internet access  

---

## Example IP Allocation

| Network Address | Host Range | Department |
|---------------|-----------|------------|
| 192.168.1.x   | 1–254     | Finance    |
| 192.168.2.x   | 1–254     | HR         |
| 192.168.3.x   | 1–254     | Employees  |

---

## Key Concept: Host Capacity

Number of hosts depends on how many bits are allocated:

- **More network bits → More networks, fewer hosts**
- **More host bits → Fewer networks, more hosts**

---

## Example: Large Organization

If an organization has **3000 employees**:

- Use **2 octets for network**
- Use **2 octets for hosts**

### Result:
- Networks: ~65,000  
- Hosts per network: ~65,000  

---

## Problem: Identifying Network vs Host

Given an IP:
```

192.168.1.2

```

👉 Can we identify:
- Network address?
- Host address?

❌ **No**, because:
- Bit allocation is **not fixed**

---

## Solution: Classful IP Addressing

To solve this, **IP classes** were introduced.

### Classes of IP Addresses
There are **5 classes**:

- Class A  
- Class B  
- Class C  
- Class D  
- Class E  

These classes define:
- Which bits belong to the **network**
- Which bits belong to the **host**

---

## Conclusion
- IPv4 uses a **hierarchical structure**
- IP address = **Network + Host**
- Allocation depends on **network size**
- Classful addressing helps identify structure easily


## Diagram - Classifcation of IP Addressing
<img width="3568" height="4172" alt="31-AUG-2021-IPCLASSES" src="https://github.com/user-attachments/assets/622fd037-cca9-42f8-b79d-78ba6c5c3a04" />

## 📡 Broadcast vs Multicast

### 📢 Broadcast Communication

![Image](https://images.openai.com/static-rsc-4/Jns7MJAWRVhC7GfmvNway7xcT4ysLimpjiAMixFUPmeqq2V8D8WPG4B9je7ky3DxUkwEqNgpYundCs4RfL-qDIHAsrlP5pHkufOLZHTQW9sh7DmTh30Yz-Dsx1nfnqJ_XbtkeUi47--y1bhQgdBj_DXKIIaByj7iCEVeIetKr-QszkR7gl-FJR9JW-HxnBkA?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/7tyNM0YXC1sJ6cIBFDgcitVfxebQwtktAFvoYVqQiwMNSO2xRHAXqj_H4zdX12DssqHYY7OXLgJwnl7A0V1oC9ntFbj7MY0GBjrnAZO6E593MLU40tPxXCZLn5xcX6gbSEC3nQ1IhgHIwJaxZQ9-8K4aJgrj_ll_3deKBtIWSrcA4TwAhkpww4UzTV0UO-zi?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/u2Csm4SqpjUBroX_-1FngVjJmuXv6sWgPzBL0OGs4VYfgvjQCnSrPwH4N9vEDLRNe2j-d6PFQ5hAYTnBnkpUV3YbpKv1a5Qa86J9ukHQ_7GNLfoSyTcb1OjbSpzeXElqo60I6WUg-SP37gafbZTUzMbt043Ig5edLBCMvjXfrcL0DwBIMbjd1Zi5jz1yip2W?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/FIW8JUrKlQuoDJ_v_JUd05FS6CDDeDH5WHahVJNB2mdTeaeG3O5z72TgBxuZCV9YY1GHCpRoHYfQhXW_i-N_-HlsMbGf6xBvghew9_i-yUybJrfpZJo1eV-yVLKqoVz19jPQl7oxJEIrtffBRqM5Id1TDbNyb4RPYRdxXIjDyBFA_mJtRWL5loe3DNLYfqfY?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/6Wcc41NmDwp9-vCuF23zlGXS86idyps2U2sXKdcDKsjsc8eQ2PPy06YhY3NQzwiWMulmSnZCuu_ZiG2cfbSubaCqhx6djENBVKiWcI3gYTup97iI-Ws-LlcagSABTD4eHWEwTczFtageUcaHQkXQqNc-LVvTJ7Ec823ShuIxJyIWe74rGHxOY4dhrTMOosBJ?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/463c3y--edq732ykkAryDgrvBu9duxq_jQQ-Ge2Nhp7s8qNndH-fsVoDauje0k-8PDXq5_SXqg1nUmd0GSE_COvZYRliTfiyB23CU6rcLSDdPr4lMvp4q6fYKLMW9s0i_H9MBzINR6Od3pQHiBY5o4ChJrvvHMTOOHTkELH5jNttN4friXOGMOS5UT0RdtPM?purpose=fullsize)

**Broadcast** means sending data from **one device to all devices** in the same network.

### Key Points

* One sender → **All receivers**
* Uses special address: **255.255.255.255** (IPv4 broadcast)
* Every device in the network **receives and processes** the packet
* Works only within a **local network (LAN)**

### Example

* ARP (Address Resolution Protocol) request
* “Who has this IP?” message sent to all devices

---

### 👥 Multicast Communication

![Image](https://images.openai.com/static-rsc-4/TbUU4jUVVYnQzbwrJrXtZqudIuG6fYzqmRW5hsOHqGOe1DMSX0sjKZuovHsw14P6x0SVOmOJ3DC7ThWshk5Yd7wfaXDXK61BsQSD1jYbpYGYItOkTUyB-EiuFH-eWkpYNjgsXieIdZxBSx_vhfSOh0jCvgkKbJ8iwmZZ4dePikIRqOBl5kagjKVWxHG-A1um?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/khBNCxX3je9VZrJhMVzf4bnSHwpsznP1cXRwhFvbPgbFWcrJFUzWkW5ERJyVJhHhpzsTJ5_ELtU8vbZmqw9d0U2Y2eCMvPsvorTemqfVXDDx5Oo_ilOdJ_D7711gPFRW-7AX1XmmuEfw_gmOek2fVCdCAm7Z70DMF7Yj1gg4Z687mdvBqYU9vzVVddsrKcZk?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/7tyNM0YXC1sJ6cIBFDgcitVfxebQwtktAFvoYVqQiwMNSO2xRHAXqj_H4zdX12DssqHYY7OXLgJwnl7A0V1oC9ntFbj7MY0GBjrnAZO6E593MLU40tPxXCZLn5xcX6gbSEC3nQ1IhgHIwJaxZQ9-8K4aJgrj_ll_3deKBtIWSrcA4TwAhkpww4UzTV0UO-zi?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/H2DEfZ4RXq_M24H0BSxH7cyrB6o2J5PDymhPZJdkEFmIAU6Dlkl5v3acOPxi_RHx_IVcKeSKihb0Iv_i_Ma48bwrPcjaA5199ZZJaBAzknak1KYm-Zq3W2TIDEPOLAWeo_fJFEpSvV41UWPetmC1hLqi3MUe9EAAjuOak1inhutdsifz5wACAdjNQg6d2GrM?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/az4wuKEjySIwycqz-_hebT4aJ9q6nVCxP6Ds14l7XCW6WbhNjv3FajtSHdHmD8XDlhqDx8RlmY-nb4gb_QmM37el6AOh39MZbJN9QvKMX0zx7I1vGQuvct9CAmNdOtdXi-wzvdl9wwR5D8mmLZcMR2g9sybDo7sR05uSV23Anzpq4a44-7nV9KflkXvNf2wI?purpose=fullsize)

**Multicast** means sending data from **one device to a selected group of devices**.

### Key Points

* One sender → **Specific group of receivers**
* Uses IP range: **224.0.0.0 to 239.255.255.255**
* Only devices that **join the group** receive the data
* Efficient — avoids unnecessary traffic

### Example

* Live video streaming
* Online gaming updates
* Stock market data distribution

---

## ⚖️ Difference Between Broadcast and Multicast

| Feature       | Broadcast           | Multicast                      |
| ------------- | ------------------- | ------------------------------ |
| Communication | One → All           | One → Selected group           |
| Efficiency    | Less efficient      | More efficient                 |
| Network load  | High                | Low                            |
| IP Range      | 255.255.255.255     | 224.0.0.0 – 239.255.255.255    |
| Usage         | Small networks, ARP | Streaming, group communication |


## 🔢 Total Addresses: `2^8 = 256`

When you allocate **8 bits for the host portion** of an IP address:

* Each bit can be **0 or 1**
* Total combinations = **2⁸ = 256**

👉 So, you get **256 total IP addresses** in that network.

---

## ⚠️ Why Only 254 Usable Hosts?

Out of those 256 addresses, **2 are reserved** and **cannot be assigned to devices**.

### 1. Network Address (First Address)

* All host bits = `0`
* Identifies the **network itself**
* Example: `192.168.1.0`

👉 Used by routers to identify the network
❌ Cannot assign to a computer

---

### 2. Broadcast Address (Last Address)

* All host bits = `1`

* Used to send data to **all devices in the network**

* Example: `192.168.1.255`

👉 Sends message to everyone
❌ Cannot assign to a computer

---

## 🧮 Final Calculation

* Total addresses = **256**
* Reserved:

  * 1 Network address
  * 1 Broadcast address

👉 **256 - 2 = 254 usable host addresses**

---

## 📊 Example

| Type              | Address                     |
| ----------------- | --------------------------- |
| Network Address   | 192.168.1.0                 |
| Usable Hosts      | 192.168.1.1 – 192.168.1.254 |
| Broadcast Address | 192.168.1.255               |

---

## 🧠 Simple Way to Remember

* First address → Network
* Last address → Broadcast
* Everything in between → Usable hosts


