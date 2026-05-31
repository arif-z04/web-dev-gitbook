# 5. Images

## The Image Element

```html
<img src="photo.jpg" alt="Description of the photo">
```

## Essential Image Attributes

### src (Required)

Specifies the image file location:

```html
<!-- Relative path -->
<img src="images/photo.jpg" alt="Photo">

<!-- Absolute path -->
<img src="https://example.com/images/photo.jpg" alt="Photo">

<!-- Current folder -->
<img src="photo.jpg" alt="Photo">
```

### alt (Required)

Provides alternative text for accessibility and SEO:

```html
<!-- Good alt text - describes the image -->
<img src="sunset.jpg" alt="Sunset over the ocean at dusk">

<!-- Bad alt text -->
<img src="image.jpg" alt="image">

<!-- Decorative image (empty alt) -->
<img src="divider.png" alt="">
```

## Why Alt Text Matters

1. **Accessibility**: Screen readers read alt text to blind users
2. **SEO**: Search engines use alt text to understand images
3. **Performance**: Shows if image fails to load
4. **Mobile**: Displays on slow connections
5. **Mobile users**: Disabled images on data plans

### Good Alt Text Guidelines

✅ Describe the content, not "image of" or "picture of"
✅ Keep it concise (under 125 characters usually)
✅ Use empty alt="" for purely decorative images
✅ Include relevant context
✅ Write as if describing to someone who can't see it

## Additional Image Attributes

### width and height

Prevents layout shift:

```html
<img src="photo.jpg" alt="Photo" width="800" height="600">
```

**Why specify dimensions?**
- Browser reserves space while loading
- Prevents content jumping when image loads
- Improves perceived performance

### title

Shows tooltip on hover:

```html
<img src="photo.jpg" alt="Sunset" title="Click to enlarge">
```

### loading

Lazy loading for performance:

```html
<!-- Lazy load image (supported browsers) -->
<img src="photo.jpg" alt="Photo" loading="lazy">

<!-- Eager loading (default) -->
<img src="hero.jpg" alt="Hero" loading="eager">
```

### decoding

Specifies decoding preference:

```html
<img src="photo.jpg" alt="Photo" decoding="async">
```

## Image Formats and When to Use Them

| Format | Use Case | Pros | Cons |
|--------|----------|------|------|
| **JPG** | Photos, complex images | Excellent compression, small file size | Lossy, not transparent |
| **PNG** | Logos, screenshots, graphics | Transparent background, lossless | Larger file size |
| **GIF** | Animations, simple graphics | Animation support | Limited colors, large files |
| **WebP** | Modern web (all formats) | Best compression | Not supported in all browsers |
| **SVG** | Icons, logos, vector graphics | Scalable, small, interactive | Only for vector graphics |

## Responsive Images

### max-width Technique

```html
<style>
    img {
        max-width: 100%;
        height: auto;
    }
</style>

<img src="large-image.jpg" alt="Responsive image">
```

### Picture Element (Art Direction)

```html
<picture>
    <!-- Small screens -->
    <source media="(max-width: 600px)" srcset="mobile.jpg">
    
    <!-- Medium screens -->
    <source media="(max-width: 1200px)" srcset="tablet.jpg">
    
    <!-- Large screens and fallback -->
    <img src="desktop.jpg" alt="Responsive image">
</picture>
```

### srcset (Resolution Switching)

```html
<!-- Different resolutions for different devices -->
<img 
    src="image.jpg"
    srcset="image-small.jpg 480w,
            image-medium.jpg 768w,
            image-large.jpg 1200w"
    sizes="(max-width: 600px) 100vw,
           (max-width: 1200px) 50vw,
           800px"
    alt="Responsive image">
```

## Figure and Figcaption

Semantically group images with captions:

```html
<figure>
    <img src="chart.jpg" alt="Sales growth chart">
    <figcaption>Figure 1: Sales growth from 2022-2026</figcaption>
</figure>
```

### Multiple Images in Figure

```html
<figure>
    <img src="photo1.jpg" alt="Mountain landscape">
    <img src="photo2.jpg" alt="Ocean view">
    <figcaption>Scenic locations from our 2026 travel</figcaption>
</figure>
```

## Image Best Practices

✅ **Use descriptive, meaningful filenames**
```html
<!-- Good -->
<img src="office-team-meeting.jpg" alt="Our team in a meeting">

<!-- Bad -->
<img src="img123.jpg" alt="meeting">
```

✅ **Optimize image file sizes**
- Compress images before uploading
- Use appropriate formats
- Consider using WebP with fallbacks

✅ **Always include alt text**
- Never leave it blank (unless decorative)
- Describe the content, not "image of..."

✅ **Specify dimensions**
- Prevents layout shift
- Improves performance

✅ **Use lazy loading for off-screen images**
```html
<img src="product-image.jpg" alt="Product" loading="lazy">
```

✅ **Consider accessibility**
- Sufficient color contrast
- Text not embedded in images
- Decorative images have empty alt

## Common Image Mistakes

❌ **Missing alt text**:
```html
<!-- Wrong -->
<img src="photo.jpg">

<!-- Right -->
<img src="photo.jpg" alt="Descriptive text">
```

❌ **Vague alt text**:
```html
<!-- Wrong -->
<img src="photo.jpg" alt="image">

<!-- Right -->
<img src="team-photo.jpg" alt="Our software development team at the office">
```

❌ **Always using title instead of alt**:
```html
<!-- Incomplete -->
<img src="photo.jpg" title="My Photo">

<!-- Complete -->
<img src="photo.jpg" alt="My Photo" title="Click to enlarge">
```

❌ **Not specifying dimensions**:
```html
<!-- Causes layout shift -->
<img src="photo.jpg" alt="Photo">

<!-- Better -->
<img src="photo.jpg" alt="Photo" width="400" height="300">
```

## Complete Example: Product Gallery

```html
<section class="product-gallery">
    <figure>
        <picture>
            <source media="(max-width: 600px)" srcset="product-small.webp">
            <source media="(max-width: 1200px)" srcset="product-medium.webp">
            <img 
                src="product-large.jpg" 
                alt="Premium Laptop - Silver, Front View"
                width="800"
                height="600"
                loading="lazy">
        </picture>
        <figcaption>Our flagship laptop in silver</figcaption>
    </figure>
    
    <figure>
        <img 
            src="product-side.jpg" 
            alt="Premium Laptop - Silver, Side View"
            width="800"
            height="600"
            loading="lazy">
        <figcaption>Elegant side profile</figcaption>
    </figure>
</section>
```

## Key Takeaways

✅ Always include descriptive alt text

✅ Use appropriate image formats

✅ Implement responsive images with srcset or picture

✅ Specify width and height to prevent layout shift

✅ Use lazy loading for performance

✅ Use figure and figcaption for semantic image grouping

✅ Optimize images before uploading

---

**Next: [Lists →](06-lists.md)**
