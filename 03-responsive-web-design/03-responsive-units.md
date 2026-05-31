# Responsive Units Guide

## Understanding Responsive Units

### Absolute Units
```css
/* Fixed size - avoid for responsive design */
width: 100px;
font-size: 16px;
```

### Relative Units

#### em (Relative to parent)
```css
parent { font-size: 16px; }
child { font-size: 2em; } /* 32px */
```

#### rem (Relative to root)
```css
html { font-size: 16px; }
body { font-size: 1rem; } /* 16px */
h1 { font-size: 3rem; } /* 48px */
```

**Best Practice**: Use rem for most measurements

#### Percentage (%)
```css
.container { width: 100%; }
.column { width: 33.333%; }
```

#### Viewport Units
```css
width: 100vw;  /* Full viewport width */
height: 100vh; /* Full viewport height */
```

## When to Use Which

- **rem**: Font sizes and spacing
- **%**: Widths and flexible layouts
- **em**: Component-relative sizing
- **px**: Borders, shadows (rarely for layout)
- **vw/vh**: Full-screen sections

---

Continue learning about responsive techniques in the guide.
