# Day 04 - OSI Model (Open Systems Interconnection)

## 📌 Objective

Understand the OSI Model and how data travels through its seven layers during network communication.

---

## 📚 Topics Covered

- What is the OSI Model?
- The 7 Layers of the OSI Model
- Responsibilities of each layer
- Encapsulation & Decapsulation
- Mapping real networking concepts to OSI layers
- Practical Windows networking commands

---

## 🌐 OSI Model

| Layer | Name | Responsibility |
|-------|------|----------------|
| 7 | Application | User-facing applications and network services |
| 6 | Presentation | Encryption, decryption, compression |
| 5 | Session | Establishes, manages, and terminates sessions |
| 4 | Transport | Reliable communication, TCP/UDP, Port Numbers |
| 3 | Network | IP Addressing and Routing |
| 2 | Data Link | MAC Addressing and Frame Delivery |
| 1 | Physical | Transmission of bits over cables or wireless media |

---

## 🔄 Real-World Example

Opening **https://google.com**

Application
- Chrome creates the request.
- DNS resolves the domain name.

Presentation
- TLS encrypts the data.

Session
- Communication session is established.

Transport
- TCP performs the 3-Way Handshake.
- Source and Destination Port Numbers are used.

Network
- Source and Destination IP Addresses are added.

Data Link
- Source and Destination MAC Addresses are added.

Physical
- Data is transmitted as Wi-Fi or Ethernet signals.

---

## 📦 Encapsulation

Application Data

↓

Transport Header (TCP/UDP)

↓

Network Header (IP)

↓

Data Link Header (MAC)

↓

Physical Layer (Bits)

At the receiver, the reverse process is called **Decapsulation**.

---

## 💻 Practical Commands

```cmd
ipconfig /all
```

Displays detailed network configuration, including:
- IPv4 Address
- MAC Address
- DNS Server
- Default Gateway

```cmd
getmac
```

Displays the MAC Address of the network adapters.

```cmd
arp -a
```

Displays the ARP cache, showing the mapping between IP Addresses and MAC Addresses.

---

## 📷 Screenshots

- OSI Model Flowchart
- ipconfig /all
- getmac
- arp -a

---

## 🎯 Key Takeaways

- The OSI Model provides a structured approach to understanding network communication.
- Each layer has a specific responsibility.
- TCP, UDP, and Port Numbers operate at the Transport Layer.
- IP Addresses operate at the Network Layer.
- MAC Addresses operate at the Data Link Layer.
- Encapsulation adds headers as data moves down the OSI layers.
- Decapsulation removes headers as data reaches the destination.

---

## 🚀 Progress

- ✅ Day 01 - Networking Basics
- ✅ Day 02 - Private IP, Public IP & NAT
- ✅ Day 03 - Ports, TCP, UDP & TCP 3-Way Handshake
- ✅ Day 04 - OSI Model

Stay tuned for **Day 05 - TCP/IP Model & OSI vs TCP/IP Comparison**.
