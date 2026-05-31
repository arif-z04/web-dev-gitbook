# 3. Text Elements

## Working with Text Content

HTML provides various elements for different types of text content. Using the right element is important for semantic meaning, accessibility, and SEO.

## Headings

Headings organize content hierarchically and help both users and search engines understand page structure.

```html
<h1>Main Page Title</h1>
<h2>Section Title</h2>
<h3>Subsection Title</h3>
<h4>Minor Section</h4>
<h5>Even Smaller Section</h5>
<h6>Smallest Heading</h6>
```

### Heading Best Practices

✅ **Use only one `<h1>` per page** - It's the main topic
```html
<h1>Web Development Guide</h1>
```

✅ **Don't skip heading levels** - Go h1 → h2 → h3, not h1 → h3
```html
<!-- Right -->
<h1>Main Title</h1>
<h2>Section</h2>
<h3>Subsection</h3>

<!-- Wrong -->
<h1>Main Title</h1>
<h3>Subsection</h3>
```

✅ **Use headings for structure, not styling**
```html
<!-- Wrong - using h1 just to make text big -->
<h1>Welcome</h1>

<!-- Right - using heading semantically -->
<h1>Welcome to My Website</h1>
```

## Paragraphs

```html
<p>This is a paragraph of text.</p>
<p>Each paragraph is a distinct block of text.</p>
```

### Multi-line Text

```html
<p>
    This paragraph spans
    multiple lines in the code,
    but will display as one
    continuous paragraph.
</p>
```

**Important**: Whitespace in HTML is collapsed. Multiple spaces, tabs, and line breaks are treated as single spaces.

## Line Breaks and Horizontal Rules

### Line Break (`<br>`)

Creates a single line break:

```html
<p>
    First line<br>
    Second line<br>
    Third line
</p>
```

### Horizontal Rule (`<hr>`)

Creates a thematic break:

```html
<p>Section 1</p>
<hr>
<p>Section 2</p>
```

## Strong and Emphasis

### Strong (`<strong>`)

Indicates content of strong importance:

```html
<p><strong>Warning:</strong> This is important!</p>
<p><strong>Never</strong> mix production and development databases.</p>
```

**Display**: Bold text
**Semantics**: Strong importance
**Screen readers**: Emphasize with different tone

### Emphasis (`<em>`)

Indicates stressed or emphasized content:

```html
<p>This is <em>really</em> important.</p>
<p>You <em>must</em> validate your HTML.</p>
```

**Display**: Italic text
**Semantics**: Emphasis/stress
**Screen readers**: Alter pronunciation

### Bold vs Strong

```html
<!-- Semantic emphasis -->
<p><strong>Warning:</strong> Hot surface!</p>

<!-- For styling only (not recommended) -->
<p><b>Product:</b> Web Framework</p>
```

### Italic vs Emphasis

```html
<!-- Semantic emphasis -->
<p>This is <em>really</em> important.</p>

<!-- For styling (less common) -->
<p>The book <i>1984</i> is a classic.</p>
```

## Superscript and Subscript

### Superscript (`<sup>`)

Renders text above the baseline:

```html
<p>E = mc<sup>2</sup></p>
<p>This is a reference<sup>[1]</sup></p>
```

### Subscript (`<sub>`)

Renders text below the baseline:

```html
<p>H<sub>2</sub>O</p>
<p>The molecular formula for water is H<sub>2</sub>O</p>
```

## Quotes

### Block Quote (`<blockquote>`)

For longer quotations:

```html
<blockquote>
    <p>The only way to do great work is to love what you do.</p>
    <footer>— Steve Jobs</footer>
</blockquote>
```

**CSS for styling**:
```css
blockquote {
    border-left: 4px solid #007bff;
    padding-left: 1rem;
    margin-left: 0;
    color: #666;
}
```

### Inline Quote (`<q>`)

For short, inline quotations:

```html
<p>Steve Jobs said <q>the only way to do great work is to love what you do</q>.</p>
```

### Citation (`<cite>`)

References the source of a quote:

```html
<blockquote>
    <p>Innovation distinguishes between a leader and a follower.</p>
    <footer>— <cite>Steve Jobs</cite></footer>
</blockquote>
```

## Code and Preformatted Text

### Inline Code (`<code>`)

For code snippets within text:

```html
<p>Use the <code>console.log()</code> function to debug.</p>
```

### Code Block (`<pre>`)

Preserves formatting and whitespace:

```html
<pre>
function hello() {
    console.log("Hello, World!");
}
</pre>
```

### Pre-formatted Code

Combined for code blocks:

```html
<pre><code>
const greeting = (name) => {
    return `Hello, ${name}!`;
};
</code></pre>
```

**CSS styling**:
```css
pre {
    background-color: #f4f4f4;
    border: 1px solid #ddd;
    padding: 1rem;
    overflow-x: auto;
    border-radius: 4px;
}

code {
    font-family: 'Courier New', monospace;
    font-size: 0.9em;
}
```

## Keyboard Input (`<kbd>`)

Represents user keyboard input:

```html
<p>Press <kbd>Ctrl</kbd> + <kbd>C</kbd> to copy.</p>
```

## Variable (`<var>`)

Represents a variable or placeholder:

```html
<p>The formula is <var>E</var> = <var>m</var><var>c</var><sup>2</sup></p>
```

## Deleted and Inserted Text

### Deleted Text (`<del>`)

```html
<p><del>Old price: $100</del> New price: $79</p>
```

### Inserted Text (`<ins>`)

```html
<p>The conference is <del>May 15</del> <ins>June 1</ins></p>
```

**With datetime attribute**:

```html
<p>
    <del datetime="2026-05-31T10:00Z">Old information</del>
    <ins datetime="2026-06-01T14:30Z">New information</ins>
</p>
```

## Abbreviation (`<abbr>`)

Defines an abbreviation:

```html
<p>The <abbr title="HyperText Markup Language">HTML</abbr> specification...</p>
<p><abbr title="Application Programming Interface">API</abbr> stands for Application Programming Interface.</p>
```

**Browser behavior**: Typically shows a dotted underline with tooltip on hover.

## Time Element (`<time>`)

Represents a specific date/time:

```html
<p>The event is on <time datetime="2026-06-15">June 15, 2026</time></p>
<p>Dinner is at <time>19:00</time></p>
<p>Published <time datetime="2026-05-31T14:30:00Z">May 31, 2026 at 2:30 PM</time></p>
```

**Machine-readable format** (datetime attribute):
- Dates: `2026-05-31`
- Times: `14:30`
- DateTime: `2026-05-31T14:30:00Z`

## Address (`<address>`)

Contact information:

```html
<address>
    John Doe<br>
    123 Web Street<br>
    Web City, WC 12345<br>
    <a href="mailto:john@example.com">john@example.com</a>
</address>
```

## Mark (`<mark>`)

Highlights text:

```html
<p>This is <mark>important</mark> information.</p>
```

**CSS default**: Yellow background

## Small Text (`<small>`)

Side comments or legal text:

```html
<p>
    Regular price: $100
    <small>(Discounted from $150)</small>
</p>
```

## Text Directionality (`<bdi>` and `<bdo>`)

### Bidirectional Isolation (`<bdi>`)

```html
<p>Username: <bdi>مرحبا</bdi></p>
```

### Bidirectional Override (`<bdo>`)

```html
<p><bdo dir="rtl">This text goes right to left</bdo></p>
```

## Practical Example: Blog Post

```html
<article>
    <h1>Getting Started with HTML5</h1>
    
    <p>
        Published on <time datetime="2026-05-31">May 31, 2026</time>
        <small>(Updated June 1)</small>
    </p>
    
    <p>
        <strong>HTML5</strong> is the current standard for web markup.
        It provides semantic elements that make your code more <em>meaningful</em>.
    </p>
    
    <blockquote>
        <p>HTML is the foundation of the web.</p>
        <footer>— Web Standards</footer>
    </blockquote>
    
    <p>
        To learn more about <abbr title="HyperText Markup Language">HTML</abbr>,
        visit the <cite>MDN Web Docs</cite>.
    </p>
    
    <pre><code>&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;title&gt;My Page&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h1&gt;Hello World&lt;/h1&gt;
&lt;/body&gt;
&lt;/html&gt;</code></pre>
</article>
```

## Key Takeaways

✅ Use semantic text elements for proper meaning

✅ One `<h1>` per page, proper heading hierarchy

✅ Use `<strong>` for importance, `<em>` for emphasis

✅ Use `<code>` and `<pre>` for code snippets

✅ Use `<abbr>` with title for abbreviations

✅ Use `<time>` with datetime for machine-readable dates

---

**Next: [Links and Navigation →](04-links-navigation.md)**
