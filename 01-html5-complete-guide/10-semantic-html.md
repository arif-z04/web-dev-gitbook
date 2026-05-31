# 10. Semantic HTML

## What is Semantic HTML?

Semantic HTML uses meaningful elements that describe their content and structure, not just their appearance.

### Non-Semantic Elements

```html
<!-- Less meaningful -->
<div class="header">
    <div class="nav">
        <div><a href="/">Home</a></div>
        <div><a href="/about">About</a></div>
    </div>
</div>
```

### Semantic Elements

```html
<!-- More meaningful -->
<header>
    <nav>
        <a href="/">Home</a>
        <a href="/about">About</a>
    </nav>
</header>
```

## Semantic Container Elements

### `<header>`

Introductory content for a page or section:

```html
<header>
    <h1>My Website</h1>
    <p>Welcome to my personal blog</p>
</header>
```

### `<nav>`

Navigation links:

```html
<nav>
    <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about">About</a></li>
        <li><a href="/contact">Contact</a></li>
    </ul>
</nav>
```

### `<main>`

Main content of the page:

```html
<main>
    <article>
        <h1>Article Title</h1>
        <p>Article content...</p>
    </article>
</main>
```

### `<section>`

Thematic grouping of content:

```html
<section>
    <h2>Services</h2>
    <p>We offer the following services:</p>
    <ul>
        <li>Web Design</li>
        <li>Web Development</li>
    </ul>
</section>
```

### `<article>`

Self-contained content:

```html
<article>
    <h2>How to Learn Web Development</h2>
    <p>Published by John Smith on May 31, 2026</p>
    <p>Web development requires learning HTML, CSS, and JavaScript...</p>
</article>
```

### `<aside>`

Sidebar or tangential content:

```html
<aside>
    <h3>Related Links</h3>
    <ul>
        <li><a href="/blog">Blog</a></li>
        <li><a href="/resources">Resources</a></li>
    </ul>
</aside>
```

### `<footer>`

Footer content:

```html
<footer>
    <p>&copy; 2026 My Company</p>
    <p><a href="/privacy">Privacy Policy</a> | <a href="/terms">Terms</a></p>
</footer>
```

## Semantic Content Elements

### `<article>`

```html
<article>
    <h2>Understanding Flexbox</h2>
    <p>Published on <time datetime="2026-05-31">May 31, 2026</time></p>
    <p>Flexbox is a powerful CSS layout system...</p>
</article>
```

### `<section>`

```html
<section id="pricing">
    <h2>Pricing Plans</h2>
    <article>
        <h3>Basic Plan</h3>
        <p>$9/month</p>
    </article>
    <article>
        <h3>Pro Plan</h3>
        <p>$29/month</p>
    </article>
</section>
```

### `<figure>` and `<figcaption>`

```html
<figure>
    <img src="chart.png" alt="Sales growth chart">
    <figcaption>Figure 1: Sales grew 45% YoY</figcaption>
</figure>
```

### `<mark>`

```html
<p>You can <mark>highlight important</mark> text.</p>
```

## Complete Semantic Page

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Semantic Web Design - Learn Modern HTML</title>
</head>
<body>
    <header>
        <h1>My Blog</h1>
        <p>Share knowledge about web development</p>
    </header>
    
    <nav>
        <ul>
            <li><a href="/">Home</a></li>
            <li><a href="/about">About</a></li>
            <li><a href="/blog">Blog</a></li>
            <li><a href="/contact">Contact</a></li>
        </ul>
    </nav>
    
    <main>
        <article>
            <h2>Understanding Semantic HTML</h2>
            <time datetime="2026-05-31">May 31, 2026</time>
            
            <section>
                <h3>What is Semantic HTML?</h3>
                <p>Semantic HTML describes meaning to both browser and developer...</p>
            </section>
            
            <section>
                <h3>Benefits of Semantic HTML</h3>
                <ul>
                    <li>Improved accessibility</li>
                    <li>Better SEO</li>
                    <li>Easier maintenance</li>
                </ul>
            </section>
            
            <figure>
                <img src="semantic-elements.png" alt="Diagram of semantic HTML elements">
                <figcaption>The semantic structure of a modern web page</figcaption>
            </figure>
        </article>
        
        <aside>
            <h3>Related Articles</h3>
            <ul>
                <li><a href="/html-best-practices">HTML Best Practices</a></li>
                <li><a href="/accessibility-guide">Accessibility Guide</a></li>
            </ul>
        </aside>
    </main>
    
    <footer>
        <p>&copy; 2026 My Blog. All rights reserved.</p>
        <nav>
            <a href="/privacy">Privacy Policy</a> |
            <a href="/terms">Terms of Service</a>
        </nav>
    </footer>
</body>
</html>
```

## Why Semantic HTML Matters

### 1. Accessibility
Screen readers understand page structure:
```html
<button>Click me</button>  <!-- Wrong for navigation -->
<a href="/">Home</a>       <!-- Right for navigation -->
```

### 2. SEO
Search engines understand content better:
```html
<main>
    <article>Main content ranked higher</article>
</main>
```

### 3. Maintainability
Developers understand code faster:
```html
<nav><!-- Navigation code --></nav>   <!-- Clear purpose -->
<div id="nav"><!-- Navigation --></div> <!-- Unclear purpose -->
```

### 4. Machine Readability
AI and bots understand your content:
```html
<article> understood by content analyzers
<time> understood by calendar/scheduling services
<address> understood by contact scrapers
```

## Key Takeaways

✅ Use meaningful semantic elements

✅ Structure content with `<header>`, `<main>`, `<footer>`

✅ Use `<article>` for self-contained content

✅ Use `<section>` for thematic groups

✅ Use `<nav>` for navigation

✅ Use `<aside>` for related sidebar content

✅ Semantic HTML improves accessibility and SEO

---

**Next: [Accessibility →](11-accessibility.md)**
