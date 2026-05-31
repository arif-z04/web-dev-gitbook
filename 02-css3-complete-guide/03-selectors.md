# CSS Selectors Reference

All CSS3 selectors with examples and use cases:

## Element Selectors
```css
p { color: blue; }
div { margin: 0; }
```

## Class Selectors
```css
.intro { font-weight: bold; }
.button { padding: 10px 20px; }
```

## ID Selectors
```css
#header { background: gray; }
#footer { margin-top: 40px; }
```

## Attribute Selectors
```css
[href] { color: blue; }
[type="text"] { border: 1px solid #ccc; }
[class~="highlight"] { background: yellow; }
```

## Pseudo-Classes
```css
a:hover { color: red; }
li:first-child { font-weight: bold; }
li:nth-child(2n) { background: #f5f5f5; }
p:last-of-type { margin-bottom: 0; }
```

## Pseudo-Elements
```css
p::first-line { font-weight: bold; }
p::first-letter { font-size: 2em; }
button::before { content: "→ "; }
```

## Combinators
```css
div p { color: blue; }           /* Descendant */
div > p { color: blue; }         /* Child */
h1 + p { margin-top: 0; }       /* Adjacent sibling */
h1 ~ p { color: gray; }         /* General sibling */
```

## Multiple Selectors
```css
h1, h2, h3 { color: navy; }
.btn, button { padding: 10px; }
```
