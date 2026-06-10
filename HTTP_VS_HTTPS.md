# HTTP vs HTTPS — Security Fundamentals

## Task Description
This task explains the difference between **HTTP** and **HTTPS**, focusing on how **TLS/SSL encryption**, **certificates**, and **HSTS** improve security.  
You will learn how secure communication works and why HTTPS is mandatory for modern web applications.

---

# 1. How TLS/SSL Works (High‑Level Overview)

TLS/SSL provides **encryption**, **authentication**, and **integrity** for HTTPS connections.

---

##  Certificates & Public Key Cryptography
A website uses a **digital certificate** issued by a trusted Certificate Authority (CA).

### What the certificate contains
- Website’s public key  
- Domain name  
- Issuer (CA)  
- Expiry date  
- Signature from CA  

### Purpose
- Proves the server is legitimate  
- Enables encrypted communication  

---

##  Chain of Trust
Browsers trust a website because of a **hierarchy of certificates**:

    Root CA → Intermediate CA → Website Certificate

### How it works
1. Browser trusts Root CAs (pre‑installed in OS/browser)
2. Root CA signs Intermediate CA
3. Intermediate CA signs website certificate
4. Browser verifies the chain → connection is trusted

If any certificate in the chain is invalid → browser shows a warning.

---

##  TLS Handshake (Simplified)
1. Browser says: “I want to connect securely”
2. Server sends certificate
3. Browser verifies certificate chain
4. Browser and server generate encryption keys
5. Secure encrypted connection begins

No passwords or sensitive data are exposed during handshake.

---

# 2. Benefits of HTTPS Over HTTP

HTTPS = HTTP + TLS encryption  
HTTP = plain text (no security)

---

##  Confidentiality
Data is encrypted → attackers cannot read it.

### Example
Login credentials, cookies, and API data are protected from:
- Wi‑Fi sniffing  
- MITM attacks  
- Packet inspection  

---

##  Integrity
Data cannot be modified in transit.

Prevents:
- Injection attacks  
- Tampering  
- Content manipulation  

---

##  Authenticity
Browser verifies the server’s identity using certificates.

Prevents:
- Fake websites  
- Phishing domains pretending to be real  
- MITM impersonation  

---

# 3. HSTS (HTTP Strict Transport Security)

HSTS forces browsers to use **HTTPS only**, never HTTP.

---

##  What HSTS Does
- Prevents protocol downgrade attacks  
- Prevents users from accidentally visiting HTTP versions  
- Protects first‑time connections after initial visit  

### Example Header
    Strict-Transport-Security: max-age=31536000; includeSubDomains; preload

---

##  Why HSTS Improves Security
- Attackers cannot force browser to switch to HTTP  
- Cookies cannot leak over insecure connections  
- Eliminates SSL‑strip attacks  

---

##  HSTS Preload List
Browsers maintain a built‑in list of domains that **must** use HTTPS.  
Once added, even the first visit is protected.

---

#  Summary
    HTTP → no encryption, vulnerable to attacks
    HTTPS → encrypted, authenticated, integrity‑protected
    TLS/SSL → enables secure communication using certificates
    HSTS → forces HTTPS and prevents downgrade attacks
