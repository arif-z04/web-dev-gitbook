# 20 Golden Rules of Responsive Web Design

## 1. Mobile First
Design for mobile devices first, then progressively enhance for larger screens.

```css
/* Mobile-first approach */
.container { width: 100%; }

@media (min-width: 768px) {
    .container { width: 750px; }
}
```

## 2. Use Semantic HTML
Proper HTML structure improves accessibility and SEO.

```html
<!-- Good: Semantic -->
<header><h1>Title</h1></header>
<nav>Navigation</nav>
<main>Content</main>
<footer>Footer</footer>

<!-- Bad: Non-semantic -->
<div class="header"><div class="title">Title</div></div>
```

## 3. Avoid Fixed Widths
Use flexible, percentage-based widths instead.

```css
/* Bad: Fixed width */
.container { width: 960px; }

/* Good: Flexible */
.container { width: 90%; max-width: 1200px; }
```

## 4. Prefer Flexbox and Grid
Use modern layout techniques for flexible designs.

```css
/* Flexbox */
.container { display: flex; flex-wrap: wrap; }

/* CSS Grid */
.grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); }
```

## 5. Use Relative Units
Use rem, em, and % instead of px.

```css
/* Better */
font-size: 1.5rem;
padding: 1em;
width: 90%;

/* Less flexible */
font-size: 24px;
padding: 16px;
width: 960px;
```

## 6. Make Images Flexible
```css
img {
    max-width: 100%;
    height: auto;
}

picture { display: block; width: 100%; }
```

## 7. Design for Touch Devices
Make tap targets large enough (min 44px x 44px).

```css
button {
    padding: 12px 20px;  /* At least 44px height */
    font-size: 16px;
    min-height: 44px;
}
```

## 8. Maintain Accessibility
Design with accessibility in mind from the start.

```html
<button aria-label="Close menu">×</button>
<img src="photo.jpg" alt="Descriptive alt text">
```

## 9. Optimize Performance
- Minimize HTTP requests
- Optimize images
- Use CSS instead of images where possible

## 10. Test on Multiple Devices
- Test on real devices
- Use browser dev tools
- Check multiple breakpoints

## 11. Keep Consistent Spacing
Use a spacing scale for consistency.

```css
:root {
    --space-xs: 4px;
    --space-sm: 8px;
    --space-md: 16px;
    --space-lg: 24px;
    --space-xl: 32px;
}

.button { padding: var(--space-sm) var(--space-md); }
```

## 12. Use CSS Variables
Reusable values for colors, fonts, spacing.

```css
:root {
    --primary: #007bff;
    --font-stack: Arial, sans-serif;
    --border-radius: 4px;
}

body { font-family: var(--font-stack); }
```

## 13. Avoid Excessive Media Queries
Keep media queries minimal with flexible design.

```css
/* Instead of many breakpoints: */
.container { max-width: 90%; }
img { max-width: 100%; }
```

## 14. Follow Progressive Enhancement
Core content and functionality work for everyone.

```html
<!-- Works without CSS -->
<h1>Title</h1>
<p>Content</p>

<!-- Enhanced with CSS for better display -->
```

## 15. Maintain Readable Typography
- Base font size: 16px
- Line height: 1.5-1.6
- Line length: 45-75 characters

```css
body {
    font-size: 16px;
    line-height: 1.6;
    max-width: 70ch;
}
```

## 16. Ensure Color Contrast
Minimum contrast ratio 4.5:1 for normal text.

```css
/* Good contrast */
body { color: #000; background: #fff; }  /* 21:1 */

/* Poor contrast - avoid */
body { color: #999; background: #ddd; }  /* 1.23:1 */
```

## 17. Minimize Layout Shift
Reserve space for dynamic content.

```css
/* Reserve space for images */
img { aspect-ratio: 16 / 9; }

/* Reserve space for ads */
.ad-container { min-height: 250px; }
```

## 18. Use Modern CSS Features
- CSS Grid
- Flexbox
- CSS Variables
- Calc()
- Clamp()

```css
font-size: clamp(16px, 2vw, 32px);
grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
```

## 19. Keep Components Reusable
Build modular, component-based layouts.

```css
.card {
    padding: 20px;
    border-radius: 4px;
    background: #f5f5f5;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.card.featured { background: #e8f4f8; }
.card.error { background: #fee; }
```

## 20. Prioritize User Experience
- Fast load times
- Intuitive navigation
- Clear calls-to-action
- Accessible to everyone

---

**These 20 rules form the foundation of modern, professional web design.**
