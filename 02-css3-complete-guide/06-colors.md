# Colors in CSS3

CSS3 offers multiple ways to specify colors for maximum flexibility and compatibility.

## Named Colors

```css
body { background: white; }
h1 { color: navy; }
p { color: gray; }
a { color: blue; }
```

Common colors: red, blue, green, black, white, gray, yellow, orange, pink, purple, etc.

## Hexadecimal Colors

```css
/* 3-digit hex (shorthand) */
#FFF /* White */
#000 /* Black */

/* 6-digit hex */
#FFFFFF /* White */
#000000 /* Black */
#FF0000 /* Red */
#00FF00 /* Green */
#0000FF /* Blue */
```

## RGB Colors

```css
rgb(255, 0, 0)      /* Red */
rgb(0, 255, 0)      /* Green */
rgb(0, 0, 255)      /* Blue */
rgb(128, 128, 128)  /* Gray */
```

## RGBA Colors (With Transparency)

```css
rgba(255, 0, 0, 0.5)    /* 50% opaque red */
rgba(0, 0, 0, 0.8)      /* 80% opaque black */
rgba(255, 255, 255, 0)  /* Fully transparent white */
```

## HSL Colors (Hue, Saturation, Lightness)

```css
hsl(0, 100%, 50%)      /* Red */
hsl(120, 100%, 50%)    /* Green */
hsl(240, 100%, 50%)    /* Blue */
hsl(0, 0%, 50%)        /* Gray */
```

## HSLA Colors (With Transparency)

```css
hsla(0, 100%, 50%, 0.5)  /* 50% opaque red */
```

## Linear Gradients

```css
background: linear-gradient(to right, red, yellow);
background: linear-gradient(45deg, red, blue);
background: linear-gradient(to right, red, green, blue);
```

## Radial Gradients

```css
background: radial-gradient(circle, red, yellow);
background: radial-gradient(ellipse, blue 0%, white 100%);
```

## Best Practices

✅ Use consistent color naming
✅ Define colors as CSS variables
✅ Test color contrast for accessibility
✅ Consider colorblind users

---

Continue learning about CSS fundamentals and advanced techniques.
