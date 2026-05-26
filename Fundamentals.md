# Fundamentals of the Web — Brief Technical Notes

## Task Description
This task introduces the core building blocks of how the web works: the World Wide Web, HTTP, URLs, websites, web servers, and web browsers.  
These concepts form the foundation for understanding networking, web development, and cybersecurity.

---

# 1. WWW — World Wide Web

### What It Is
The **World Wide Web (WWW)** is a system of interlinked documents and resources accessed over the **internet**.

### Key Points
- Uses HTTP/HTTPS to request and deliver content
- Contains HTML pages, images, videos, APIs, and files
- Runs **on top of** the internet (the internet is the infrastructure)

---

# 2. HTTP — Purpose & Request/Response Model

### Purpose
HTTP (HyperText Transfer Protocol) defines **how clients and servers communicate**.

### How It Works
- Browser sends an **HTTP request**
- Server returns an **HTTP response**

### Example Flow
    Client → GET /index.html
    Server → 200 OK + HTML content

### Characteristics
- Stateless  
- Text‑based  
- Foundation of all web communication  

---

# 3. URL — Structure & Components

A URL identifies the location of a resource on the web.

### Structure
    scheme://host:port/path?query#fragment

### Components
- **Scheme** → http, https  
- **Host** → domain or IP  
- **Port** → optional (80, 443)  
- **Path** → resource location  
- **Query** → key=value parameters  
- **Fragment** → page section  

Example:
    https://example.com/products?id=10#details

---

# 4. Website — Components & Hosting Basics

### What a Website Is
A collection of web pages served over the internet.

### Components
- **Frontend** → HTML, CSS, JavaScript  
- **Backend** → server logic, APIs, databases  
- **Assets** → images, fonts, videos  

### Hosting Basics
- Files stored on a **web server**
- Domain name maps to server IP
- Browser fetches files via HTTP/HTTPS

---

# 5. Web Server — Role & Examples

### Role
A web server:
- Accepts HTTP requests  
- Serves static files (HTML, CSS, JS, images)  
- Forwards dynamic requests to backend apps  

### Popular Web Servers
- Apache  
- Nginx  
- Microsoft IIS  

### Basic Behavior
    Client → Request → Server → Response → Browser renders page

---

# 6. Web Browser — Role, Rendering Engine, User Agent

### Role
A browser retrieves, interprets, and displays web content.

### Rendering Engine
Responsible for turning HTML/CSS/JS into a visual webpage.

Examples:
- Blink → Chrome, Edge  
- WebKit → Safari  
- Gecko → Firefox  

### What the Browser Does
- Parses HTML → builds DOM  
- Applies CSS → layout  
- Executes JavaScript → interactivity  

### User Agent
A string sent to servers identifying the browser and OS.

