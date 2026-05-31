# 12. SEO Fundamentals

## What is SEO?

Search Engine Optimization (SEO) is the practice of optimizing your website to rank higher in search engine results.

## HTML Elements for SEO

### Title Tag

```html
<title>Best Web Development Course - Learn HTML, CSS, JavaScript</title>
```

Best practices:
- 50-60 characters (displays fully in search results)
- Include primary keyword at the beginning
- Unique for each page
- Make it compelling to encourage clicks

### Meta Description

```html
<meta name="description" content="Learn web development from scratch with our comprehensive guide covering HTML5, CSS3, and responsive design. Perfect for beginners.">
```

Best practices:
- 150-160 characters
- Include primary keyword
- Write as a marketing message
- Unique for each page

### Heading Hierarchy

```html
<h1>Main Page Topic</h1>
<h2>Section Title</h2>
<h3>Subsection</h3>
```

Benefits:
- Tells search engines page structure
- Improves accessibility
- Only one `<h1>` per page

### URL Structure

```html
<!-- Good URL - descriptive and short -->
<a href="/web-development-guide">Guide</a>

<!-- Bad URL - unclear -->
<a href="/page?id=12345">Guide</a>
```

## Meta Tags for SEO

### Viewport (Mobile)

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Essential for mobile rankings.

### Charset

```html
<meta charset="UTF-8">
```

Ensures proper text rendering.

### Open Graph Tags (Social Sharing)

```html
<meta property="og:title" content="Page Title">
<meta property="og:description" content="Page description">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:url" content="https://example.com/page">
<meta property="og:type" content="website">
```

### Twitter Card Tags

```html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Page Title">
<meta name="twitter:description" content="Description">
<meta name="twitter:image" content="https://example.com/image.jpg">
```

### Robots Meta Tag

```html
<!-- Allow indexing and following links -->
<meta name="robots" content="index, follow">

<!-- Don't index this page -->
<meta name="robots" content="noindex, nofollow">

<!-- Don't display snippets -->
<meta name="robots" content="nosnippet">
```

## Structured Data (Schema.org)

Help search engines understand your content:

```html
<!-- Article markup -->
<article>
    <h1>Understanding Flexbox</h1>
    <time datetime="2026-05-31">May 31, 2026</time>
    <p>Flexbox is a powerful CSS layout system...</p>
</article>

<!-- With JSON-LD schema -->
<script type="application/ld+json">
{
    "@context": "https://schema.org",
    "@type": "Article",
    "headline": "Understanding Flexbox",
    "datePublished": "2026-05-31",
    "description": "Flexbox is a powerful CSS layout system..."
}
</script>
```

## Internal Linking Strategy

```html
<!-- Link to related content -->
<article>
    <h1>Getting Started with HTML</h1>
    <p>
        Now that you understand HTML, 
        <a href="/css-basics">learn CSS basics</a> 
        to style your pages.
    </p>
</article>
```

### Anchor Text

```html
<!-- Good: Descriptive anchor text -->
<a href="/guide">Learn web development</a>

<!-- Bad: Generic anchor text -->
<a href="/guide">Click here</a>
```

## Mobile Optimization

```html
<!-- Mobile viewport -->
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- Fast loading -->
<link rel="preconnect" href="https://fonts.googleapis.com">

<!-- Mobile-friendly design (CSS media queries) -->
<style>
    @media (max-width: 768px) {
        body { font-size: 16px; }
    }
</style>
```

## Site Structure

```html
<!-- Clear hierarchy -->
Homepage
├── /services
├── /about
├── /blog
│   ├── /blog/article-1
│   └── /blog/article-2
└── /contact
```

## Canonical Tags

```html
<!-- Avoid duplicate content issues -->
<link rel="canonical" href="https://example.com/page">
```

Use when:
- Multiple URLs point to same content
- Sorting/filtering creates duplicate pages
- Mobile and desktop versions

## SEO Checklist

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Charset and viewport (mobile) -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- Title and description -->
    <title>Main Keyword - Secondary Keywords | Brand Name</title>
    <meta name="description" content="Compelling description with keywords, under 160 characters">
    
    <!-- Open Graph for social sharing -->
    <meta property="og:title" content="Title">
    <meta property="og:description" content="Description">
    <meta property="og:image" content="image.jpg">
    <meta property="og:url" content="https://example.com/page">
    
    <!-- Canonical tag -->
    <link rel="canonical" href="https://example.com/page">
    
    <!-- Favicon -->
    <link rel="icon" href="favicon.ico">
</head>
<body>
    <!-- Semantic structure -->
    <header>
        <h1>Page Title - Main Topic</h1>
    </header>
    
    <main>
        <article>
            <h2>Section Title</h2>
            <p>Content with keywords...</p>
            <a href="/related-page">Related article title</a>
        </article>
    </main>
    
    <footer>
        <p>&copy; 2026 Company</p>
    </footer>
    
    <!-- Structured data -->
    <script type="application/ld+json">
    {
        "@context": "https://schema.org",
        "@type": "Article",
        "headline": "Page Title",
        "description": "Page description"
    }
    </script>
</body>
</html>
```

## Key Takeaways

✅ Use descriptive title and meta description

✅ Implement proper heading hierarchy

✅ Use semantic HTML elements

✅ Include alt text for images

✅ Use open graph tags for social sharing

✅ Implement structured data markup

✅ Ensure mobile responsiveness

✅ Create descriptive URLs

✅ Use internal links strategically

---

**Next: [Advanced HTML →](13-advanced-html.md)**
