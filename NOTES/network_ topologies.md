# Network Topologies

The way computers are interconnected over a network is called **Network Topology**.

## Types of Network Topologies

There are two types of network topologies:

1. **Logical Topology**
   - Defines how data moves between computers over the network.

2. **Physical Topology**
   - Defines how computers are physically arranged and interconnected.

---

## Types of Physical Topologies

There are five main types of physical network topologies:

1. Bus Topology  
2. Ring Topology  
3. Star Topology  
4. Mesh Topology  
5. Hybrid Topology  

---

## 1. Bus Topology

A **backbone cable** runs through the entire network, and all computers are connected (tapped) into this cable.

- When a computer sends data, it places the data packet onto the backbone cable.
- The data travels sequentially from one end to the other.
- Each computer checks if the data belongs to it; if not, it forwards the data.

### Advantages

- Low cost of setup  
- Quick to install  
- Easy troubleshooting and fault detection  

### Disadvantages

- Not suitable for large networks  
- Signal degradation with more devices  
- High chance of data collision  
- Low security  
- If the backbone cable fails, the entire network fails  

### Use Case

- Suitable for small networks (e.g., home networks)

---

## 2. Ring Topology

In a **Ring Topology**, each computer is connected to its adjacent computers, forming a circular structure.

- Each computer requires **2 Network Interface Cards (NICs)**  
- Data flows in a **single direction (clockwise)**  
- Low chance of data collision  

### Limitation

- Data must pass through all intermediate nodes to reach the destination  
- This slows down communication  

### Dual Ring Topology (Improvement)

- Each computer is connected using **two wires (rings)**:
  - One for clockwise direction  
  - One for anti-clockwise direction  
- Data can travel in both directions  
- Improves speed and reliability  

### Advantages

- Supports larger networks  
- No data collisions  
- Easy to add/remove nodes  

### Disadvantages

- High setup cost  
- Failure of one node affects the network  
- Troubleshooting is difficult  

---

## 3. Star Topology

All computers are connected to a central device called a **Hub**.

- A computer sends data to the hub  
- The hub forwards data to all connected devices  
- Uses duplex cables for better performance  

### Advantages

- Low cost  
- Easy to set up  
- Easy to add/remove devices  
- Failure of one node does not affect others  
- No data collision  
- Easy troubleshooting  

### Disadvantages

- If the hub fails, the entire network fails  

---

## 4. Mesh Topology

Each computer is connected to **every other computer** (n-1 connections).

- Provides multiple paths for data transmission  
- Highly reliable and robust  

### Advantages

- Very robust network  
- High data transfer speed  
- No data collision  

### Disadvantages

- Very expensive  
- Complex setup  
- Difficult troubleshooting  
- Suitable mainly for WAN (Wide Area Networks)  

---

## 5. Hybrid Topology

A **Hybrid Topology** is formed by combining two or more different topologies.

- Example: Star + Bus, Star + Ring  

---

## Summary

| Topology | Cost | Reliability | Speed | Complexity |
|----------|------|------------|-------|-----------|
| Bus      | Low  | Low        | Medium| Low       |
| Ring     | Medium | Medium   | Medium| Medium    |
| Star     | Low  | High       | High  | Low       |
| Mesh     | High | Very High  | Very High | High |
| Hybrid   | Varies | High     | High  | High      |


## Diagram - Network Topologies
<img width="3568" height="4172" alt="16-AUG-2021-NETWORK-TOPOLOGIES" src="https://github.com/user-attachments/assets/442edc45-fc80-429d-a536-0c4b5b32b440" />
