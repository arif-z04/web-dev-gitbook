# Additional Responsive Design Topics

## Media Query Strategies

### Mobile-First
```css
/* Mobile styles (default) */
.container { width: 100%; }

/* Enhanced for tablet */
@media (min-width: 768px) {
    .container { width: 750px; }
}

/* Enhanced for desktop */
@media (min-width: 1024px) {
    .container { width: 970px; }
}
```

### Common Breakpoints
- Small phones: 320px - 480px
- Large phones: 480px - 768px
- Tablets: 768px - 1024px
- Desktops: 1024px - 1440px
- Large screens: 1440px+

## Responsive Patterns

### Navigation
- Mobile: Hamburger menu
- Tablet: Mix of icons and text
- Desktop: Full horizontal menu

### Grids
- Mobile: Single column
- Tablet: Two columns
- Desktop: Three or more columns

### Typography
- Mobile: Smaller font sizes
- Tablet: Medium font sizes
- Desktop: Larger font sizes with longer line lengths

---

Explore these topics in depth in the Final Project section where they're all implemented.
