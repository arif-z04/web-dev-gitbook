# The CSS Box Model Deep Dive

The box model is fundamental to CSS layout:

```
┌─────────────────────────────────┐
│ Margin (Transparent, outside)   │
│ ┌─────────────────────────────┐ │
│ │ Border (Colored line)       │ │
│ │ ┌─────────────────────────┐ │ │
│ │ │ Padding (Inside space)  │ │ │
│ │ │ ┌─────────────────────┐ │ │ │
│ │ │ │ Content             │ │ │ │
│ │ │ │ (Text, images, etc) │ │ │ │
│ │ │ └─────────────────────┘ │ │ │
│ │ └─────────────────────────┘ │ │
│ └─────────────────────────────┘ │
└─────────────────────────────────┘
```

## Box Sizing

### content-box (default)
Width = content only
```css
div { 
    box-sizing: content-box; 
    width: 200px;
    padding: 20px;
    /* Total width: 240px */
}
```

### border-box (recommended)
Width = content + padding + border
```css
div { 
    box-sizing: border-box; 
    width: 200px;
    padding: 20px;
    /* Total width: 200px */
}
```

**Best Practice**: Use `border-box` for all elements:
```css
* { box-sizing: border-box; }
```

## Margin vs Padding
- **Padding**: Inside the element, pushes content inward
- **Margin**: Outside the element, pushes adjacent elements away

## Collapsing Margins
Adjacent margins collapse into one:
```css
h1 { margin-bottom: 20px; }
p { margin-top: 20px; }
/* Distance between h1 and p: 20px (not 40px) */
```

## Shorthand Properties
```css
/* Margin and padding follow: top right bottom left */
margin: 10px;                    /* All sides */
margin: 10px 20px;              /* Top/bottom, left/right */
margin: 10px 20px 30px;         /* Top, left/right, bottom */
margin: 10px 20px 30px 40px;   /* Top, right, bottom, left */

/* Same for padding, border, etc */
```
