# 🌐 Day 11 — URL Anatomy

## 📌 Overview

A URL (Uniform Resource Locator) is the address used to locate a resource on the internet.

Understanding URL anatomy is important for learning:

* 🌐 Networking
* 🔐 Cybersecurity
* 💻 Web Development
* 🛡️ Web Security
* 🔗 HTTP & APIs

---

## 1️⃣ What is a URL?

A URL tells the browser **where a resource is located and how to access it**.

Example:

```text
https://api.shop.com:8080/products?search=phone&page=2#reviews
```

---

## 2️⃣ URL Structure

A URL can contain several components:

```text
https://api.shop.com:8080/products?search=phone&page=2#reviews
  │     │      │   │       │          │                  │
  │     │      │   │       │          │                  └── Fragment
  │     │      │   │       │          └── Query Parameters
  │     │      │   │       └── Path
  │     │      │   └── Port
  │     │      └── Domain
  │     └── Subdomain
  └── Scheme / Protocol
```

---

## 3️⃣ Scheme / Protocol

Example:

```text
https://
```

The scheme tells the browser which protocol should be used.

### HTTP

```text
http://
```

HTTP sends data without encryption.

### HTTPS

```text
https://
```

HTTPS provides encrypted communication between the browser and server using TLS.

Commonly:

```text
HTTP  → Port 80
HTTPS → Port 443
```

---

## 4️⃣ Domain Name

Example:

```text
shop.com
```

The domain identifies the website/service we want to access.

A domain normally contains:

```text
shop.com
│    │
│    └── TLD
└── Domain name
```

Here:

* `shop` → domain name
* `.com` → Top-Level Domain (TLD)

---

## 5️⃣ Subdomain

Example:

```text
api.shop.com
```

Here:

```text
api → Subdomain
shop.com → Domain
```

Subdomains are commonly used to separate services.

Examples:

```text
www.example.com
api.example.com
mail.example.com
blog.example.com
```

---

## 6️⃣ Port

Example:

```text
:8080
```

A port identifies a specific network service running on a server.

Common ports:

| Port | Common Usage                |
| ---- | --------------------------- |
| 80   | HTTP                        |
| 443  | HTTPS                       |
| 22   | SSH                         |
| 21   | FTP                         |
| 25   | SMTP                        |
| 53   | DNS                         |
| 8080 | Common alternative web port |

Example:

```text
https://example.com:8080
```

Here `8080` is the port number.

---

## 7️⃣ Path

Example:

```text
/products
```

The path identifies the requested resource or endpoint.

Examples:

```text
/login
/products
/users
/about
/dashboard
```

For example:

```text
https://example.com/products
```

The browser is requesting the `/products` resource.

---

## 8️⃣ Query Parameters

Example:

```text
?search=phone&page=2
```

Query parameters provide additional information to the server.

Structure:

```text
?key=value&key=value
```

Example:

```text
?search=phone&page=2
```

Here:

```text
search = phone
page   = 2
```

Another example:

```text
/products?category=mobile&brand=apple
```

---

## 9️⃣ Fragment

Example:

```text
#reviews
```

A fragment usually identifies a specific section of a webpage.

Example:

```text
https://example.com/products#reviews
```

The browser can navigate directly to the `reviews` section.

### Important:

The fragment is generally handled by the browser and is **not normally sent to the server as part of the HTTP request**.

---

# 🔟 Complete URL Breakdown

Consider:

```text
https://api.shop.com:8080/products?search=phone&page=2#reviews
```

| Component | Value                 |
| --------- | --------------------- |
| Scheme    | `https`               |
| Subdomain | `api`                 |
| Domain    | `shop.com`            |
| Port      | `8080`                |
| Path      | `/products`           |
| Query     | `search=phone&page=2` |
| Fragment  | `reviews`             |

---

# 1️⃣1️⃣ URL → Server Flow

When we enter a URL in the browser:

```text
User
  ↓
Browser
  ↓
URL
  ↓
DNS Lookup
  ↓
IP Address
  ↓
Server
  ↓
HTTP Request
  ↓
HTTP Response
  ↓
Browser
```

### Step-by-step

### Step 1 — Enter URL

```text
https://example.com
```

### Step 2 — DNS Lookup

The browser needs the server's IP address.

Example:

```text
example.com
      ↓
DNS
      ↓
93.x.x.x
```

### Step 3 — Connect to Server

The browser connects to the server using the appropriate network protocol and port.

### Step 4 — Send HTTP Request

Example:

```http
GET /products HTTP/1.1
Host: example.com
```

### Step 5 — Server Responds

The server sends an HTTP response.

```text
HTTP Response
      ↓
Browser
      ↓
Webpage
```

---

# 1️⃣2️⃣ URL Security Basics 🔐

Sensitive information should not normally be placed in URLs.

### ❌ Avoid putting:

```text
password
API keys
access tokens
session secrets
sensitive personal information
```

Example of a bad practice:

```text
https://example.com/login?username=user&password=12345
```

URLs may be stored in:

* Browser history
* Server logs
* Proxy logs
* Analytics systems
* Bookmarks
* Monitoring systems

### ✅ Better approach

Use HTTPS and appropriate request mechanisms for sensitive data.

---

# 1️⃣3️⃣ Practical Learning 🛠️

I practiced URL inspection using:

### 🌐 Chrome

Used the browser address bar to inspect different URL components.

### 🛠️ Chrome DevTools

Useful tabs:

```text
DevTools
   ↓
Network
   ↓
Request
   ↓
Headers
   ↓
URL / Method / Status / Headers
```

### ⌨️ curl

Example:

```bash
curl https://example.com
```

Inspect response headers:

```bash
curl -I https://example.com
```

Verbose request:

```bash
curl -v https://example.com
```

These commands helped me understand what happens when a browser communicates with a web server.

---

# 🧠 Key Takeaways

After studying URL Anatomy, I learned:

* What a URL is
* Different URL components
* HTTP vs HTTPS
* Domain and subdomain
* Network ports
* URL paths
* Query parameters
* URL fragments
* DNS resolution
* HTTP request flow
* Basic URL security
* Practical URL inspection using Chrome DevTools and `curl`

---

# 🔄 Overall Concept

```text
URL
 │
 ├── Scheme
 ├── Subdomain
 ├── Domain
 ├── Port
 ├── Path
 ├── Query Parameters
 └── Fragment
        │
        ↓
       DNS
        ↓
    IP Address
        ↓
      Server
        ↓
  HTTP Request
        ↓
 HTTP Response
        ↓
     Browser
```

---

## 🚀 Next Learning Goal

**HTTPS Security**

Next, I will learn how HTTPS protects communication between the browser and the server using **TLS encryption**.

---

### 📚 Tools Used

* Google Chrome
* Chrome DevTools
* `curl`
* Browser Network Inspector

### 🏷️ Tags

`#CyberSecurity` `#Networking` `#WebSecurity` `#HTTP` `#HTTPS` `#URL` `#DevTools` `#curl` `#LearningInPublic`
