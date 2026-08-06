# 🌐 Day 2 - Private IP, Public IP & NAT

## 📖 Objective

Understand how devices communicate with the Internet using Private IP, Public IP, and Network Address Translation (NAT).

---

## 📚 Topics Covered

- Private IP Address
- Public IP Address
- NAT (Network Address Translation)
- Source IP
- Destination IP
- Packet Flow
- Gateway
- DNS Recap

---

## 🧠 What I Learned

### Private IP
A Private IP is used for communication inside a local network.

Example:
10.254.xxx.x

---

### Public IP
A Public IP is assigned by the Internet Service Provider (ISP) and is visible on the Internet.

Example:
42.xxx.xxx.xxx

---

### NAT

NAT translates the private IP address into a public IP address before sending packets to the Internet.

Without NAT, private IP addresses cannot communicate directly over the Internet.

---

## 🌍 Packet Flow

Laptop

↓

DNS Request

↓

Gateway (Mobile Hotspot)

↓

Vodafone Network

↓

NAT

↓

Google Server

↓

Response

↓

NAT

↓

Laptop

---

## 💻 Practical Commands

```cmd
ipconfig

tracert google.com

netstat -n

arp -a
```

## 🎯 Practical Completed

- Checked Private IP
- Checked Default Gateway
- Observed Active Connections
- Traced packet path to Google
- Understood NAT packet translation

---

## 🔑 Key Takeaways

- Google never sees my private IP.
- NAT translates the Source IP.
- DNS resolves domain names into IP addresses.
- Every Internet request passes through NAT before reaching public servers.

---

## ✅ Status

Day 2 Completed
