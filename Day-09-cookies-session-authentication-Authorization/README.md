# Day 9 — Cookies, Sessions & Authentication 🔐

Today I learned how Cookies, Sessions, and Authentication work together behind a website login.

## 🔄 Complete Flow

User Login
↓
Authentication
↓
Session Creation
↓
Session ID
↓
Set-Cookie
↓
Browser Stores Cookie
↓
Browser Sends Cookie with Requests
↓
Server Validates Session
↓
Access Granted / Denied

---

## 🧠 Key Concepts

### 1. Cookie 🍪

A cookie is small data stored by the browser.

The server can send a cookie using:

```http
Set-Cookie: session_id=ABC123

The browser stores it and can send it back in future requests:

Cookie: session_id=ABC123
2. Session 🔐

A session represents the user's authenticated state on the server.

Example:

Session ID: ABC123
User: User123
Status: Authenticated

The browser usually keeps the session identifier in a cookie.

3. Authentication vs Authorization

Authentication

Who are you?

Example:

Username + Password
        ↓
Server verifies identity
        ↓
Authentication successful ✅

Authorization

What are you allowed to do?

Example:

Normal User → View own profile ✅
Normal User → Admin settings ❌


Admin → Admin settings ✅
🛡️ Cookie Security Flags
HttpOnly

Prevents JavaScript from directly reading the cookie.

document.cookie
      ↓
HttpOnly cookie
      ↓
❌ Not accessible
Secure

Cookie is sent only over HTTPS.

HTTPS → Cookie ✅
HTTP  → Cookie ❌
SameSite

Controls how cookies behave in cross-site contexts.

Common values:

Strict → Most restrictive
Lax    → Balanced
None   → Cross-site cookies allowed
⏳ Session Expiration

A session doesn't remain valid forever.

Idle Timeout
No activity
    ↓
Timeout
    ↓
Session expires
Absolute Timeout
Session created
    ↓
Maximum lifetime reached
    ↓
Session expires

Even if the browser still has the old cookie, the server can reject the expired session.

🚪 Logout & Session Invalidation

Logout is more than just deleting a browser cookie.

Typical flow:

User clicks Logout
        ↓
Logout request
        ↓
Server invalidates session
        ↓
Cookie cleared / expired
        ↓
User requests protected page
        ↓
Session invalid ❌
        ↓
Login required
Important takeaway
Logout
=
Server-side Session Invalidation
+
Cookie Clearance/Expiration
🧪 Practical Commands
Check HTTP response headers
curl -I https://github.com
Observe HTTP → HTTPS redirect
curl -I http://github.com

Example:

HTTP/1.1 301 Moved Permanently
Location: https://github.com/
Check a 403 response
curl -I https://httpbin.org/status/403
Cookie practical
https://httpbin.org/cookies

I also used Chrome DevTools:

DevTools
   ↓
Network
   ↓
Request Headers
   ↓
Cookie

and:

DevTools
   ↓
Application
   ↓
Cookies
   ↓
HttpOnly / Secure / SameSite
🎯 What I understood today

The biggest takeaway from Day 9:

Login
  ↓
Authentication
  ↓
Session Creation
  ↓
Session ID → Cookie
  ↓
Browser stores Cookie
  ↓
Cookie sent with requests
  ↓
Server validates Session
  ↓
Access granted
  ↓
Logout
  ↓
Session invalidated
  ↓
Access denied

This helped me understand how browser-side cookies and server-side sessions work together to maintain authentication.

#Day9 #CyberSecurity #WebSecurity #Networking #HTTP #Cookies #Sessions #Authentication



**GitHub-க்கு இது better format** — headings, code blocks, flow diagrams எல்லாம் clean-aa render ஆகும்.
