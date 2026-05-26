# Hands‑On Browser DevTools Tasks

## Task Description
This task focuses on practicing real‑world debugging using browser DevTools.  
You will inspect CSS, trigger JavaScript errors, analyze network performance, and examine cookies.  
Each task includes space for writing results or adding screenshots.

---

# 1. Inspect & Edit Page CSS (Layout Change)

### Task
Use DevTools → Elements panel to:
- Select an element
- Modify its CSS (color, padding, layout, etc.)
- Observe changes live

### Example CSS You Might Edit
    display: flex;
    justify-content: center;
    background-color: #222;
    color: white;

---

# 2. Reproduce a JavaScript Error & Debug It

### Task
Open Console and intentionally trigger an error, for example:
    nonExistentFunction();

Then:
- Read the error message
- Click the file link to jump to the source
- Use breakpoints to inspect variables

### Expected Error Example
    Uncaught ReferenceError: nonExistentFunction is not defined
---

# 3. Capture Page Load & Identify Slow Requests

### Task
Open Network tab → Reload page → Sort by “Time”.

Identify:
- Slowest requests
- Their status codes
- Their file types

### Example Observation Format
    Slow Request 1: /api/data  → 1.8s
    Slow Request 2: /images/banner.png → 1.2s
    Slow Request 3: /fonts/main.woff2 → 900ms

### Top 3 Causes of Slow Loading
1. Large image files  
2. Slow backend API response  
3. Uncached static assets  

---

# 4. Show Cookies & Explain Cookie Attributes

### Task
Open Application tab → Cookies → Select domain.

List cookies and describe their attributes.

### Cookie Attributes Explained
- **SameSite**  
    Controls cross‑site cookie sending.  
    Values: Lax, Strict, None.

- **Secure**  
    Cookie is sent only over HTTPS.

- **HttpOnly**  
    JavaScript cannot access this cookie (prevents XSS theft).

- **Expires / Max‑Age**  
    Defines cookie lifetime.

- **Domain / Path**  
    Controls where the cookie is valid.


