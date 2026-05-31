# 6. Lists

## Three Types of Lists

HTML provides three ways to organize list content, each with its own semantic meaning.

## Unordered Lists (`<ul>`)

Used for lists where order doesn't matter:

```html
<ul>
    <li>Apples</li>
    <li>Bananas</li>
    <li>Oranges</li>
</ul>
```

**Default Display**: Bullet points

### Unordered List Examples

```html
<!-- Features list -->
<h2>Product Features</h2>
<ul>
    <li>Easy to use</li>
    <li>Affordable pricing</li>
    <li>24/7 support</li>
    <li>Cloud storage</li>
</ul>

<!-- Navigation menu -->
<nav>
    <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about">About</a></li>
        <li><a href="/services">Services</a></li>
    </ul>
</nav>
```

## Ordered Lists (`<ol>`)

Used for lists where order matters:

```html
<ol>
    <li>Wake up</li>
    <li>Shower</li>
    <li>Breakfast</li>
    <li>Work</li>
</ol>
```

**Default Display**: Numbered (1, 2, 3...)

### List Type Attribute

Change the numbering style:

```html
<!-- Default numbers -->
<ol>
    <li>First</li>
    <li>Second</li>
</ol>

<!-- Lowercase letters -->
<ol type="a">
    <li>First</li>
    <li>Second</li>
</ol>

<!-- Uppercase letters -->
<ol type="A">
    <li>First</li>
    <li>Second</li>
</ol>

<!-- Lowercase Roman numerals -->
<ol type="i">
    <li>First</li>
    <li>Second</li>
</ol>

<!-- Uppercase Roman numerals -->
<ol type="I">
    <li>First</li>
    <li>Second</li>
</ol>
```

### Start Attribute

Start numbering from a different number:

```html
<ol start="10">
    <li>Tenth item</li>
    <li>Eleventh item</li>
    <li>Twelfth item</li>
</ol>
```

### Reversed Attribute

Reverse the order:

```html
<ol reversed>
    <li>Third</li>
    <li>Second</li>
    <li>First</li>
</ol>
```

## Description Lists (`<dl>`)

Used for term-definition pairs:

```html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language - the structure of web pages</dd>
    
    <dt>CSS</dt>
    <dd>Cascading Style Sheets - the styling of web pages</dd>
    
    <dt>JavaScript</dt>
    <dd>A programming language that adds interactivity to web pages</dd>
</dl>
```

**Components**:
- `<dt>` - Definition Term
- `<dd>` - Definition Description

### Description List Example

```html
<h2>Web Development Glossary</h2>
<dl>
    <dt>DOM</dt>
    <dd>Document Object Model - the browser's representation of an HTML page</dd>
    
    <dt>API</dt>
    <dd>Application Programming Interface - a way for applications to communicate</dd>
    
    <dt>SEO</dt>
    <dd>Search Engine Optimization - techniques to improve search rankings</dd>
</dl>
```

## Nested Lists

Lists can contain other lists:

```html
<ul>
    <li>Fruits
        <ul>
            <li>Apples</li>
            <li>Bananas</li>
        </ul>
    </li>
    <li>Vegetables
        <ul>
            <li>Carrots</li>
            <li>Broccoli</li>
        </ul>
    </li>
</ul>
```

### Complex Nested Lists

```html
<ol>
    <li>Installation
        <ol type="a">
            <li>Download the software</li>
            <li>Run the installer</li>
            <li>Follow the setup wizard</li>
        </ol>
    </li>
    <li>Configuration
        <ol type="a">
            <li>Set preferences</li>
            <li>Configure account</li>
            <li>Test connection</li>
        </ol>
    </li>
    <li>Usage
        <ol type="a">
            <li>Create a project</li>
            <li>Add users</li>
            <li>Start working</li>
        </ol>
    </li>
</ol>
```

## List Styling with CSS

### Remove Bullets

```css
ul {
    list-style: none;
}
```

### Custom Bullets

```css
ul {
    list-style-image: url('checkmark.png');
}
```

### List Style Position

```css
/* Outside (default) */
ul {
    list-style-position: outside;
}

/* Inside */
ul {
    list-style-position: inside;
}
```

### Styling Nested Lists

```css
/* First level - circles */
ul {
    list-style-type: circle;
}

/* Second level - squares */
ul ul {
    list-style-type: square;
}

/* Third level - discs */
ul ul ul {
    list-style-type: disc;
}
```

## List Accessibility

### Labels for Screen Readers

```html
<nav aria-label="Main navigation">
    <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about">About</a></li>
    </ul>
</nav>
```

### Semantic Structure

```html
<!-- Good: Clear structure -->
<ul>
    <li><strong>HTML</strong> - Structure</li>
    <li><strong>CSS</strong> - Styling</li>
    <li><strong>JavaScript</strong> - Interactivity</li>
</ul>

<!-- Less semantic -->
<p>
    • HTML - Structure<br>
    • CSS - Styling<br>
    • JavaScript - Interactivity
</p>
```

## Common List Patterns

### Navigation Menu

```html
<nav>
    <ul class="nav-menu">
        <li><a href="/">Home</a></li>
        <li>
            <a href="/products">Products</a>
            <ul class="submenu">
                <li><a href="/products/software">Software</a></li>
                <li><a href="/products/services">Services</a></li>
            </ul>
        </li>
        <li><a href="/about">About</a></li>
        <li><a href="/contact">Contact</a></li>
    </ul>
</nav>
```

### Breadcrumb Navigation

```html
<nav aria-label="Breadcrumb">
    <ol>
        <li><a href="/">Home</a></li>
        <li><a href="/products">Products</a></li>
        <li><a href="/products/software">Software</a></li>
        <li aria-current="page">My Software</li>
    </ol>
</nav>
```

### Step-by-Step Instructions

```html
<ol>
    <li>Open the software</li>
    <li>Click on "New Project"</li>
    <li>Enter a project name</li>
    <li>Select your preferences</li>
    <li>Click "Create"</li>
</ol>
```

### FAQ Section

```html
<dl>
    <dt>How do I reset my password?</dt>
    <dd>
        <ol>
            <li>Click "Forgot Password" on the login page</li>
            <li>Enter your email address</li>
            <li>Check your email for a reset link</li>
            <li>Click the link and enter your new password</li>
        </ol>
    </dd>
    
    <dt>Can I change my subscription?</dt>
    <dd>Yes, you can change your subscription anytime in your account settings.</dd>
</dl>
```

## Common Mistakes

❌ **Using for layout only** (avoid):
```html
<!-- Wrong: Using list for non-list content -->
<ul>
    <li>Column 1</li>
    <li>Column 2</li>
    <li>Column 3</li>
</ul>
```

❌ **Improper nesting**:
```html
<!-- Wrong -->
<ul>
    <li>Item 1</li>
    <li>Item 2
    <ul>
        <li>Subitem</li>
    </ul>
    <!-- Missing closing </li> -->
    <li>Item 3</li>
</ul>

<!-- Right -->
<ul>
    <li>Item 1</li>
    <li>Item 2
        <ul>
            <li>Subitem</li>
        </ul>
    </li>
    <li>Item 3</li>
</ul>
```

❌ **Wrong list type**:
```html
<!-- Wrong: Using ul for steps -->
<ul>
    <li>First step</li>
    <li>Second step</li>
    <li>Third step</li>
</ul>

<!-- Right -->
<ol>
    <li>First step</li>
    <li>Second step</li>
    <li>Third step</li>
</ol>
```

## Key Takeaways

✅ Use `<ul>` for unordered items

✅ Use `<ol>` for ordered sequences

✅ Use `<dl>` for term-definition pairs

✅ Nest lists properly for hierarchical content

✅ Use semantic markup for accessibility

✅ Combine lists with CSS for flexible styling

✅ Use ARIA labels for complex navigation

---

**Next: [Tables →](07-tables.md)**
