# Server‑Side Technologies & Web Servers — Fundamentals

## Task Description
This task introduces the basics of **server‑side programming**, how **web servers** like Apache and Nginx operate, and how a **browser request travels** through the server to the application.  
These concepts are essential for understanding backend development, APIs, and cybersecurity.

---

# 1. Introduction to Server‑Side Languages

Server‑side languages run on the **server**, not in the browser.  
They handle logic, databases, authentication, APIs, and dynamic content.

---

## Node.js (Primary Focus)
Node.js uses **JavaScript on the server**.

### Key Features
- Non‑blocking, event‑driven architecture  
- Fast for real‑time apps (chat, streaming)  
- Uses npm for packages  

### Example (Simple Server)
    const http = require("http");
    http.createServer((req, res) => {
        res.end("Hello from Node.js server");
    }).listen(3000);

---

## PHP (Brief Overview)
PHP is widely used for traditional web apps and CMS platforms (WordPress, Drupal).

### Example
    <?php
        echo "Hello from PHP";
    ?>

---

## Python (Brief Overview)
Python is used with frameworks like Flask and Django.

### Example (Flask)
    from flask import Flask
    app = Flask(__name__)

    @app.route("/")
    def home():
        return "Hello from Python Flask"

    app.run()

---

# 2. Overview of Web Servers: Apache vs Nginx

Web servers deliver content to clients and forward requests to backend applications.

---

## Apache HTTP Server
### Characteristics
- Process‑based architecture  
- Highly configurable with .htaccess  
- Great for shared hosting  
- Strong support for PHP  

### When to Use
- Traditional websites  
- Heavy use of .htaccess rules  
- PHP‑based applications  

---

## Nginx
### Characteristics
- Event‑driven, asynchronous  
- Extremely fast under high load  
- Acts as a reverse proxy, load balancer, or static file server  

### When to Use
- High‑traffic applications  
- API gateways  
- Reverse proxy setups  
- Serving static files efficiently  

---

## Apache vs Nginx Summary
    Apache → Flexible, module‑rich, great for PHP  
    Nginx → Fast, scalable, ideal for modern high‑traffic apps

---

# 3. Request Lifecycle: Browser → Web Server → Application

Understanding the request flow is essential for debugging, performance tuning, and security.

---

## Step‑by‑Step Lifecycle

### 1. Browser Sends Request
    User enters URL → Browser sends HTTP request

### 2. DNS Resolution
    Domain name → IP address lookup

### 3. Web Server Receives Request
    Apache or Nginx checks:
    - Routing rules
    - Static file availability
    - Reverse proxy configuration

### 4. Server Decides:
    - Serve static file directly (HTML, CSS, JS, images)
    - OR forward request to backend (Node.js, PHP, Python)

### 5. Application Processes Request
    - Runs logic
    - Queries database
    - Generates response (HTML or JSON)

### 6. Response Sent Back
    Application → Web server → Browser

### 7. Browser Renders Output
    HTML → DOM  
    CSS → Layout  
    JS → Interactivity  
