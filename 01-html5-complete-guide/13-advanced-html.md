# 13. Advanced HTML

## Data Attributes

Store custom data on HTML elements:

```html
<!-- Store product data -->
<div class="product" data-id="12345" data-price="99.99" data-category="electronics">
    <h3>Laptop</h3>
    <p data-description="High-performance laptop">Premium device</p>
</div>
```

Access with JavaScript:

```javascript
const product = document.querySelector('.product');
console.log(product.dataset.id);       // "12345"
console.log(product.dataset.price);    // "99.99"
console.log(product.dataset.category); // "electronics"
```

## SVG (Scalable Vector Graphics)

Embed scalable graphics:

```html
<!-- Inline SVG -->
<svg width="100" height="100">
    <circle cx="50" cy="50" r="40" fill="blue">
</svg>

<!-- SVG as image -->
<img src="logo.svg" alt="Company logo">

<!-- SVG with external file -->
<object data="graphic.svg" type="image/svg+xml"></object>
```

### SVG Example

```html
<svg width="200" height="200" viewBox="0 0 200 200">
    <!-- Circle -->
    <circle cx="100" cy="100" r="80" fill="lightblue" stroke="blue" stroke-width="2">
    
    <!-- Rectangle -->
    <rect x="50" y="50" width="100" height="100" fill="rgba(255,0,0,0.5)">
    
    <!-- Line -->
    <line x1="10" y1="10" x2="190" y2="190" stroke="black" stroke-width="2">
    
    <!-- Text -->
    <text x="100" y="100" text-anchor="middle" font-size="20">SVG</text>
</svg>
```

## Canvas

Draw graphics with JavaScript:

```html
<canvas id="myCanvas" width="400" height="300"></canvas>

<script>
    const canvas = document.getElementById('myCanvas');
    const ctx = canvas.getContext('2d');
    
    // Draw rectangle
    ctx.fillStyle = 'blue';
    ctx.fillRect(10, 10, 100, 50);
    
    // Draw circle
    ctx.beginPath();
    ctx.arc(200, 150, 50, 0, Math.PI * 2);
    ctx.fillStyle = 'red';
    ctx.fill();
    
    // Draw text
    ctx.fillStyle = 'black';
    ctx.font = '20px Arial';
    ctx.fillText('Hello Canvas', 10, 100);
</script>
```

## Web Components (Preview)

Create reusable custom elements:

```html
<!-- Custom element -->
<custom-card title="My Card">
    <p>Card content here</p>
</custom-card>

<script>
    class CustomCard extends HTMLElement {
        connectedCallback() {
            const title = this.getAttribute('title');
            this.innerHTML = `
                <div class="card">
                    <h2>${title}</h2>
                    ${this.innerHTML}
                </div>
            `;
        }
    }
    
    customElements.define('custom-card', CustomCard);
</script>
```

## Template Element

Define reusable HTML templates:

```html
<!-- Define template -->
<template id="product-template">
    <div class="product">
        <h3 class="title"></h3>
        <p class="price"></p>
        <button>Add to Cart</button>
    </div>
</template>

<!-- Use template -->
<div id="products"></div>

<script>
    const template = document.getElementById('product-template');
    const products = document.getElementById('products');
    
    const items = [
        { title: 'Laptop', price: '$999' },
        { title: 'Mouse', price: '$25' }
    ];
    
    items.forEach(item => {
        const clone = template.content.cloneNode(true);
        clone.querySelector('.title').textContent = item.title;
        clone.querySelector('.price').textContent = item.price;
        products.appendChild(clone);
    });
</script>
```

## Details and Summary

Create collapsible sections:

```html
<details>
    <summary>What is HTML?</summary>
    <p>HTML is the standard markup language for web pages...</p>
</details>

<details open>
    <summary>Frequently Asked Questions</summary>
    <dl>
        <dt>Q1: What is CSS?</dt>
        <dd>CSS is used for styling HTML elements.</dd>
    </dl>
</details>
```

## Dialog Element

Create modal dialogs:

```html
<button onclick="document.getElementById('myDialog').showModal()">
    Open Dialog
</button>

<dialog id="myDialog">
    <form method="dialog">
        <h2>Confirm Action</h2>
        <p>Are you sure?</p>
        <button value="cancel">Cancel</button>
        <button value="default">OK</button>
    </form>
</dialog>

<script>
    const dialog = document.getElementById('myDialog');
    dialog.addEventListener('close', (e) => {
        console.log('Dialog result:', dialog.returnValue);
    });
</script>
```

## Meter and Progress

Display measurements and progress:

```html
<!-- Storage usage -->
<label for="storage">Storage Used:</label>
<meter id="storage" value="6" min="0" max="10"></meter>

<!-- Download progress -->
<label for="download">Download Progress:</label>
<progress id="download" value="70" max="100"></progress>
```

## Mark, Wbr, and Ruby

Advanced text elements:

```html
<!-- Highlighted text -->
<p>This is <mark>important</mark> information.</p>

<!-- Word break opportunity -->
<p>thisislongwordthatneedstobrok<wbr>en</p>

<!-- Ruby annotation (for Asian text) -->
<ruby>漢字<rp>(</rp><rt>Kanji</rt><rp>)</rp></ruby>
```

## Output Element

Display calculation results:

```html
<form>
    <input type="number" id="a" value="5">
    +
    <input type="number" id="b" value="3">
    = <output for="a b" id="result"></output>
    
    <script>
        const a = document.getElementById('a');
        const b = document.getElementById('b');
        const result = document.getElementById('result');
        
        function calculate() {
            result.value = parseInt(a.value) + parseInt(b.value);
        }
        
        a.addEventListener('input', calculate);
        b.addEventListener('input', calculate);
        calculate();
    </script>
</form>
```

## Complete Advanced Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Advanced HTML Features</title>
</head>
<body>
    <!-- Custom element -->
    <custom-widget title="Interactive Widget">
        <p>Custom content here</p>
    </custom-widget>
    
    <!-- Details/summary -->
    <details>
        <summary>More Information</summary>
        <p>Detailed information...</p>
    </details>
    
    <!-- Canvas -->
    <canvas id="canvas" width="300" height="200"></canvas>
    
    <!-- Dialog -->
    <button onclick="document.getElementById('dialog').showModal()">
        Open Dialog
    </button>
    <dialog id="dialog">
        <p>This is a modal dialog</p>
        <button onclick="this.closest('dialog').close()">Close</button>
    </dialog>
    
    <!-- Progress -->
    <progress value="65" max="100"></progress>
</body>
</html>
```

## Key Takeaways

✅ Use data attributes for custom data storage

✅ Use SVG for scalable vector graphics

✅ Use Canvas for dynamic graphics

✅ Use Web Components for reusable elements

✅ Use Templates for HTML templates

✅ Use Details/Summary for collapsible content

✅ Use Dialog for modal dialogs

✅ Use Progress/Meter for measurements

---

**End of HTML5 Guide**

**Next: [CSS3 Complete Guide →](../02-css3-complete-guide/README.md)**
