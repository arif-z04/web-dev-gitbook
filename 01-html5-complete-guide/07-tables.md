# 7. Tables

## Table Structure

Tables organize data into rows and columns:

```html
<table>
    <thead>
        <tr>
            <th>Header 1</th>
            <th>Header 2</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Data 1</td>
            <td>Data 2</td>
        </tr>
    </tbody>
</table>
```

## Table Elements

### `<table>`
Container for all table content

### `<thead>`
Groups header rows

### `<tbody>`
Groups body rows

### `<tfoot>`
Groups footer rows

### `<tr>`
Table row

### `<th>`
Table header cell

### `<td>`
Table data cell

### `<caption>`
Table title/description

## Basic Table Example

```html
<table>
    <caption>Student Grades</caption>
    <thead>
        <tr>
            <th>Student Name</th>
            <th>Math</th>
            <th>English</th>
            <th>Science</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>John Smith</td>
            <td>92</td>
            <td>88</td>
            <td>95</td>
        </tr>
        <tr>
            <td>Jane Doe</td>
            <td>95</td>
            <td>91</td>
            <td>93</td>
        </tr>
        <tr>
            <td>Bob Johnson</td>
            <td>87</td>
            <td>89</td>
            <td>85</td>
        </tr>
    </tbody>
</table>
```

## Table with Footer

```html
<table>
    <thead>
        <tr>
            <th>Product</th>
            <th>Price</th>
            <th>Quantity</th>
            <th>Total</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Laptop</td>
            <td>$999</td>
            <td>2</td>
            <td>$1998</td>
        </tr>
        <tr>
            <td>Mouse</td>
            <td>$25</td>
            <td>5</td>
            <td>$125</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <th>Total</th>
            <td colspan="3">$2123</td>
        </tr>
    </tfoot>
</table>
```

## Spanning Cells

### colspan (Span Across Columns)

```html
<table>
    <tr>
        <th colspan="2">Full Name</th>
        <th>Grade</th>
    </tr>
    <tr>
        <td>John</td>
        <td>Smith</td>
        <td>A</td>
    </tr>
</table>
```

### rowspan (Span Across Rows)

```html
<table>
    <tr>
        <th>Month</th>
        <th>Sales</th>
    </tr>
    <tr>
        <td rowspan="3">Q1</td>
        <td>January: $10,000</td>
    </tr>
    <tr>
        <td>February: $12,000</td>
    </tr>
    <tr>
        <td>March: $11,000</td>
    </tr>
</table>
```

## Table Accessibility

### scope Attribute

```html
<table>
    <thead>
        <tr>
            <th scope="col">Name</th>
            <th scope="col">Email</th>
            <th scope="col">Role</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th scope="row">Alice</th>
            <td>alice@example.com</td>
            <td>Manager</td>
        </tr>
        <tr>
            <th scope="row">Bob</th>
            <td>bob@example.com</td>
            <td>Developer</td>
        </tr>
    </tbody>
</table>
```

### headers Attribute

For complex tables:

```html
<table>
    <thead>
        <tr>
            <th id="name">Name</th>
            <th id="q1">Q1 2026</th>
            <th id="q2">Q2 2026</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th headers="name">Product A</th>
            <td headers="q1">$50,000</td>
            <td headers="q2">$55,000</td>
        </tr>
    </tbody>
</table>
```

## Responsive Tables

### CSS for Responsive Tables

```css
/* Stack columns on small screens */
@media (max-width: 768px) {
    table, thead, tbody, th, td, tr {
        display: block;
    }
    
    thead tr {
        position: absolute;
        top: -9999px;
        left: -9999px;
    }
    
    tr {
        margin-bottom: 1rem;
    }
    
    td {
        position: relative;
        padding-left: 50%;
    }
    
    td:before {
        content: attr(data-label);
        position: absolute;
        left: 0;
        font-weight: bold;
    }
}
```

### Responsive Table HTML

```html
<table>
    <thead>
        <tr>
            <th>Product</th>
            <th>Price</th>
            <th>Stock</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td data-label="Product">Laptop</td>
            <td data-label="Price">$999</td>
            <td data-label="Stock">5</td>
        </tr>
        <tr>
            <td data-label="Product">Mouse</td>
            <td data-label="Price">$25</td>
            <td data-label="Stock">12</td>
        </tr>
    </tbody>
</table>
```

## Complex Table Example

```html
<table>
    <caption>Company Sales Report Q1 2026</caption>
    <thead>
        <tr>
            <th scope="col">Region</th>
            <th scope="col">Product</th>
            <th scope="col">January</th>
            <th scope="col">February</th>
            <th scope="col">March</th>
            <th scope="col">Total</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th scope="row" rowspan="2">North America</th>
            <td>Software</td>
            <td>$150,000</td>
            <td>$160,000</td>
            <td>$170,000</td>
            <td>$480,000</td>
        </tr>
        <tr>
            <td>Services</td>
            <td>$80,000</td>
            <td>$85,000</td>
            <td>$90,000</td>
            <td>$255,000</td>
        </tr>
        <tr>
            <th scope="row" rowspan="2">Europe</th>
            <td>Software</td>
            <td>$120,000</td>
            <td>$130,000</td>
            <td>$140,000</td>
            <td>$390,000</td>
        </tr>
        <tr>
            <td>Services</td>
            <td>$60,000</td>
            <td>$70,000</td>
            <td>$75,000</td>
            <td>$205,000</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <th colspan="2">Grand Total</th>
            <td>$410,000</td>
            <td>$445,000</td>
            <td>$475,000</td>
            <td>$1,330,000</td>
        </tr>
    </tfoot>
</table>
```

## Table Styling Tips

```css
/* Basic table styling */
table {
    width: 100%;
    border-collapse: collapse;
    margin: 1rem 0;
}

th, td {
    border: 1px solid #ddd;
    padding: 0.75rem;
    text-align: left;
}

thead {
    background-color: #f8f9fa;
    font-weight: bold;
}

tbody tr:nth-child(even) {
    background-color: #f8f9fa;
}

tbody tr:hover {
    background-color: #e9ecef;
}
```

## Common Mistakes

❌ **Using tables for layout**:
```html
<!-- Wrong: Using table for page layout -->
<table>
    <tr>
        <td>Header</td>
    </tr>
    <tr>
        <td>Sidebar</td>
        <td>Content</td>
    </tr>
</table>

<!-- Right: Use CSS for layout -->
<header>Header</header>
<div class="container">
    <aside>Sidebar</aside>
    <main>Content</main>
</div>
```

❌ **Missing table structure**:
```html
<!-- Wrong -->
<table>
    <tr><th>Name</th><th>Age</th></tr>
    <tr><td>John</td><td>30</td></tr>
</table>

<!-- Right -->
<table>
    <thead>
        <tr><th>Name</th><th>Age</th></tr>
    </thead>
    <tbody>
        <tr><td>John</td><td>30</td></tr>
    </tbody>
</table>
```

❌ **Missing accessibility attributes**:
```html
<!-- Less accessible -->
<table>
    <tr><td>Name</td></tr>
    <tr><td>John</td></tr>
</table>

<!-- More accessible -->
<table>
    <thead>
        <tr><th scope="col">Name</th></tr>
    </thead>
    <tbody>
        <tr><th scope="row">John</th></tr>
    </tbody>
</table>
```

## Key Takeaways

✅ Use `<thead>`, `<tbody>`, `<tfoot>` for semantic structure

✅ Use `<th scope="col|row">` for accessibility

✅ Use `<caption>` to describe the table

✅ Never use tables for layout

✅ Use colspan/rowspan for cell spanning

✅ Make tables responsive with CSS

✅ Use proper semantic elements

---

**Next: [Forms →](08-forms.md)**
