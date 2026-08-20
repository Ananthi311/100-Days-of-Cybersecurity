
Day 10 — HTTP Methods & API Requests
📌 Overview

HTTP is the protocol used for communication between a client (browser/app) and a server.

A typical flow looks like:

Client
   ↓
HTTP Request
   ↓
Server
   ↓
Application Logic / Database
   ↓
HTTP Response
   ↓
Client
🌐 HTTP Methods

HTTP methods tell the server what action the client wants to perform.

Method	Purpose	Example
GET	Retrieve data	GET /users
POST	Send/create new data	POST /users
PUT	Fully update a resource	PUT /users/1
PATCH	Partially update a resource	PATCH /users/1
DELETE	Request removal of a resource	DELETE /users/1
📤 HTTP Request Structure

An HTTP request can contain:

Method
URL / Path
Query Parameters
Headers
Request Body (when required)

Example:

GET /products?q=phone HTTP/1.1
Host: example.com
Accept: application/json
User-Agent: Mozilla/5.0
Breakdown
GET              → HTTP Method
/products        → Path
?q=phone         → Query Parameter
Host             → Header
Accept           → Header
📥 HTTP Response Structure

A server response usually contains:

Status Code
Response Headers
Response Body

Example:

HTTP/1.1 200 OK
Content-Type: application/json


{
  "message": "Success"
}
Breakdown
200 OK                    → Status Code
Content-Type              → Response Header
{"message":"Success"}     → Response Body
🔢 Common HTTP Status Codes
Status Code	Meaning
200	OK / Successful
201	Created
400	Bad Request
401	Unauthorized
403	Forbidden
404	Not Found
500	Internal Server Error
🔄 Complete HTTP Communication Flow
Browser / App
      │
      │ HTTP Request
      │
      ▼
┌─────────────────────┐
│ Method              │
│ URL / Path          │
│ Headers             │
│ Query Parameters    │
│ Body (if required)  │
└──────────┬──────────┘
           │
           ▼
        Server
           │
           ▼
 Application Logic
           │
           ▼
        Database
           │
           ▼
┌─────────────────────┐
│ HTTP Response       │
│                     │
│ Status Code         │
│ Headers             │
│ Response Body       │
└──────────┬──────────┘
           │
           ▼
      Browser / App
🧪 Basic curl Practical

Retrieve a resource:

curl https://example.com

View response headers:

curl -I https://example.com

Send a POST request with JSON data:

curl -X POST https://httpbin.org/post \
-H "Content-Type: application/json" \
-d "{\"name\":\"test\"}"
🔐 Security Perspective

Understanding HTTP communication is important in cybersecurity because many security mechanisms and vulnerabilities involve HTTP requests and responses.

Examples include:

Authentication
Authorization
Cookies and Sessions
API Security
Request Headers
Input Validation
Access Control
🧠 Key Takeaway

HTTP methods define what action the client requests, while HTTP requests and responses carry the data required for communication between the client and server.
