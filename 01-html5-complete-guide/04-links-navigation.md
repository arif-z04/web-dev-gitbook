# 4. Links and Navigation

## The Anchor Tag - Creating Links

The `<a>` (anchor) tag creates hyperlinks - the foundation of the web.

```html
<a href="https://example.com">Click here</a>
```

## Link Attributes

### href (Required)

Specifies where the link goes:

```html
<!-- External link -->
<a href="https://example.com">Visit Example</a>

<!-- Relative link -->
<a href="pages/about.html">About Us</a>

<!-- Email link -->
<a href="mailto:contact@example.com">Email us</a>

<!-- Phone link -->
<a href="tel:+1234567890">Call us</a>

<!-- Internal page link -->
<a href="#section2">Jump to Section 2</a>
```

### title

Provides additional information (shows as tooltip):

```html
<a href="https://example.com" title="Visit our main website">Our Website</a>
```

### target

Controls where the link opens:

```html
<!-- Default - same tab/window -->
<a href="https://example.com">Default</a>

<!-- New tab -->
<a href="https://example.com" target="_blank">Open in new tab</a>

<!-- Named window -->
<a href="https://example.com" target="mywindow">Open in named window</a>
```

⚠️ **Security note for target="_blank"**:

```html
<!-- Vulnerable -->
<a href="https://external-site.com" target="_blank">External Link</a>

<!-- Secure -->
<a href="https://external-site.com" target="_blank" rel="noopener noreferrer">External Link</a>
```

The `rel="noopener noreferrer"` prevents security vulnerabilities.

### rel

Defines the relationship between current and linked document:

```html
<!-- Next page in sequence -->
<a href="page2.html" rel="next">Next Page</a>

<!-- Previous page -->
<a href="page1.html" rel="prev">Previous Page</a>

<!-- External link -->
<a href="https://external.com" rel="external">External Site</a>

<!-- Don't pass referrer info -->
<a href="https://example.com" rel="noreferrer">No Referrer</a>

<!-- Search engine should not follow this link -->
<a href="https://example.com" rel="nofollow">No Follow</a>
```

## URL Paths

### Absolute URLs

Complete web address:

```html
<!-- Works from anywhere -->
<a href="https://example.com/pages/about.html">About</a>
```

### Relative URLs

Relative to current page location:

```html
<!-- Same folder -->
<a href="about.html">About</a>

<!-- Subfolder -->
<a href="pages/contact.html">Contact</a>

<!-- Parent folder -->
<a href="../index.html">Home</a>

<!-- Root folder -->
<a href="/index.html">Home</a>

<!-- Current page, different section -->
<a href="#section2">Section 2</a>
```

## Special Link Types

### Email Links

```html
<a href="mailto:contact@example.com">Send us an email</a>

<!-- With subject -->
<a href="mailto:contact@example.com?subject=Website Inquiry">Contact us</a>

<!-- With subject and body -->
<a href="mailto:contact@example.com?subject=Question&body=I have a question...">Email with template</a>

<!-- Multiple recipients -->
<a href="mailto:john@example.com,jane@example.com">Email multiple people</a>
```

### Phone Links

```html
<a href="tel:+1-800-555-0123">Call us: +1 (800) 555-0123</a>
<a href="tel:+1-800-555-0123">1-800-555-0123</a>
```

### SMS Links

```html
<a href="sms:+1234567890">Send SMS</a>
<a href="sms:+1234567890?body=Hello">Send SMS with text</a>
```

### WhatsApp Links

```html
<a href="https://wa.me/1234567890">Message on WhatsApp</a>
```

## Internal Page Navigation

### Using IDs for anchor links

```html
<!-- Link to anchor -->
<a href="#section2">Go to Section 2</a>

<!-- Target element -->
<h2 id="section2">Section 2</h2>

<!-- Link to another page's anchor -->
<a href="page.html#section3">View Section 3 on Another Page</a>
```

### Navigation Example

```html
<!-- Table of Contents -->
<nav>
    <ul>
        <li><a href="#intro">Introduction</a></li>
        <li><a href="#features">Features</a></li>
        <li><a href="#pricing">Pricing</a></li>
        <li><a href="#contact">Contact</a></li>
    </ul>
</nav>

<!-- Content sections -->
<h2 id="intro">Introduction</h2>
<p>Content...</p>

<h2 id="features">Features</h2>
<p>Content...</p>

<h2 id="pricing">Pricing</h2>
<p>Content...</p>

<h2 id="contact">Contact</h2>
<p>Content...</p>
```

## Navigation Structures

### Simple List Navigation

```html
<nav>
    <a href="/">Home</a>
    <a href="/about">About</a>
    <a href="/services">Services</a>
    <a href="/contact">Contact</a>
</nav>
```

### Unordered List Navigation

```html
<nav>
    <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about">About</a></li>
        <li><a href="/services">Services</a></li>
        <li><a href="/contact">Contact</a></li>
    </ul>
</nav>
```

### Navigation with Submenus

```html
<nav>
    <ul>
        <li>
            <a href="/products">Products</a>
            <ul>
                <li><a href="/products/electronics">Electronics</a></li>
                <li><a href="/products/books">Books</a></li>
                <li><a href="/products/clothing">Clothing</a></li>
            </ul>
        </li>
        <li><a href="/about">About</a></li>
        <li><a href="/contact">Contact</a></li>
    </ul>
</nav>
```

## Accessibility for Links

### Descriptive Link Text

❌ Bad:
```html
<p>To learn more, <a href="/about">click here</a></p>
```

✅ Good:
```html
<p><a href="/about">Learn more about our company</a></p>
```

### Current Page Indicator

```html
<nav>
    <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about" aria-current="page">About</a></li>
        <li><a href="/contact">Contact</a></li>
    </ul>
</nav>
```

### Skip to Main Content

```html
<a href="#main" class="skip-link">Skip to main content</a>

<header>
    <nav>Navigation...</nav>
</header>

<main id="main">
    Main content...
</main>
```

## Common Link Mistakes

❌ **Mistake 1: Missing href**
```html
<!-- Wrong -->
<a>Click me</a>

<!-- Right -->
<a href="/page">Click me</a>
```

❌ **Mistake 2: Using buttons for links**
```html
<!-- Wrong for navigation -->
<button onclick="location.href='/'">Home</button>

<!-- Right -->
<a href="/">Home</a>
```

❌ **Mistake 3: Vague link text**
```html
<!-- Wrong -->
<p><a href="/policy">Click here</a> for our privacy policy</p>

<!-- Right -->
<p><a href="/policy">Read our privacy policy</a></p>
```

❌ **Mistake 4: Opening external links unsafely**
```html
<!-- Unsafe -->
<a href="https://external.com" target="_blank">External</a>

<!-- Safe -->
<a href="https://external.com" target="_blank" rel="noopener noreferrer">External</a>
```

## Real-World Examples

### Website Header with Navigation

```html
<header>
    <h1>My Company</h1>
    <nav>
        <ul>
            <li><a href="/">Home</a></li>
            <li>
                <a href="/services">Services</a>
                <ul>
                    <li><a href="/services/web-design">Web Design</a></li>
                    <li><a href="/services/development">Development</a></li>
                </ul>
            </li>
            <li><a href="/about">About</a></li>
            <li><a href="/blog">Blog</a></li>
            <li><a href="/contact">Contact</a></li>
        </ul>
    </nav>
</header>
```

### Footer with Multiple Link Groups

```html
<footer>
    <section>
        <h3>Company</h3>
        <ul>
            <li><a href="/about">About Us</a></li>
            <li><a href="/careers">Careers</a></li>
            <li><a href="/press">Press</a></li>
        </ul>
    </section>
    
    <section>
        <h3>Support</h3>
        <ul>
            <li><a href="/help">Help Center</a></li>
            <li><a href="/contact">Contact Us</a></li>
            <li><a href="mailto:support@example.com">Email Support</a></li>
        </ul>
    </section>
    
    <section>
        <h3>Legal</h3>
        <ul>
            <li><a href="/privacy">Privacy Policy</a></li>
            <li><a href="/terms">Terms of Service</a></li>
        </ul>
    </section>
</footer>
```

### Breadcrumb Navigation

```html
<nav aria-label="breadcrumb">
    <ol>
        <li><a href="/">Home</a></li>
        <li><a href="/products">Products</a></li>
        <li><a href="/products/electronics">Electronics</a></li>
        <li aria-current="page">Laptops</li>
    </ol>
</nav>
```

## Best Practices

✅ Use descriptive link text

✅ Use relative links for internal navigation

✅ Always use `rel="noopener noreferrer"` with `target="_blank"`

✅ Use semantic `<nav>` element for navigation

✅ Use IDs for internal page anchors

✅ Make links keyboard accessible

✅ Ensure sufficient color contrast for links

✅ Indicate external links clearly

---

**Next: [Images →](05-images.md)**
