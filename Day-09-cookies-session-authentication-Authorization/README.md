Day 9 — Cookies, Sessions & Authentication 🔐

Today I learned how Cookies, Sessions, and Authentication work together behind a website login.

🔄 Complete Flow
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
Key Concepts
Cookie 🍪

A cookie is small data stored by the browser.
Set-Cookie: session_id=ABC123
The browser stores it and sends it with future requests:
Cookie: session_id=ABC123
Session 🔐

A session represents the user's authenticated state on the server.
Session ID: ABC123
User: User123
Status: Authenticated
Authentication vs Authorization

Authentication → Who are you?

Authorization → What are you allowed to do?
Login
  ↓
Authentication
  ↓
Session
  ↓
Authorization
  ↓
Allow / Deny

🛡️ Cookie Security
HttpOnly

Prevents JavaScript from directly reading the cookie.
document.cookie
      ↓
HttpOnly Cookie
      ↓
❌ Not accessible
Secure

Cookie is sent only over HTTPS.

HTTPS → Cookie ✅
HTTP  → Cookie ❌

SameSite

Controls cookie behavior in cross-site contexts.

Strict → Most restrictive
Lax    → Balanced
None   → Cross-site cookies allowed

⏳ Session Expiration

Sessions don't remain valid forever.

Session Created
      ↓
Timeout
      ↓
Session Expired
      ↓
Login Required

🚪 Logout & Session Invalidation
User clicks Logout
        ↓
Logout Request
        ↓
Server invalidates Session
        ↓
Cookie cleared / expired
        ↓
Protected page requested
        ↓
Session invalid ❌
        ↓
Login Required

Important:

Logout
=
Session Invalidation
+
Cookie Clearance / Expiration
🧪 Practical Commands
Check response headers
curl -I https://github.com
HTTP → HTTPS redirect
curl -I http://github.com

Example:

HTTP/1.1 301 Moved Permanently
Location: https://github.com/
Check 403 response
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
🎯 Day 9 Takeaway
Login
  ↓
Authentication
  ↓
Session Creation
  ↓
Session ID → Cookie
  ↓
Browser Stores Cookie
  ↓
Cookie sent with requests
  ↓
Server validates Session
  ↓
Access Granted
  ↓
Logout
  ↓
Session Invalidated
  ↓
Access Denied

Today I connected HTTP, Cookies, Sessions, Authentication, Authorization and Web Security into one complete flow.

#Day9 #CyberSecurity #WebSecurity #Networking #HTTP #Cookies #Sessions #Authentication
