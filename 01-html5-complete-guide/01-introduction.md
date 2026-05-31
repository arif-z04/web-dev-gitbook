# Chapter 1: Introduction to HTML

## What is HTML?

HTML stands for **HyperText Markup Language**. It is the standard markup language used to create web pages and web applications. Unlike programming languages that use logic and algorithms, HTML is a *markup language* that uses tags to describe the structure and content of documents.

### Key Concept

> HTML tells the browser **what content is**, CSS tells it **how to style it**, and JavaScript adds **behavior and interactivity**.

## A Brief History

- **1989**: Tim Berners-Lee invented HTML at CERN
- **1993**: HTML 2.0 - First standard HTML specification
- **1997**: HTML 4.01 - Major improvements and standardization
- **2000**: XHTML - XML-based reformulation of HTML
- **2014**: HTML5 - Current standard with modern features
- **2022+**: Living Standard - Continuous updates and improvements

### Why HTML5?

HTML5 introduced:
- Semantic elements (`<article>`, `<section>`, `<nav>`, etc.)
- Native multimedia support (`<audio>`, `<video>`)
- Canvas for graphics
- Improved accessibility features
- Better form controls
- APIs for offline storage, geolocation, and more

## HTML vs CSS vs JavaScript

Understanding the distinction between these three technologies is crucial:

| Aspect | HTML | CSS | JavaScript |
|--------|------|-----|------------|
| **Purpose** | Structure & Content | Styling & Layout | Behavior & Interactivity |
| **Type** | Markup Language | Styling Language | Programming Language |
| **What It Does** | Defines elements | Styles elements | Controls elements |
| **Example** | `<button>Click Me</button>` | `button { color: blue; }` | `button.onclick = ...` |

### Real-World Analogy

Think of a website like a house:
- **HTML** = The structure and rooms (walls, doors, windows)
- **CSS** = The decoration and furniture (paint, carpets, layout)
- **JavaScript** = The utilities (electricity, plumbing, automation)

## How Browsers Render HTML

### The Rendering Pipeline

```
┌─────────────────────────────────────────────────────┐
│ 1. HTML Parsing                                     │
│    - Browser reads HTML code                        │
│    - Creates DOM tree                               │
└─────────────────┬───────────────────────────────────┘
                  │
┌─────────────────▼───────────────────────────────────┐
│ 2. CSS Parsing & Styling                            │
│    - Browser reads CSS rules                        │
│    - Creates CSSOM (CSS Object Model)               │
│    - Applies styles to DOM nodes                    │
└─────────────────┬───────────────────────────────────┘
                  │
┌─────────────────▼───────────────────────────────────┐
│ 3. Layout (Reflow)                                  │
│    - Browser calculates size and position          │
│    - Creates layout tree                            │
└─────────────────┬───────────────────────────────────┘
                  │
┌─────────────────▼───────────────────────────────────┐
│ 4. Painting (Rasterization)                         │
│    - Browser converts layout to pixels             │
│    - Creates paint records                          │
└─────────────────┬───────────────────────────────────┘
                  │
┌─────────────────▼───────────────────────────────────┐
│ 5. Compositing & Display                            │
│    - Browser composites layers                      │
│    - Displays final result on screen               │
└─────────────────────────────────────────────────────┘
```

### Understanding the DOM

The **DOM** (Document Object Model) is the browser's internal representation of your HTML:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Page</title>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>Welcome to HTML5</p>
  </body>
</html>
```

This creates a tree structure:

```
Document
└── html
    ├── head
    │   └── title
    │       └── "My Page"
    └── body
        ├── h1
        │   └── "Hello World"
        └── p
            └── "Welcome to HTML5"
```

## Website Architecture

### Typical Website Structure

```
Website
├── Frontend (Client-side)
│   ├── HTML (Structure)
│   ├── CSS (Styling)
│   └── JavaScript (Behavior)
└── Backend (Server-side)
    ├── Server
    ├── Database
    └── APIs
```

### Three-Layer Model

1. **Presentation Layer**: HTML, CSS, JavaScript (what users see)
2. **Business Logic Layer**: Server-side code (processes requests)
3. **Data Layer**: Databases (stores information)

## HTML Today

Modern HTML is part of a larger ecosystem:

- **HTML5** - Structure and content
- **CSS3** - Styling and animations
- **JavaScript (ES6+)** - Interactivity and logic
- **APIs** - Geolocation, Storage, Canvas, WebGL, etc.
- **Frameworks** - React, Vue, Angular (built on HTML)

## Your First HTML Document

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Web Page</title>
</head>
<body>
    <h1>Welcome to HTML5!</h1>
    <p>This is my first web page.</p>
</body>
</html>
```

### Why This Structure?

- `<!DOCTYPE html>` - Tells browser this is HTML5
- `<html lang="en">` - Root element with language attribute
- `<meta charset="UTF-8">` - Character encoding (essential for all languages)
- `<meta name="viewport">` - Makes page responsive
- `<title>` - Browser tab title and SEO
- `<body>` - All visible content

## Key Takeaways

✅ HTML is a markup language that structures web content

✅ HTML works with CSS for styling and JavaScript for interactivity

✅ Browsers parse HTML into a DOM tree for rendering

✅ Understanding how browsers render helps write efficient HTML

✅ HTML5 provides semantic and modern web features

---

**Next: [Chapter 2: HTML Document Structure →](02-document-structure.md)**

**Previous**: [Back to HTML5 Guide](README.md)
