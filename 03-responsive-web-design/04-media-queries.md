# Media Queries Deep Dive

## Media Query Syntax

```css
@media (condition) {
    /* CSS rules when condition is true */
}
```

## Common Media Query Features

### Width
```css
@media (min-width: 768px) { }
@media (max-width: 767px) { }
@media (min-width: 768px) and (max-width: 1023px) { }
```

### Orientation
```css
@media (orientation: portrait) { }
@media (orientation: landscape) { }
```

### Hover
```css
@media (hover: hover) {
    button:hover { background: blue; }
}
```

### Color Scheme
```css
@media (prefers-color-scheme: dark) {
    body { background: #1a1a1a; color: #fff; }
}
```

### Reduced Motion (Accessibility)
```css
@media (prefers-reduced-motion: reduce) {
    * { animation: none; transition: none; }
}
```

## Best Practices

1. Start with mobile styles
2. Add media queries for larger screens
3. Use meaningful breakpoints
4. Test on real devices
5. Consider all query types
