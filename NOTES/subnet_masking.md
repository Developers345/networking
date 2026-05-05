# IP Address Structure and Classification

## Types of Addresses in an IP Address
There are **two types of addresses** within an IP address (due to hierarchical distribution):

1. **Network Address**
2. **Host Address**

---

## Problem
Given an IP address, how do we identify:
- Network portion?
- Host portion?

👉 By default, we **cannot determine** this because the bit allocation is not fixed.

---

## Solution: IP Address Classes
To solve this problem, **IP classes** were introduced.

IP addresses are classified into **5 classes**:
- Class A
- Class B
- Class C
- Class D
- Class E

---

## IP Class Identification

To determine the class of an IP address:
👉 Look at the **first octet (higher bits)**

| First Octet Range | Class   | Network Bits | Host Bits | Purpose |
|------------------|---------|--------------|-----------|---------|
| 0 – 126          | Class A | 8            | 24        | Large networks |
| 128 – 191        | Class B | 16           | 16        | Medium networks |
| 192 – 223        | Class C | 24           | 8         | Small networks |
| 224 – 239        | Class D | N/A          | N/A       | Multicast |
| 240 – 255        | Class E | N/A          | N/A       | Experimental |

---

## Special Case
- **127.x.x.x** → Loopback address  
  - Used for a system to communicate with itself

---

## Host Calculation Example

If **8 bits are allocated for host**:
```

2^8 = 256 total addresses
Usable hosts = 256 - 2 = 254

```

### Why subtract 2?
1. **Network Address** → First address (all host bits = 0)  
2. **Broadcast Address** → Last address (all host bits = 1)

---

## Broadcast Address

**Broadcasting** means:
> Sending data from one device to **all devices in the same network**

- Achieved by setting all host bits to **1**
- Example (Class C):
```

192.168.1.255

```

---

## Multicast (Class D)

- Used to send data to a **group of devices**
- IP range: **224.0.0.0 – 239.255.255.255**
- Not used for host/network division

---

## Subnet Mask

To identify network and host portions, **Subnet Mask** is used.

### Default Subnet Masks

- **Class A**  
```

11111111.00000000.00000000.00000000

```

- **Class B**  
```

11111111.11111111.00000000.00000000

```

- **Class C**  
```

11111111.11111111.11111111.00000000

```

---

## How Network Address is Derived

👉 Perform **bitwise AND** between:
- IP address  
- Subnet mask  

Result → **Network Address**

---

## Router Example (How Routing Works)

### Network 1
- 192.168.1.2  
- 192.168.1.3  
- 192.168.1.4  
- 192.168.1.5  

### Network 2
- 192.168.2.2  
- 192.168.2.3  
- 192.168.2.4  
- 192.168.2.5  

---

## Data Transfer Scenario

- Source: `192.168.1.2`  
- Destination: `192.168.2.5`

### Step-by-Step Flow

1. Sender sends data to **Switch**
2. Switch checks **MAC address (Layer 2)**
3. Destination not found in same network  
4. Switch forwards packet to **Router**
5. Router:
   - Uses **subnet mask** to identify network
   - Checks **routing table**
6. Router forwards packet to **destination network**
7. Packet reaches destination system

---

## Key Concepts

- IP address = **Network + Host**
- Subnet mask helps identify both parts
- Router uses:
  - Network address
  - Routing table  
  to forward packets correctly

---

## Conclusion

- IP classes define structure (network vs host bits)
- Subnet masks help in identifying network boundaries
- Routers use this information for **efficient data routing**


## Diagram - Subnet Mask
<img width="3568" height="4172" alt="01-SEP-2021-SUBNETMASK" src="https://github.com/user-attachments/assets/19dd0689-23b0-405e-9c16-6cb5bae3c560" />

