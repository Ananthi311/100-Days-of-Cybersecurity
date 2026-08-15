
# Day 08 - HTTP, HTTPS & Web Communication

## 📌 Overview

Today, I learned the basics of how web communication works between a client and a web server.

I explored HTTP and HTTPS, HTTP requests and responses, common HTTP methods, status codes, and response headers using practical commands.

---

## 🌐 HTTP vs HTTPS

- **HTTP** → Used for communication between a client and a web server.
- **HTTPS** → HTTP communication secured using TLS encryption.

Common ports:

- HTTP → Port 80
- HTTPS → Port 443

---

## 🔄 Web Communication Flow

```text
User
  ↓
Browser / Client
  ↓
DNS resolves Domain Name → IP Address
  ↓
TCP Connection
  ↓
HTTP/HTTPS Request
  ↓
Web Server
  ↓
HTTP Response
  ↓
Status Code + Headers + Content
  ↓
Browser displays the webpage
📤 HTTP Methods
GET

Used to retrieve data from a server.

Example:

Client → GET Request → Server
POST

Used to send data to a server.

Example:

Username + Password
        ↓
POST Request
        ↓
Web Server
📊 HTTP Status Codes
Status Code	Meaning
200	OK - Request successful
301	Moved Permanently
403	Forbidden
404	Not Found
500	Internal Server Error
🧪 Practical Commands
Check HTTP Response Headers
curl -I https://example.com

Observed:

HTTP/1.1 200 OK
Content-Type: text/html
Server: cloudflare
Test a Non-Existing Page
curl -I https://example.com/this-page-does-not-exist

Observed:

HTTP/1.1 404 Not Found
Test HTTP to HTTPS Redirect
curl -I http://github.com

Observed:

HTTP/1.1 301 Moved Permanently
Location: https://github.com/
Test Forbidden Access
curl -I https://httpbin.org/status/403

Observed:

HTTP/1.1 403 FORBIDDEN
🧠 Understanding Response Headers

Some important headers observed during the practical:

Content-Type → Type of content returned by the server.
Server → Information about the server or infrastructure handling the response.
Last-Modified → Indicates when the resource was last modified.
Location → Specifies the new URL during a redirect.
Strict-Transport-Security → Helps enforce HTTPS connections.
Content-Security-Policy → Controls which resources a webpage is allowed to load.
🎯 Key Takeaway
Client
  ↓
HTTP/HTTPS Request
  ↓
Web Server
  ↓
HTTP Response
  ↓
Status Code + Headers + Content

Understanding HTTP communication is an important foundation for web development, networking, and cybersecurity.

🚀 Day 08 Completed

Topics covered:

HTTP vs HTTPS
TLS encryption basics
HTTP GET and POST methods
HTTP Request and Response
HTTP Status Codes
200, 301, 403, 404 and 500
HTTP Response Headers
Practical usage of curl


Now I'll create a clean **Day 8 flowchart image** suitable for your GitHub and LinkedIn post.  
