# 2. HTML Document Structure

## The Anatomy of an HTML Document

Every HTML page follows a consistent structure. Understanding this structure is fundamental to writing valid, accessible HTML.

## The Complete Document Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Page description">
    <title>Page Title</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Page content goes here -->
    <h1>Welcome</h1>
    <p>Content...</p>
    <script src="script.js"></script>
</body>
</html>
```

## Breaking Down Each Component

### 1. DOCTYPE Declaration

```html
<!DOCTYPE html>
```

**Purpose**: Tells the browser this is an HTML5 document.

**Why it matters**: 
- Without it, the browser enters "quirks mode" and renders inconsistently
- It's required for valid HTML
- It must be the very first line of the document

**Before HTML5** (don't use these):
```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" 
    "http://www.w3.org/TR/html4/strict.dtd">
```

The HTML5 DOCTYPE is much simpler!

### 2. The `<html>` Element

```html
<html lang="en">
    <!-- All content goes here -->
</html>
```

**Purpose**: Root element containing all other elements.

**The `lang` attribute**:
```html
<html lang="en">      <!-- English -->
<html lang="es">      <!-- Spanish -->
<html lang="fr">      <!-- French -->
<html lang="de">      <!-- German -->
<html lang="zh-CN">   <!-- Simplified Chinese -->
```

**Why it matters**:
- Helps screen readers pronounce words correctly
- Assists search engines
- Enables browser translation features
- Is required for accessibility compliance

### 3. The `<head>` Section

The head contains metadata about the page but isn't displayed in the browser window.

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Page description">
    <meta name="keywords" content="web, development, html">
    <meta name="author" content="Your Name">
    
    <title>Page Title</title>
    
    <link rel="stylesheet" href="styles.css">
    <link rel="icon" href="favicon.ico">
    
    <style>
        body { color: #333; }
    </style>
</head>
```

#### Essential Meta Tags

**Character Encoding**:
```html
<meta charset="UTF-8">
```
- Must be in the first 1024 bytes of the document
- Ensures text renders correctly
- Prevents encoding-related bugs

**Viewport Meta Tag**:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
- Essential for responsive design
- Tells browsers how to render on mobile devices
- Without it, mobile sites look zoomed out

**Description**:
```html
<meta name="description" content="A concise description of your page">
```
- Used by search engines in search results
- Keep it 155-160 characters
- Improves click-through rates

**Open Graph Tags** (for social media):
```html
<meta property="og:title" content="My Page Title">
<meta property="og:description" content="Description">
<meta property="og:image" content="image.jpg">
<meta property="og:url" content="https://example.com">
```

#### The `<title>` Element

```html
<title>My Website - About Web Development</title>
```

**Purpose**:
- Shown in browser tab
- Used by search engines as the page heading
- Used by screen readers to identify the page
- Important for bookmarks

**Best practices**:
- Keep it under 60 characters (displays fully in search results)
- Put keywords at the beginning
- Make each page title unique
- Be descriptive and concise

❌ Bad: `<title>Home</title>`
✅ Good: `<title>Web Development Guide - Learn HTML, CSS, JavaScript</title>`

#### Linking External Resources

**Stylesheets**:
```html
<link rel="stylesheet" href="styles.css">
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto">
```

**Favicon**:
```html
<link rel="icon" href="favicon.ico">
<link rel="apple-touch-icon" href="apple-touch-icon.png">
```

**Preconnect for Performance**:
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="dns-prefetch" href="https://cdn.example.com">
```

### 4. The `<body>` Element

```html
<body>
    <!-- All visible content goes here -->
</body>
```

**Purpose**: Contains all visible content - everything users see and interact with.

**Structure example**:
```html
<body>
    <header>...</header>
    <nav>...</nav>
    <main>...</main>
    <aside>...</aside>
    <footer>...</footer>
</body>
```

## Complete Modern Page Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Meta tags for character encoding and viewport -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- SEO Meta tags -->
    <meta name="description" content="Learn web development with our comprehensive guide">
    <meta name="keywords" content="HTML, CSS, JavaScript, web development">
    <meta name="author" content="Your Name">
    
    <!-- Open Graph tags for social sharing -->
    <meta property="og:title" content="Web Development Guide">
    <meta property="og:description" content="Learn web development">
    <meta property="og:image" content="https://example.com/image.jpg">
    <meta property="og:url" content="https://example.com">
    
    <!-- Page title -->
    <title>Web Development Guide | Learn Modern Web Development</title>
    
    <!-- Favicon -->
    <link rel="icon" href="favicon.ico">
    
    <!-- External stylesheets -->
    <link rel="stylesheet" href="styles.css">
    
    <!-- Preconnect to external domains -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    
    <!-- Inline styles (if needed) -->
    <style>
        /* Critical CSS */
    </style>
</head>
<body>
    <!-- Semantic structure -->
    <header>
        <h1>My Website</h1>
        <nav>Navigation links</nav>
    </header>
    
    <main>
        <article>
            <h2>Main content</h2>
            <p>Article content...</p>
        </article>
        
        <aside>
            Sidebar content
        </aside>
    </main>
    
    <footer>
        Footer information
    </footer>
    
    <!-- Scripts at the end of body -->
    <script src="script.js"></script>
</body>
</html>
```

## Document Structure Best Practices

### 1. Logical Hierarchy

```html
<h1>Main Page Title</h1>
<h2>Section Title</h2>
<h3>Subsection</h3>
<h4>Sub-subsection</h4>
```

- Use only ONE `<h1>` per page
- Don't skip heading levels
- Use headings for structure, not styling

### 2. Semantic Organization

```html
<header>Header content</header>
<nav>Navigation</nav>
<main>Main content</main>
<aside>Sidebar</aside>
<footer>Footer</footer>
```

### 3. Proper Meta Tag Order

1. DOCTYPE declaration
2. Opening `<html>` tag with lang
3. `<head>` opening tag
4. Charset meta tag
5. Viewport meta tag
6. Other meta tags
7. Title tag
8. Link tags
9. Style tags
10. Body and content

## Common Mistakes

❌ **Missing DOCTYPE**:
```html
<!-- Wrong -->
<html>
<head>...</head>
</html>
```

✅ **Always include DOCTYPE**:
```html
<!DOCTYPE html>
<html>
</html>
```

❌ **Missing viewport meta tag**:
```html
<!-- Wrong for modern web -->
<head>
    <title>My Page</title>
</head>
```

✅ **Always include viewport**:
```html
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Page</title>
</head>
```

❌ **Improper meta tag order**:
```html
<!-- Wrong -->
<title>My Page</title>
<meta charset="UTF-8">
```

✅ **Correct order**:
```html
<meta charset="UTF-8">
<title>My Page</title>
```

## Key Takeaways

1. **DOCTYPE is mandatory** - Always start with `<!DOCTYPE html>`
2. **Head metadata matters** - SEO, accessibility, and usability depend on proper head tags
3. **Charset first** - Always declare UTF-8 encoding early
4. **Viewport tag is essential** - Responsive design requires this meta tag
5. **One `<h1>` per page** - Use proper heading hierarchy
6. **Semantic structure** - Use meaningful elements

---

**Next: [Text Elements →](03-text-elements.md)**
