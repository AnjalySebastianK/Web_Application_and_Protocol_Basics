# Cookies, Sessions, and Web Storage — Essential Notes

##  Task Description
This task explains how browsers store data using **cookies**, **localStorage**, **sessionStorage**, and how applications manage **sessions** or **JWT tokens**.  
These concepts are critical for authentication, security, and SOC analysis.

---

# 1. Cookie Attributes — Secure, HttpOnly, SameSite

Cookies are small key‑value pairs stored in the browser and sent with HTTP requests.

### Secure
- Cookie is sent **only over HTTPS**
- Prevents attackers from stealing cookies on insecure HTTP
- Recommended for all authentication cookies

### HttpOnly
- JavaScript **cannot access** the cookie
- Protects against XSS attacks stealing session tokens
- Should always be used for session/auth cookies

### SameSite
Controls whether cookies are sent on cross‑site requests.

Values:
- **Strict** → cookie sent only from same site  
- **Lax** → cookie sent for top‑level navigation (default)  
- **None** → cookie sent cross‑site (must use Secure)

### Security Implications
- Prevents CSRF (SameSite)
- Prevents XSS cookie theft (HttpOnly)
- Prevents MITM cookie theft (Secure)

---

# 2. Cookies vs localStorage vs sessionStorage

### Cookies
- Sent automatically with every HTTP request
- Small size (~4 KB)
- Can be Secure, HttpOnly, SameSite
- Used for authentication (session IDs)

### localStorage
- Persistent storage (survives browser restart)
- Not sent with requests
- Accessible via JavaScript
- Vulnerable to XSS attacks

### sessionStorage
- Cleared when tab closes
- Not shared across tabs
- Not sent with requests
- Also vulnerable to XSS

### Summary Table
    Cookies → best for authentication (with HttpOnly + Secure)
    localStorage → good for non‑sensitive preferences
    sessionStorage → temporary per‑tab data

---

# 3. When to Use Server‑Side Sessions vs JWT

### Server‑Side Sessions
The server stores session data; browser stores only a session ID cookie.

### When to Use
- Traditional web apps
- Sensitive authentication
- Need server‑side control (logout, revoke sessions)
- Want strong protection against token theft

### Pros
- HttpOnly cookies protect tokens
- Server can invalidate sessions anytime
- More secure for high‑risk apps

### Cons
- Requires server memory or database
- Harder to scale horizontally

---

### JWT (JSON Web Tokens)
Token contains user data and is stored client‑side (often in localStorage or cookies).

### When to Use
- Mobile apps
- Microservices
- Stateless APIs
- Large distributed systems

### Pros
- No server storage needed
- Easy scaling
- Works across multiple services

### Cons
- Cannot be revoked easily
- Storing JWT in localStorage is risky (XSS)
- Larger attack surface if token is stolen

---

#  Best Practice Summary
    Use HttpOnly + Secure cookies for authentication.
    Avoid storing JWTs in localStorage.
    Use server‑side sessions for sensitive apps.
    Use JWTs only when stateless architecture is required.
