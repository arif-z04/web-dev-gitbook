# Responsive Web Design Guide

## Understanding Responsive Design

Responsive Web Design (RWD) creates websites that adapt beautifully to any screen size.

### Mobile First Approach

Build for mobile first, then enhance for larger screens:

```css
/* Mobile styles (default) */
.container {
    width: 100%;
    padding: 10px;
}

/* Tablet and up */
@media (min-width: 768px) {
    .container {
        width: 750px;
        padding: 20px;
    }
}

/* Desktop and up */
@media (min-width: 1024px) {
    .container {
        width: 970px;
    }
}
```

## Viewport Meta Tag

Essential for responsive design:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Without this, mobile browsers display the desktop version zoomed out.

## Flexible Layouts

### Percentage-Based Widths

```css
.container {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
}

.column {
    width: 33.333%;
    float: left;
    padding: 10px;
    box-sizing: border-box;
}
```

### Flexbox for Responsive Layouts

```css
.container {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
}

.item {
    flex: 1;
    min-width: 250px;
}
```

### CSS Grid for Responsive Layouts

```css
.grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
}
```

## Responsive Images

### Max-width Technique

```css
img {
    max-width: 100%;
    height: auto;
}
```

### Picture Element (HTML)

```html
<picture>
    <source media="(max-width: 600px)" srcset="mobile.jpg">
    <source media="(max-width: 1200px)" srcset="tablet.jpg">
    <img src="desktop.jpg" alt="Image">
</picture>
```

## Media Queries

### Breakpoints

```css
/* Mobile: 320px - 767px */
@media (max-width: 767px) {
    .sidebar { display: none; }
}

/* Tablet: 768px - 1023px */
@media (min-width: 768px) and (max-width: 1023px) {
    .sidebar { width: 250px; }
}

/* Desktop: 1024px and up */
@media (min-width: 1024px) {
    .sidebar { width: 300px; }
}

/* Large screens: 1920px and up */
@media (min-width: 1920px) {
    .sidebar { width: 400px; }
}
```

### Media Features

```css
/* Orientation */
@media (orientation: landscape) { }
@media (orientation: portrait) { }

/* Hover capability */
@media (hover: hover) {
    a:hover { color: blue; }
}

/* Reduced motion (accessibility) */
@media (prefers-reduced-motion: reduce) {
    * { animation: none; transition: none; }
}

/* Dark mode preference */
@media (prefers-color-scheme: dark) {
    body { background: #1a1a1a; color: #fff; }
}
```

## Responsive Typography

### Fluid Typography

```css
/* Responsive font size */
body {
    font-size: clamp(16px, 2vw, 32px);
}

h1 {
    font-size: clamp(24px, 5vw, 48px);
}
```

### Media Query Typography

```css
body { font-size: 14px; }

@media (min-width: 768px) {
    body { font-size: 16px; }
}

@media (min-width: 1024px) {
    body { font-size: 18px; }
}
```

## Responsive Navigation

### Mobile-First Navigation

```html
<nav class="navbar">
    <button class="menu-toggle">☰ Menu</button>
    <ul class="nav-menu" id="navMenu">
        <li><a href="/">Home</a></li>
        <li><a href="/about">About</a></li>
        <li><a href="/services">Services</a></li>
        <li><a href="/contact">Contact</a></li>
    </ul>
</nav>
```

```css
/* Mobile: Hamburger menu */
.nav-menu {
    display: none;
    flex-direction: column;
    position: absolute;
    background: white;
    width: 100%;
    top: 60px;
}

.nav-menu.active {
    display: flex;
}

.menu-toggle {
    display: block;
    background: none;
    border: none;
    font-size: 24px;
    cursor: pointer;
}

/* Desktop: Horizontal menu */
@media (min-width: 768px) {
    .nav-menu {
        display: flex !important;
        flex-direction: row;
        position: static;
        width: auto;
    }
    
    .menu-toggle {
        display: none;
    }
}
```

## Complete Responsive Page

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Website</title>
    <style>
        * { box-sizing: border-box; }
        
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            font-size: 16px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background: #333;
            color: white;
            padding: 20px 0;
        }
        
        header h1 {
            margin: 0;
        }
        
        /* Navigation */
        nav ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: none;
        }
        
        nav li {
            margin: 10px 0;
        }
        
        nav a {
            color: white;
            text-decoration: none;
        }
        
        @media (min-width: 768px) {
            nav ul {
                display: flex;
                gap: 20px;
            }
            
            nav li {
                margin: 0;
            }
        }
        
        /* Main content */
        main {
            display: grid;
            grid-template-columns: 1fr;
            gap: 20px;
            padding: 20px 0;
        }
        
        @media (min-width: 768px) {
            main {
                grid-template-columns: 2fr 1fr;
            }
        }
        
        /* Cards */
        .card {
            background: #f5f5f5;
            padding: 20px;
            border-radius: 4px;
        }
        
        /* Footer */
        footer {
            background: #333;
            color: white;
            padding: 20px 0;
            margin-top: 40px;
        }
        
        /* Images */
        img {
            max-width: 100%;
            height: auto;
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>My Website</h1>
        </div>
    </header>
    
    <nav class="container">
        <ul>
            <li><a href="/">Home</a></li>
            <li><a href="/about">About</a></li>
            <li><a href="/services">Services</a></li>
            <li><a href="/contact">Contact</a></li>
        </ul>
    </nav>
    
    <main class="container">
        <article class="card">
            <h2>Welcome</h2>
            <p>This is a responsive website that adapts to all screen sizes.</p>
            <img src="hero.jpg" alt="Hero image">
        </article>
        
        <aside class="card">
            <h3>Sidebar</h3>
            <p>This sidebar only appears on larger screens.</p>
        </aside>
    </main>
    
    <footer>
        <div class="container">
            <p>&copy; 2026 My Website</p>
        </div>
    </footer>
</body>
</html>
```

## Key Takeaways

✅ Mobile-first approach

✅ Use viewport meta tag

✅ Flexible layouts with percentage or flexbox/grid

✅ Responsive images with max-width

✅ Media queries for different screen sizes

✅ Test on multiple devices

✅ Use relative units (rem, em, %)

---

**Next: [Golden Rules →](../04-golden-rules/README.md)**
