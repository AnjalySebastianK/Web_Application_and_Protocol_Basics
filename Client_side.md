#  Client‑Side Technologies — Fundamentals

## Task Description
This task introduces the three core client‑side technologies of the web: **HTML**, **CSS**, and **JavaScript**.  
You will learn their basic concepts, how they work together, and why they are essential for building interactive web pages.

---

# 1. HTML — Structure, Tags, Semantic Elements

### What HTML Is
HTML (HyperText Markup Language) defines the **structure** of a webpage.  
It uses **tags** to describe content such as headings, paragraphs, images, and links.

### Basic Structure
    <html>
        <head>
            <title>Page Title</title>
        </head>
        <body>
            <h1>Hello World</h1>
            <p>This is a paragraph.</p>
        </body>
    </html>

### Common Tags
- <h1> to <h6> → headings  
- <p> → paragraph  
- <a> → link  
- <img> → image  
- <ul>, <ol>, <li> → lists  
- <div>, <span> → generic containers  

### Semantic Elements
Semantic tags describe meaning, not just layout:
- <header>  
- <nav>  
- <section>  
- <article>  
- <footer>  

These improve accessibility and SEO.

---

# 2. CSS — Selectors, Box Model, Positioning, Responsive Basics

### What CSS Is
CSS (Cascading Style Sheets) controls the **appearance** of a webpage: colors, layout, spacing, fonts, and responsiveness.

### Selectors
    h1 { color: blue; }
    .btn { padding: 10px; }
    #main { background: lightgray; }

### Box Model
Every element is a box made of:
- Content  
- Padding  
- Border  
- Margin  

### Positioning
    position: static;
    position: relative;
    position: absolute;
    position: fixed;
    position: sticky;

Used to control how elements appear on the page.

### Responsive Basics
    @media (max-width: 600px) {
        body {
            background: lightblue;
        }
    }

Responsive design ensures pages work on mobile, tablet, and desktop.

---

# 3. JavaScript — Data Types, Functions, DOM, Events

### What JavaScript Is
JavaScript adds **interactivity** and **logic** to webpages.  
It can modify HTML, respond to user actions, and communicate with servers.

### Data Types
- String  
- Number  
- Boolean  
- Array  
- Object  
- Null  
- Undefined  

### Functions
    function greet() {
        console.log("Hello!");
    }

### DOM Manipulation
    document.getElementById("title").innerText = "Updated Title";

JavaScript can change text, styles, attributes, and structure of the page.

### Events
    button.addEventListener("click", function() {
        alert("Button clicked!");
    });

Events respond to user actions like clicks, typing, scrolling, and form submissions.
