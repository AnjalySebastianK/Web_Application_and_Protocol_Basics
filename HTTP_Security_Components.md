# HTTP Security Components — Essential Notes

## Task Description
This task covers the security features built into the HTTP protocol.  
You will learn about **security headers**, **CORS**, and **authentication methods**, all of which are critical for securing modern web applications and preventing common attacks.

---

# 1. Security‑Focused HTTP Headers

Security headers help protect websites from attacks like XSS, clickjacking, and protocol downgrade attacks.

---

## Content-Security-Policy (CSP)
Controls which resources the browser is allowed to load.

### Purpose
- Prevents XSS by blocking unauthorized scripts
- Restricts images, fonts, frames, AJAX calls, etc.

### Example
    Content-Security-Policy: default-src 'self';

---

## X-Frame-Options
Prevents your site from being embedded in an iframe.

### Purpose
- Protects against clickjacking attacks

### Values
- DENY → no iframes allowed
- SAMEORIGIN → only same domain can embed

---

## X-XSS-Protection
Legacy header for older browsers.

### Purpose
- Enables built‑in XSS filters (mostly deprecated)

### Example
    X-XSS-Protection: 1; mode=block

---

## Strict-Transport-Security (HSTS)
Forces the browser to use HTTPS only.

### Purpose
- Prevents protocol downgrade attacks
- Protects against MITM on first request

### Example
    Strict-Transport-Security: max-age=31536000; includeSubDomains

---

# 2. HTTP Access Control & CORS Basics

CORS (Cross‑Origin Resource Sharing) controls which domains can access your server.

---

## What Causes CORS Errors
A browser blocks a request when:
- A frontend at **origin A** tries to access a backend at **origin B**
- The backend does NOT explicitly allow origin A

### Example Scenario
Frontend: http://localhost:3000  
Backend: http://localhost:5000  
→ Browser blocks request unless backend allows it.

---

## How to Fix CORS Errors
Server must send proper headers:

### Allow a specific origin
    Access-Control-Allow-Origin: http://localhost:3000

### Allow methods
    Access-Control-Allow-Methods: GET, POST, PUT, DELETE

### Allow headers
    Access-Control-Allow-Headers: Content-Type, Authorization

### Allow credentials (cookies)
    Access-Control-Allow-Credentials: true

---

# 3. HTTP Authentication Methods

Authentication ensures only authorized users can access protected resources.

---

## Basic Authentication
Credentials are sent as Base64 encoded string.

### Example
    Authorization: Basic dXNlcjpwYXNz

### Issues
- Not secure without HTTPS
- Credentials sent on every request

---

## Bearer Token Authentication
Client sends a token (usually JWT or API token).

### Example
    Authorization: Bearer eyJhbGciOi...

### Advantages
- More secure than Basic Auth
- Tokens can expire
- No need to send username/password repeatedly

---

## Best Practices
- Always use HTTPS  
- Never store tokens in localStorage (XSS risk)  
- Prefer HttpOnly cookies for sensitive tokens  
- Use short‑lived tokens + refresh tokens  
- Validate tokens on every request  

