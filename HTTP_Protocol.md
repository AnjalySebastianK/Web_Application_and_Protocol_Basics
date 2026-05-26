# HTTP Protocol — Detailed Fundamentals

##  Task Description
This task explains the core components of the **HTTP protocol**, including HTTP methods, status codes, and headers.  
Understanding these concepts is essential for web development, APIs, debugging, and cybersecurity.

---

# 1. HTTP Methods — Purpose & Use‑Cases

HTTP methods define the **action** a client wants to perform on a resource.

### GET
- Retrieves data from the server  
- No body  
- Safe & idempotent  
- Use‑case: fetch pages, images, API data

### POST
- Sends data to the server  
- Used to create resources  
- Not idempotent  
- Use‑case: login forms, file uploads, creating records

### PUT
- Replaces an existing resource  
- Idempotent  
- Use‑case: update user profile, replace product data

### DELETE
- Removes a resource  
- Idempotent  
- Use‑case: delete user, remove item from database

### PATCH
- Partially updates a resource  
- More efficient than PUT  
- Use‑case: update only one field (e.g., email)

### OPTIONS
- Returns allowed methods for a resource  
- Used in CORS preflight requests  
- Use‑case: browser checks server permissions

---

# 2. HTTP Response Status Codes — Categories & Examples

Status codes indicate the result of a request.

---

## 1xx — Informational
- 100 Continue → server received request headers  
- 101 Switching Protocols → upgrading connection (e.g., WebSockets)

---

## 2xx — Success
- 200 OK → request succeeded  
- 201 Created → new resource created  
- 204 No Content → success but no response body

---

## 3xx — Redirection
- 301 Moved Permanently → resource moved  
- 302 Found → temporary redirect  
- 304 Not Modified → use cached version

---

## 4xx — Client Errors
- 400 Bad Request → invalid request  
- 401 Unauthorized → authentication required  
- 403 Forbidden → no permission  
- 404 Not Found → resource missing  
- 429 Too Many Requests → rate limit exceeded

---

## 5xx — Server Errors
- 500 Internal Server Error → server crashed  
- 502 Bad Gateway → invalid response from upstream  
- 503 Service Unavailable → server overloaded or down  
- 504 Gateway Timeout → upstream server took too long

---

# 3. HTTP Headers — Request & Response

Headers provide **metadata** about the request or response.

---

##  Common Request Headers

### Host
    Host: example.com
Specifies the domain being requested.

### User-Agent
    User-Agent: Chrome/120
Identifies the browser or client.

### Accept
    Accept: application/json
Tells server what formats the client can handle.

### Authorization
    Authorization: Bearer <token>
Used for authentication.

### Content-Type
    Content-Type: application/json
Describes the format of the request body.

---

##  Common Response Headers

### Content-Type
    Content-Type: text/html
Tells the browser how to interpret the response.

### Set-Cookie
    Set-Cookie: sessionId=abc123; HttpOnly; Secure
Sends cookies to the browser.

### Cache-Control
    Cache-Control: no-cache
Controls caching behavior.

### Server
    Server: nginx
Identifies the web server software.

### Access-Control-Allow-Origin
    Access-Control-Allow-Origin: *
Used in CORS to allow cross‑origin requests.

