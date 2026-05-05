# CIDR Notation (Classless Inter-Domain Routing)

In Class C IP addressing, 24 bits are allocated to the network and 8 bits are allocated to the host.  
This allows:
- Networks: 2^24  
- Hosts per network: 2^8 - 2 = 254 (usable)

Example problem:  
If I want to connect **2500 hosts within a network**, which IP class should I choose?

We should use **Class B**, where:
- Network bits: 16  
- Host bits: 16  

This allows:
- Networks: 2^16 ≈ 65,536  
- Hosts per network: 2^16 - 2 ≈ 65,534  

---

## Host Requirement Calculation

For **2500 hosts**, we need to determine the number of host bits:

- 2^11 = 2048 (not enough)  
- 2^12 = 4096 (sufficient)

So, **12 bits** are required for hosts.  
This means **4 bits (16 - 12)** are unused if we stick to Class B.

---

## Problem with Classful Addressing

Now consider this requirement:
- 2500 hosts per network  
- 75,000 networks required  

Using Class B:
- Maximum networks = 65,536 (not enough for 75,000)  
- Host bits = 16 (more than needed → waste of 4 bits)

We could:
- Use 12 bits for hosts (enough for 2500 hosts)
- Use remaining 4 bits for networks

But this is **not possible in classful addressing**, because:
- Network and host boundaries are fixed
- Bits cannot be reallocated

---

## Solution: CIDR Notation

To overcome this limitation, **CIDR (Classless Inter-Domain Routing)** was introduced.

### Key Advantages:
- Flexible allocation of network and host bits
- Efficient utilization of IP address space
- Eliminates wastage of unused bits
- Supports custom subnet sizes based on requirements

### Example:
Instead of fixed Class B (/16), we can use:
- `/20` → 12 bits for hosts (4096 addresses per network)

CIDR allows designing networks based on actual needs rather than rigid class boundaries.

# CIDR Notation

**CIDR** stands for **Classless Inter-Domain Routing**.

In traditional IP classification (classful addressing), there is **no flexibility** in allocating network and host bits. Because of this fixed allocation scheme, some bits often remain **unused**, leading to inefficient utilization of IP addresses.

---

## Why CIDR?

To overcome these limitations, **CIDR notation** was introduced.

### Advantages:
- Flexible allocation of network and host bits
- Efficient use of IP address space
- Eliminates wastage of unused bits
- Supports custom subnetting based on requirements

---

## CIDR Representation

In CIDR notation, an IP address is represented using the format:

```

IP_Address / Network_Bits

```

### Example:

```

192.168.45.32/22

```

- `/22` indicates that **22 bits are allocated to the network**
- The remaining bits are used for **hosts**

---

## What to Do Next?

To determine:
- **Network Address**
- **Host Range**
- **Broadcast Address**

We need to:
1. Convert `/22` into a **subnet mask**
2. Perform calculations based on that subnet mask




## Summary

| Feature                  | Classful Addressing | CIDR Addressing |
|--------------------------|--------------------|-----------------|
| Bit allocation           | Fixed              | Flexible        |
| Address utilization      | Inefficient        | Efficient       |
| Custom subnet sizes      | Not possible       | Possible        |
| Real-world usage         | Obsolete           | Widely used     |

## Diagram - CIDR Notation - 1
<img width="3568" height="4172" alt="02-SEP-2021-CIDR" src="https://github.com/user-attachments/assets/baafc51d-d517-4fd6-98ea-ba475f9960fe" />

## Diagram - CIDR Notation - 2
<img width="3568" height="4172" alt="03-SEP-2021-CIDR" src="https://github.com/user-attachments/assets/af2fa080-3424-407e-a4ec-488685a99982" />
