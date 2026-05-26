# Web Browsers & Developer Tools

## Task Description
This task introduces you to browser developer tools used for inspecting webpages, debugging JavaScript, analyzing network traffic, and viewing browser storage.  
You will learn how to use DevTools panels such as Elements, Console, Network, Sources, and Application to understand how websites work internally.

---

# 1. Install & Open Developer Tools
Modern browsers include built‑in DevTools.

### How to Open DevTools
- Chrome / Edge → Ctrl + Shift + I or F12
- Firefox → Ctrl + Shift + I
- Right‑click → Inspect

DevTools allow you to inspect DOM, debug JS, monitor network activity, and view storage.

---

# 2. Inspect Elements (DOM & CSS)
The Elements panel displays the live DOM and applied CSS.

### What You Can Do
- Inspect HTML structure
- Edit HTML nodes
- Modify CSS rules live
- Add/remove classes
- Test responsive layouts

### Example (CSS change)
    color: red;
    background: black;

---

# 3. Console (Logs, JS Execution, Errors)
The Console is a JavaScript environment inside the browser.

### Uses
- View console.log() output
- See warnings & errors
- Run JavaScript manually
- Test DOM manipulation

### Example
    document.body.style.background = "yellow";
    console.log("Hello from DevTools");

---

# 4. Network Tab (Requests, Headers, Payloads)
The Network panel shows all HTTP/HTTPS requests made by the page.

### What You Can Inspect
- Request URLs
- Status codes (200, 404, 500)
- Request & response headers
- Cookies sent with requests
- API responses (JSON, HTML, images)
- Load time & performance

### Example
    Request: GET /api/user
    Response: 200 OK
    Payload: { "id": 1, "name": "Anjaly" }

---

# 5. Sources / Debugger (Breakpoints & JS Execution)
The Sources or Debugger tab lets you pause and inspect JavaScript.

### Features
- Set breakpoints
- Step through code line-by-line
- Watch variable values
- View call stack
- Debug async code

### Example Workflow
1. Open a JS file
2. Click line number → add breakpoint
3. Reload page
4. Execution pauses → inspect variables

---

# 6. Application Tab (Storage & Service Workers)
The Application panel shows browser-side storage and background processes.

### Storage Types
- Cookies → small key-value data sent with requests
- localStorage → persistent storage
- sessionStorage → cleared when tab closes
- IndexedDB → large structured storage

### Service Workers
- Background scripts
- Enable offline caching
- Used in Progressive Web Apps (PWAs)

