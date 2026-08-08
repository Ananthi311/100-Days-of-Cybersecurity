Day 05 – TCP/IP Model & OSI vs TCP/IP
📚 Topics Covered
TCP/IP Model
TCP/IP 5 Layers
OSI Model vs TCP/IP Model
IP Addressing
TCP, UDP & Port Numbers
MAC Address
Routing
ICMP
Network troubleshooting commands
🌐 TCP/IP Model

The TCP/IP model consists of 5 layers:

Layer	Main Concepts	Examples
Application	Application-level communication	HTTP, HTTPS, DNS
Transport	End-to-end communication	TCP, UDP, Ports
Internet	Addressing and routing	IP, ICMP
Network Access	Local network communication	MAC, Ethernet, Wi-Fi
🔄 OSI vs TCP/IP
OSI Model                  TCP/IP Model

Application ───────┐
Presentation       ├────→ Application
Session ───────────┘

Transport ─────────────→ Transport

Network ───────────────→ Internet

Data Link ────────┐
Physical ─────────┴────→ Network Access

The OSI model has 7 layers, while the TCP/IP model commonly uses 5 layers. Multiple OSI layers are combined into single TCP/IP layers.

🔐 Web Request Flow

A simplified view of an HTTPS request:

HTTPS
  ↓
TCP + Port 443
  ↓
IP Address
  ↓
MAC Address / Wi-Fi

This helped me understand how application data moves through different networking layers.

🧪 Practical Commands
1. Ping
ping google.com

Used to test network reachability and observe ICMP-based communication.

2. Tracert
tracert google.com

Used to observe the network path/hops toward a destination.

3. Nslookup
nslookup google.com

Used to query DNS and resolve a domain name to IP information.

4. IP Configuration
ipconfig /all

Used to view network configuration such as:

IPv4 address
Subnet mask
Default gateway
DNS server
Network adapter information
🧠 Key Takeaways
Application → HTTP, HTTPS, DNS
Transport → TCP, UDP, Ports
Internet → IP, Routing, ICMP
Network Access → MAC, Ethernet, Wi-Fi
OSI and TCP/IP are different models used to understand networking communication.
Networking commands can help connect theoretical concepts with real system behavior.
🎯 Learning Outcome

I gained a better understanding of how the TCP/IP model maps to the OSI model and how common networking protocols and troubleshooting commands fit into different layers.

Day 05 completed — continuing my cybersecurity and networking fundamentals journey. 🔐
