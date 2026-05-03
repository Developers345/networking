# Data Transfer Across Networks

## How does data transfer take place between computers across a network?

As discussed earlier, it is the **programs running on two machines** that exchange data—not the hardware devices themselves.

To exchange data over a network, we **cannot send symbolic or character representations directly**, because hardware devices can only understand data in terms of **on/off states**, represented as:

- `0` (off)
- `1` (on)

---

## Why Convert Data to Binary?

To transfer data over a network, we must first convert it into **binary format (0s and 1s)**. Only then can it be transmitted over physical communication channels.

---

## Encoding and Decoding

### 🔄 Encoding
The process of converting a **symbol or character into binary format** is called **Encoding**.

- A character must first be converted into a **decimal value**
- Then that decimal value is converted into **binary**

### 🔄 Decoding
At the receiver side:
- Binary → Decimal → Character/Symbol  
This reverse process is called **Decoding**

---

## Why Standard Encoding is Required?

For encoding and decoding to work correctly:
- Both sender and receiver must use the **same character-to-decimal mapping**

To ensure this, **Character Set Encoding Standards** are used.

---

## What are Character Set Encoding Standards?

Character Set Encoding Standards define:
- A **unique decimal value for each character**
- A **common standard** for encoding and decoding data across systems

---

## Common Character Encoding Standards

1. ASCII  
2. UTF-8  
3. UTF-16  
4. Unicode  
5. ISO-9001  

---

## Why Do We Need Multiple Encoding Standards?

### ASCII Limitations
- ASCII supports:
  - English characters
  - Numbers
  - Special symbols
- Range: `0 to 127` (7-bit standard)

### Bit Requirement in ASCII
- Minimum bits per character: **1**
- Maximum bits per character: **8**

### Example (ASCII Encoding)
```

SBI0143 → decimal → binary
01010011 01000010 01001001 00110000 00110001 00110100 00110011

```

---

## Supporting More Languages

To support more characters (like Hindi, Chinese, etc.), we need a **larger range**:
- Example: `0 to 65535` → used in **UTF-16**

---

## Choosing the Right Encoding Standard

Always choose encoding based on your use case:

- If working with **English only**:
  - Use **ASCII** or **UTF-8** (efficient, 1 byte per character)

- If working with **multiple languages**:
  - Use **UTF-16** or **Unicode**

---

## ⚠️ Important Note

Choosing an inappropriate encoding standard can lead to:
- ❌ Wastage of memory  
- ❌ Increased data transfer time  

---

## ✅ Summary

- Data is transmitted in **binary (0/1)**
- **Encoding** converts characters → binary  
- **Decoding** converts binary → characters  
- **Standards ensure consistency across systems**
- Choose encoding wisely for **efficiency and performance**


## Example for Convert SBI to binary using decimal number system

# 🔤 Step 1: ASCII Decimal Values

* S → **83**
* B → **66**
* I → **73**

---

# 🔢 Step 2: Decimal → Binary Calculation (Division by 2)

## ▶️ S = 83

Divide by 2 and note remainders:

```
83 ÷ 2 = 41  remainder 1
41 ÷ 2 = 20  remainder 1
20 ÷ 2 = 10  remainder 0
10 ÷ 2 = 5   remainder 0
5 ÷ 2  = 2   remainder 1
2 ÷ 2  = 1   remainder 0
1 ÷ 2  = 0   remainder 1
```

👉 Read remainders **bottom to top**:

```id="x1"
83 → 1010011 → (add leading 0) → 01010011
```

---

## ▶️ B = 66

```
66 ÷ 2 = 33  remainder 0
33 ÷ 2 = 16  remainder 1
16 ÷ 2 = 8   remainder 0
8 ÷ 2  = 4   remainder 0
4 ÷ 2  = 2   remainder 0
2 ÷ 2  = 1   remainder 0
1 ÷ 2  = 0   remainder 1
```

👉 Bottom to top:

```id="x2"
66 → 1000010 → (add leading 0) → 01000010
```

---

## ▶️ I = 73

```
73 ÷ 2 = 36  remainder 1
36 ÷ 2 = 18  remainder 0
18 ÷ 2 = 9   remainder 0
9 ÷ 2  = 4   remainder 1
4 ÷ 2  = 2   remainder 0
2 ÷ 2  = 1   remainder 0
1 ÷ 2  = 0   remainder 1
```

👉 Bottom to top:

```id="x3"
73 → 1001001 → (add leading 0) → 01001001
```

---

# 🔗 Final Answer

```id="final"
SBI → 01010011 01000010 01001001
```

---

## 🧠 Easy Trick (for exams/interviews)

* Keep dividing by **2**
* Write **remainders**
* Read **bottom → top**
* Make it **8 bits** by adding leading zeros



## Diagram - How does data transfer take place between computers across a network?
<img width="3568" height="4172" alt="03-AUG-2021-DATA-TRANSMISSION" src="https://github.com/user-attachments/assets/fabf6d11-2c13-4449-9fae-ed9b62ddfd15" />
