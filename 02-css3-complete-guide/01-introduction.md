# 1. Introduction to CSS

## What is CSS?

CSS stands for **Cascading Style Sheets**. It's the language used to style and layout web pages — controlling colors, fonts, spacing, positioning, and responsive design.

## Why CSS Matters

HTML provides structure, but CSS provides presentation:

```
HTML + CSS + JavaScript = Complete Web Application
Structure + Presentation + Behavior
```

## Key Concepts

### The Cascade

Styles "cascade" from parent to child elements:

```html
<body style="color: blue;">
    <p>This text is blue</p> <!-- Inherits color from body -->
</body>
```

### Inheritance

Some properties inherit from parent elements:

```css
body {
    font-family: Arial;  /* Inherited by all text elements */
}

strong {
    font-weight: bold;   /* Already bold by default */
}
```

### Specificity

More specific selectors override less specific ones:

```css
p { color: blue; }           /* 0-0-1 specificity */
.text { color: red; }        /* 0-1-0 specificity - wins! */
#main { color: green; }      /* 1-0-0 specificity - always wins */
```

## CSS Syntax

```css
selector {
    property: value;
    property2: value2;
}
```

Example:

```css
h1 {
    color: blue;
    font-size: 32px;
    margin-bottom: 20px;
}
```

## Where to Put CSS

### 1. Inline Styles (Not Recommended)

```html
<h1 style="color: blue; font-size: 32px;">Title</h1>
```

**Problems**: Hard to maintain, can't reuse styles

### 2. Internal Styles (Acceptable)

```html
<head>
    <style>
        h1 { color: blue; }
        p { color: gray; }
    </style>
</head>
```

**Good for**: Single page templates

### 3. External Stylesheet (Best)

```html
<head>
    <link rel="stylesheet" href="styles.css">
</head>
```

**Advantages**:
- Reusable across multiple pages
- Cached by browsers
- Easier to maintain
- Smaller HTML files

## CSS Box Model

Every element is a box:

```
┌─────────────────────────┐
│      Margin (outside)   │
│  ┌───────────────────┐  │
│  │ Border            │  │
│  │ ┌───────────────┐ │  │
│  │ │ Padding       │ │  │
│  │ │ ┌───────────┐ │ │  │
│  │ │ │ Content   │ │ │  │
│  │ │ └───────────┘ │ │  │
│  │ └───────────────┘ │  │
│  └───────────────────┘  │
└─────────────────────────┘
```

## Selectors Overview

```css
/* Element selector */
p { color: blue; }

/* Class selector */
.intro { font-weight: bold; }

/* ID selector */
#header { background: gray; }

/* Multiple selectors */
h1, h2, h3 { color: navy; }

/* Descendant selector */
.intro p { margin: 10px; }
```

## Colors

```css
body {
    color: red;              /* Named color */
    background-color: #ff0000; /* Hex */
    border-color: rgb(255, 0, 0); /* RGB */
}
```

## Fonts

```css
body {
    font-family: Arial, Helvetica, sans-serif;
    font-size: 16px;
    font-weight: bold;
    line-height: 1.6;
}
```

## Spacing

```css
p {
    margin: 20px;    /* Outside spacing */
    padding: 10px;   /* Inside spacing */
}
```

## Common Mistakes

❌ **Using inline styles**:
```css
/* Bad */
<p style="color: red;">

/* Good */
<p class="error">
/* In CSS: .error { color: red; } */
```

❌ **Over-specific selectors**:
```css
/* Bad */
body > div > section > .main > p { color: blue; }

/* Good */
.main p { color: blue; }
```

❌ **Not using external stylesheets**:
```html
<!-- Bad: Styles all in HTML -->
<!-- Good: Link external CSS file -->
<link rel="stylesheet" href="styles.css">
```

## History of CSS

- **CSS 1 (1996)** - Basic styling
- **CSS 2 (1998)** - Positioning and absolute/relative
- **CSS 2.1 (2011)** - Clarifications and bug fixes
- **CSS 3 (2011-present)** - Modular specifications
  - Flexbox
  - CSS Grid
  - Animations
  - Media Queries
  - Custom Properties
  - And much more...

## CSS Today

Modern CSS includes:
- Flexbox for 1D layouts
- CSS Grid for 2D layouts
- Media queries for responsive design
- CSS Variables for reusable values
- Animations and transitions for motion
- Advanced selectors and functions

## Key Takeaways

✅ CSS styles HTML elements

✅ Use external stylesheets

✅ Understand the cascade and specificity

✅ Know the box model

✅ Use classes and IDs instead of inline styles

✅ CSS is constantly evolving with modern features

---

**Next: [CSS Syntax →](02-css-syntax.md)**
