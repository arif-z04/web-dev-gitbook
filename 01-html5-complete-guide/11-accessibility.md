# 11. Accessibility (A11Y)

## Why Accessibility Matters

Approximately 1 in 4 adults have some type of disability. Accessible websites benefit everyone - not just people with disabilities.

## WCAG Standards

Web Content Accessibility Guidelines (WCAG) follow four principles:

1. **Perceivable** - Information must be perceivable to senses
2. **Operable** - Users must be able to operate interface
3. **Understandable** - Content and operation must be understandable
4. **Robust** - Compatible with assistive technologies

## Semantic HTML

Using semantic elements is the foundation of accessibility:

```html
<!-- Bad: No semantic meaning -->
<div class="button" onclick="submit()">Submit</div>

<!-- Good: Semantic button -->
<button type="submit">Submit</button>
```

## Alt Text for Images

```html
<!-- Bad: No description -->
<img src="photo.jpg">

<!-- Good: Descriptive alt text -->
<img src="photo.jpg" alt="Team of five developers working at their desks">
```

## ARIA Attributes

ARIA (Accessible Rich Internet Applications) adds accessibility info:

```html
<!-- Current page indicator -->
<nav>
    <a href="/">Home</a>
    <a href="/about" aria-current="page">About</a>
</nav>

<!-- Describes page region -->
<nav aria-label="Main navigation">
    <ul>...</ul>
</nav>

<!-- Describes dialog -->
<div role="dialog" aria-labelledby="dialog-title">
    <h2 id="dialog-title">Confirm Action</h2>
</div>

<!-- Hidden label text -->
<button aria-label="Close menu">×</button>
```

## Keyboard Navigation

Ensure all functionality is keyboard accessible:

```html
<!-- Make custom elements focusable -->
<div tabindex="0" role="button">Custom Button</div>

<!-- Disable tabbing if not needed -->
<div tabindex="-1">Not in tab order</div>

<!-- Skip to main content link -->
<a href="#main" class="skip-link">Skip to main content</a>
```

## Form Accessibility

```html
<!-- Always use labels -->
<label for="username">Username:</label>
<input id="username" type="text">

<!-- Describe error messages -->
<input aria-describedby="email-error" type="email">
<span id="email-error" role="alert">Please enter a valid email</span>

<!-- Mark required fields -->
<label for="password">Password <span aria-label="required">*</span></label>
<input id="password" type="password" required>
```

## Headings for Structure

```html
<!-- Proper heading hierarchy -->
<h1>Main Title</h1>
<h2>Section 1</h2>
<h3>Subsection</h3>
<h2>Section 2</h2>

<!-- Never skip levels -->
<h1>Main Title</h1>
<h3>Wrong - skipped h2</h3>
```

## Color Contrast

Minimum contrast ratios (WCAG AA):
- Normal text: 4.5:1
- Large text: 3:1

```css
/* Good contrast -->
body { color: #000; background: #fff; }   /* 21:1 */

/* Poor contrast - don't use -->
body { color: #999; background: #ddd; }   /* 1.23:1 */
```

## Language Specification

```html
<!-- Specify page language -->
<html lang="en">

<!-- Specify content language changes -->
<p>Welcome to my website <span lang="es">¡Bienvenido!</span></p>
```

## Text Alternatives

```html
<!-- Describe infographics -->
<img src="chart.png" alt="Sales increased 40% from Q1 to Q4">

<!-- Provide transcript for audio -->
<audio controls>
    <source src="podcast.mp3">
</audio>
<details>
    <summary>Transcript</summary>
    <p>Full transcript text here...</p>
</details>

<!-- Caption for video -->
<video controls>
    <source src="video.mp4">
    <track kind="captions" src="captions.vtt">
</video>
```

## Testing Accessibility

### Browser DevTools
- Lighthouse audit (accessibility score)
- Axe DevTools extension
- WAVE extension

### Manual Testing
1. Navigate with keyboard only (no mouse)
2. Test with screen reader
3. Zoom to 200% and 400%
4. Test with browser's high contrast mode

## Complete Accessible Form

```html
<form>
    <fieldset>
        <legend>Contact Information</legend>
        
        <div class="form-group">
            <label for="fullname">Full Name <span aria-label="required">*</span></label>
            <input 
                id="fullname" 
                type="text" 
                required
                aria-describedby="fullname-help">
            <small id="fullname-help">Your full name as it appears on documents</small>
        </div>
        
        <div class="form-group">
            <label for="email">Email Address <span aria-label="required">*</span></label>
            <input 
                id="email" 
                type="email" 
                required
                aria-describedby="email-error">
            <span id="email-error" role="alert" class="error" style="display:none;">
                Please enter a valid email address
            </span>
        </div>
        
        <div class="form-group">
            <label for="message">Message</label>
            <textarea 
                id="message" 
                aria-describedby="message-help"></textarea>
            <small id="message-help">Maximum 1000 characters</small>
        </div>
        
        <button type="submit">Send Message</button>
    </fieldset>
</form>
```

## Common Accessibility Mistakes

❌ **No alt text for images**:
```html
<!-- Wrong -->
<img src="logo.png">

<!-- Right -->
<img src="logo.png" alt="Company logo">
```

❌ **Color as only indicator**:
```html
<!-- Wrong: Only color indicates error -->
<input style="background: red;">

<!-- Right: Color + text -->
<input aria-invalid="true">
<span>This field is required</span>
```

❌ **Auto-playing content**:
```html
<!-- Wrong -->
<audio autoplay>

<!-- Right -->
<audio controls>
```

## Key Takeaways

✅ Use semantic HTML elements

✅ Provide descriptive alt text for images

✅ Ensure keyboard navigation works

✅ Maintain color contrast ratios

✅ Use ARIA labels appropriately

✅ Test with accessibility tools

✅ Consider all users in design

---

**Next: [SEO Fundamentals →](12-seo-fundamentals.md)**
