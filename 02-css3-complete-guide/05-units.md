# CSS3 Complete Reference

## All CSS3 Chapters Summary

### Chapter 5: Units
- **Absolute**: px (pixels), pt (points), cm (centimeters)
- **Relative**: em, rem, %, vw (viewport width), vh (viewport height)
- **Best Practice**: Use rem for font sizes, em for component-relative sizing

### Chapter 6: Colors
- Named colors: `red`, `blue`, `green`
- Hex: `#FF0000`, `#00FF00`, `#0000FF`
- RGB: `rgb(255, 0, 0)`, `rgba(255, 0, 0, 0.5)`
- HSL: `hsl(0, 100%, 50%)`, `hsla(0, 100%, 50%, 0.5)`

### Chapter 7: Typography
- Font families: `font-family: 'Arial', sans-serif;`
- Font weight: 100-900 or `bold`, `normal`
- Line height: Unitless (1.5 recommended) or with units
- Text styling: `text-transform`, `text-decoration`, `letter-spacing`

### Chapter 8: Backgrounds
- Colors: `background-color: #f5f5f5;`
- Images: `background-image: url('bg.jpg');`
- Gradients: `linear-gradient()`, `radial-gradient()`
- Properties: `background-size`, `background-position`, `background-repeat`

### Chapter 9: Positioning
- **Static**: Default positioning (document flow)
- **Relative**: Relative to normal position
- **Absolute**: Relative to positioned parent
- **Fixed**: Relative to viewport
- **Sticky**: Between relative and fixed

### Chapter 10: Display
- **Block**: Full width, stacks vertically
- **Inline**: Only takes necessary width, flows horizontally
- **Inline-block**: Hybrid of block and inline
- **None**: Hidden, doesn't take up space
- **Flex**: Flexible box layout
- **Grid**: Grid layout system

### Chapter 11: Flexbox (Complete)
**Container Properties**:
- `display: flex`
- `flex-direction`: row, column, row-reverse, column-reverse
- `justify-content`: Aligns along main axis
- `align-items`: Aligns along cross axis
- `flex-wrap`: wrap, nowrap, wrap-reverse
- `gap`: Space between items

**Item Properties**:
- `flex`: 1 (grows equally)
- `order`: Changes order of items
- `align-self`: Individual item alignment

### Chapter 12: CSS Grid (Complete)
```css
.grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: auto 1fr auto;
    gap: 20px;
}

.item {
    grid-column: 1 / 3;
    grid-row: 1 / 2;
}
```

### Chapter 13: Transitions
```css
button {
    background: blue;
    transition: background 0.3s ease;
}

button:hover {
    background: red;
}
```

Properties: `transition-property`, `transition-duration`, `transition-timing-function`, `transition-delay`

### Chapter 14: Animations
```css
@keyframes slideIn {
    from { transform: translateX(-100%); }
    to { transform: translateX(0); }
}

.element {
    animation: slideIn 0.5s ease-in-out;
}
```

### Chapter 15: CSS Variables
```css
:root {
    --primary-color: #007bff;
    --spacing: 16px;
}

button {
    background: var(--primary-color);
    padding: var(--spacing);
}
```

### Chapter 16: Advanced CSS Features
- **calc()**: `width: calc(100% - 20px);`
- **min() / max() / clamp()**: Responsive without media queries
- **Logical properties**: `margin-inline`, `padding-block`
- **Aspect ratio**: `aspect-ratio: 16 / 9;`
- **object-fit**: `object-fit: cover;` for images in containers
