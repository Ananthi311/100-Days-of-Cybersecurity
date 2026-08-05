# Day 03 - Ports, TCP, UDP & TCP 3-Way Handshake

## 📌 Objective

Learn the fundamentals of Ports, TCP, UDP, and how a TCP connection is established using the TCP 3-Way Handshake.

---

## 📚 Topics Covered

- What is a Port?
- IP Address vs Port Number
- Common Port Numbers
- TCP (Transmission Control Protocol)
- UDP (User Datagram Protocol)
- TCP vs UDP
- TCP 3-Way Handshake
- Connection States (ESTABLISHED)
- Practical Windows Networking Commands

---

## 🔑 Key Concepts

### Common Ports

| Port | Protocol | Purpose |
|------|----------|---------|
| 53 | DNS | Domain Name Resolution |
| 80 | HTTP | Web Traffic |
| 443 | HTTPS | Secure Web Traffic |

---

### TCP

- Reliable communication
- Uses acknowledgements
- Retransmits lost packets
- Maintains packet order
- Uses the TCP 3-Way Handshake

---

### UDP

- Faster communication
- No acknowledgements
- No retransmission
- No connection establishment
- Commonly used for streaming, gaming, and VoIP

---

## 🔄 TCP 3-Way Handshake

1. **SYN** → Client requests a connection.
2. **SYN-ACK** → Server acknowledges and accepts the request.
3. **ACK** → Client confirms the response.

After the handshake, the connection enters the **ESTABLISHED** state, allowing reliable data transfer.

---

## 💻 Practical Commands

```cmd
netstat -an
```

Displays all active network connections and listening ports.

```cmd
netstat -ano
```

Displays active connections along with the Process ID (PID).

```cmd
tasklist
```

Lists all running processes.

```cmd
tasklist | findstr chrome
```

Filters the running processes to display only Google Chrome.

---

## 📷 Screenshots

Screenshots are available in the **screenshots/** folder.

- netstat -an
- netstat -ano
- tasklist
- tasklist | findstr chrome
- TCP 3-Way Handshake Flowchart

---

## 🎯 Key Takeaways

- IP Address identifies a device.
- Port Number identifies a service or application.
- TCP provides reliable communication.
- UDP prioritizes speed over reliability.
- TCP establishes connections using the 3-Way Handshake.
- Windows networking commands help analyze active connections and processes.
