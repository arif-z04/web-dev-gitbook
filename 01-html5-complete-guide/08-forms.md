# 8. Forms

## The Form Element

```html
<form action="/submit" method="POST">
    <!-- Form controls here -->
</form>
```

## Form Attributes

### action
Specifies where form data is sent

### method
- `GET` - Send data in URL (for searches, filters)
- `POST` - Send data in request body (for sensitive data)

### enctype
- `application/x-www-form-urlencoded` - Default
- `multipart/form-data` - For file uploads
- `text/plain` - Plain text

## Form Controls

### Text Inputs

```html
<!-- Single line text -->
<input type="text" name="username" placeholder="Enter username">

<!-- Email -->
<input type="email" name="email" placeholder="your@email.com">

<!-- Password -->
<input type="password" name="password" placeholder="Enter password">

<!-- URL -->
<input type="url" name="website" placeholder="https://example.com">

<!-- Telephone -->
<input type="tel" name="phone" placeholder="(123) 456-7890">

<!-- Search -->
<input type="search" name="search" placeholder="Search...">
```

### Numeric Inputs

```html
<!-- Number -->
<input type="number" name="age" min="0" max="120">

<!-- Range slider -->
<input type="range" name="volume" min="0" max="100">
```

### Date and Time

```html
<!-- Date picker -->
<input type="date" name="birthday">

<!-- Time picker -->
<input type="time" name="appointment">

<!-- Date and time -->
<input type="datetime-local" name="meeting">

<!-- Month -->
<input type="month" name="start-month">

<!-- Week -->
<input type="week" name="week">
```

### Checkboxes and Radio Buttons

```html
<!-- Checkboxes -->
<input type="checkbox" name="terms" id="terms">
<label for="terms">I agree to the terms</label>

<input type="checkbox" name="newsletter" id="newsletter">
<label for="newsletter">Subscribe to newsletter</label>

<!-- Radio buttons -->
<input type="radio" name="gender" value="male" id="male">
<label for="male">Male</label>

<input type="radio" name="gender" value="female" id="female">
<label for="female">Female</label>

<input type="radio" name="gender" value="other" id="other">
<label for="other">Other</label>
```

### File Upload

```html
<input type="file" name="avatar" accept="image/*">

<!-- Multiple files -->
<input type="file" name="documents" multiple accept=".pdf,.doc,.docx">
```

### Color Picker

```html
<input type="color" name="favorite-color" value="#ff0000">
```

### Email and Password

```html
<input type="email" name="email" required>
<input type="password" name="password" required>
```

## Labels

Always associate labels with inputs:

```html
<!-- Good -->
<label for="username">Username:</label>
<input type="text" id="username" name="username">

<!-- Bad -->
<label>Username:</label>
<input type="text" name="username">
```

## Textarea

Multi-line text input:

```html
<label for="message">Message:</label>
<textarea 
    id="message" 
    name="message" 
    rows="5" 
    cols="40"
    placeholder="Enter your message here..."
></textarea>
```

## Select Dropdown

```html
<label for="country">Country:</label>
<select id="country" name="country">
    <option value="">Select a country</option>
    <option value="us">United States</option>
    <option value="uk">United Kingdom</option>
    <option value="ca">Canada</option>
</select>

<!-- Grouped options -->
<select name="region">
    <optgroup label="North America">
        <option value="us">United States</option>
        <option value="ca">Canada</option>
    </optgroup>
    <optgroup label="Europe">
        <option value="uk">United Kingdom</option>
        <option value="fr">France</option>
    </optgroup>
</select>
```

## Buttons

```html
<!-- Submit button -->
<button type="submit">Submit Form</button>

<!-- Reset button -->
<button type="reset">Clear Form</button>

<!-- Regular button -->
<button type="button" onclick="alert('Clicked!')">Click Me</button>

<!-- Link styled as button -->
<a href="/cancel" class="button">Cancel</a>
```

## Form Validation

### HTML5 Built-in Validation

```html
<!-- Required field -->
<input type="email" required>

<!-- Pattern validation -->
<input type="text" pattern="[A-Z]{3}[0-9]{3}" placeholder="ABC123">

<!-- Min/Max for numbers -->
<input type="number" min="0" max="100">

<!-- Min/Max for length -->
<input type="text" minlength="5" maxlength="20">
```

### Validation Messages

```html
<form>
    <input type="email" name="email" required title="Please enter a valid email">
    <button type="submit">Submit</button>
</form>
```

## Complete Form Example

```html
<form action="/register" method="POST" novalidate>
    <fieldset>
        <legend>Personal Information</legend>
        
        <div class="form-group">
            <label for="firstname">First Name:</label>
            <input 
                type="text" 
                id="firstname" 
                name="firstname" 
                required>
        </div>
        
        <div class="form-group">
            <label for="lastname">Last Name:</label>
            <input 
                type="text" 
                id="lastname" 
                name="lastname" 
                required>
        </div>
        
        <div class="form-group">
            <label for="email">Email:</label>
            <input 
                type="email" 
                id="email" 
                name="email" 
                required>
        </div>
    </fieldset>
    
    <fieldset>
        <legend>Account Settings</legend>
        
        <div class="form-group">
            <label for="password">Password:</label>
            <input 
                type="password" 
                id="password" 
                name="password" 
                minlength="8" 
                required>
        </div>
        
        <div class="form-group">
            <label for="country">Country:</label>
            <select id="country" name="country" required>
                <option value="">Select...</option>
                <option value="us">United States</option>
                <option value="uk">United Kingdom</option>
            </select>
        </div>
        
        <div class="form-group">
            <input 
                type="checkbox" 
                id="terms" 
                name="terms" 
                required>
            <label for="terms">I agree to the terms and conditions</label>
        </div>
    </fieldset>
    
    <button type="submit">Create Account</button>
    <button type="reset">Clear Form</button>
</form>
```

## Key Takeaways

✅ Always use proper input types

✅ Associate labels with inputs using `for` attribute

✅ Use validation attributes

✅ Use `<fieldset>` and `<legend>` for organization

✅ Provide clear error messages

✅ Consider accessibility in form design

---

**Next: [Multimedia →](09-multimedia.md)**
