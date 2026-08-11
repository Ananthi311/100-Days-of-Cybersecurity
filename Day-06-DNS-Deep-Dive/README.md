# Day 06 – DNS Deep Dive

## 📚 Topics Covered

- DNS (Domain Name System)
- DNS Resolution
- DNS Resolver
- Root DNS Server
- TLD DNS Server
- Authoritative DNS Server
- DNS Records
- DNS Caching
- `nslookup` Practical

## 🌐 What is DNS?

DNS (Domain Name System) translates human-readable domain names into IP addresses.

Example:

```text
google.com → IP Address
DNS Resolution Flow
User
  ↓
DNS Resolver
  ↓
Root DNS Server
  ↓
TLD DNS Server (.com)
  ↓
Authoritative DNS Server
  ↓
IP Address
  ↓
Server Connection
📋 Common DNS Records
Record	Purpose
A	Domain → IPv4
AAAA	Domain → IPv6
CNAME	Alias for another domain
NS	Name Servers
MX	Mail Servers
🧪 Practical Commands
Basic DNS Lookup
nslookup google.com
A Record – IPv4
nslookup -type=A google.com
AAAA Record – IPv6
nslookup -type=AAAA google.com
NS Record – Name Servers
nslookup -type=NS google.com
MX Record – Mail Servers
nslookup -type=MX google.com
🗂️ DNS Caching

DNS responses can be cached at different levels:

Browser Cache
      ↓
OS DNS Cache
      ↓
DNS Resolver Cache
      ↓
DNS Server

Caching reduces repeated DNS lookups and improves performance.

🧠 Key Takeaways
DNS translates domain names into IP addresses.
DNS resolution can involve Resolver, Root, TLD and Authoritative DNS servers.
A → IPv4
AAAA → IPv6
NS → Name Servers
MX → Mail Servers
DNS caching helps reduce repeated lookups.
nslookup is useful for DNS queries and troubleshooting.
DNS is an Application Layer protocol.
🎯 Learning Outcome

Through this practical exercise, I gained a better understanding of how DNS works behind the scenes and how domain names are resolved into IP addresses.

I also practiced querying different DNS record types using nslookup.

Day 06 completed — continuing my cybersecurity and networking fundamentals journey. 🔐
