# Complete Source Code

## index.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Professional portfolio showcasing my web development projects">
    <meta property="og:title" content="My Portfolio - Web Developer">
    <meta property="og:description" content="Check out my web development projects">
    <meta property="og:image" content="images/hero.jpg">
    
    <title>My Portfolio - Web Developer</title>
    <link rel="icon" href="favicon.ico">
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <!-- Navigation -->
    <header class="navbar">
        <div class="container">
            <div class="nav-wrapper">
                <h1 class="logo">My Portfolio</h1>
                <button class="menu-toggle" id="menuToggle">☰ Menu</button>
                <nav class="nav-menu" id="navMenu">
                    <a href="#home" class="nav-link">Home</a>
                    <a href="#about" class="nav-link">About</a>
                    <a href="#projects" class="nav-link">Projects</a>
                    <a href="#contact" class="nav-link">Contact</a>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h2>Welcome to My Portfolio</h2>
                <p>I'm a web developer passionate about creating beautiful, responsive websites</p>
                <button class="btn btn-primary" onclick="document.getElementById('projects').scrollIntoView({behavior: 'smooth'})">
                    View My Work
                </button>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <h2>About Me</h2>
            <div class="about-content">
                <img src="images/profile.jpg" alt="My profile photo" class="profile-img">
                <div class="about-text">
                    <p>
                        I'm a passionate web developer with expertise in HTML5, CSS3, and JavaScript. 
                        I love creating responsive, accessible websites that provide excellent user experiences.
                    </p>
                    <h3>Skills</h3>
                    <ul>
                        <li>HTML5 & Semantic Markup</li>
                        <li>CSS3 & Responsive Design</li>
                        <li>JavaScript & Interactivity</li>
                        <li>Web Accessibility</li>
                        <li>SEO Optimization</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section class="projects" id="projects">
        <div class="container">
            <h2>Featured Projects</h2>
            <div class="projects-grid">
                <article class="project-card">
                    <img src="images/project-1.jpg" alt="E-commerce website project">
                    <h3>E-commerce Website</h3>
                    <p>A fully responsive online store built with HTML5 and CSS3</p>
                    <a href="#" class="btn btn-secondary">View Project</a>
                </article>

                <article class="project-card">
                    <img src="images/project-2.jpg" alt="Blog platform project">
                    <h3>Blog Platform</h3>
                    <p>A modern blog with responsive design and SEO optimization</p>
                    <a href="#" class="btn btn-secondary">View Project</a>
                </article>

                <article class="project-card">
                    <img src="images/project-3.jpg" alt="Portfolio website project">
                    <h3>Portfolio Website</h3>
                    <p>A sleek portfolio showcasing web development projects</p>
                    <a href="#" class="btn btn-secondary">View Project</a>
                </article>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <h2>Get In Touch</h2>
            <form class="contact-form" id="contactForm">
                <div class="form-group">
                    <label for="name">Name:</label>
                    <input type="text" id="name" name="name" required>
                </div>

                <div class="form-group">
                    <label for="email">Email:</label>
                    <input type="email" id="email" name="email" required>
                </div>

                <div class="form-group">
                    <label for="message">Message:</label>
                    <textarea id="message" name="message" rows="5" required></textarea>
                </div>

                <button type="submit" class="btn btn-primary">Send Message</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <p>&copy; 2026 My Portfolio. All rights reserved.</p>
            <nav class="footer-links">
                <a href="#">Privacy Policy</a> |
                <a href="#">Terms of Service</a> |
                <a href="#">Contact</a>
            </nav>
        </div>
    </footer>

    <script src="js/script.js"></script>
</body>
</html>
```

## css/style.css

```css
/* Reset and defaults */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

:root {
    --primary-color: #007bff;
    --secondary-color: #6c757d;
    --success-color: #28a745;
    --danger-color: #dc3545;
    --light-bg: #f8f9fa;
    --dark-text: #333;
    --border-color: #dee2e6;
    --font-stack: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    font-family: var(--font-stack);
    line-height: 1.6;
    color: var(--dark-text);
    font-size: 16px;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

/* Navigation */
.navbar {
    background-color: #333;
    color: white;
    padding: 20px 0;
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.nav-wrapper {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    margin: 0;
    font-size: 24px;
}

.menu-toggle {
    display: block;
    background: none;
    border: none;
    color: white;
    font-size: 24px;
    cursor: pointer;
}

.nav-menu {
    display: none;
    position: absolute;
    top: 70px;
    left: 0;
    right: 0;
    background: #333;
    flex-direction: column;
    padding: 20px;
    gap: 10px;
}

.nav-menu.active {
    display: flex;
}

.nav-link {
    color: white;
    text-decoration: none;
    padding: 10px 0;
    display: block;
    border-bottom: 1px solid #444;
}

.nav-link:hover {
    color: var(--primary-color);
}

@media (min-width: 768px) {
    .menu-toggle {
        display: none;
    }
    
    .nav-menu {
        display: flex !important;
        position: static;
        flex-direction: row;
        padding: 0;
        gap: 30px;
        background: none;
    }
    
    .nav-link {
        border: none;
        padding: 0;
    }
}

/* Hero Section */
.hero {
    background: linear-gradient(135deg, var(--primary-color), #0056b3);
    color: white;
    padding: 100px 20px;
    text-align: center;
}

.hero-content h2 {
    font-size: clamp(28px, 5vw, 48px);
    margin-bottom: 20px;
}

.hero-content p {
    font-size: 18px;
    margin-bottom: 30px;
}

/* Buttons */
.btn {
    display: inline-block;
    padding: 12px 30px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
    text-decoration: none;
    transition: all 0.3s ease;
}

.btn-primary {
    background-color: var(--primary-color);
    color: white;
}

.btn-primary:hover {
    background-color: #0056b3;
    transform: translateY(-2px);
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}

.btn-secondary {
    background-color: var(--secondary-color);
    color: white;
}

.btn-secondary:hover {
    background-color: #5a6268;
}

/* About Section */
.about {
    padding: 60px 20px;
    background-color: var(--light-bg);
}

.about h2 {
    text-align: center;
    font-size: 36px;
    margin-bottom: 40px;
}

.about-content {
    display: flex;
    flex-direction: column;
    gap: 40px;
    align-items: center;
}

.profile-img {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    object-fit: cover;
    border: 4px solid var(--primary-color);
}

.about-text ul {
    list-style: none;
    margin-left: 0;
}

.about-text li {
    padding: 8px 0;
    padding-left: 25px;
    position: relative;
}

.about-text li:before {
    content: "✓";
    position: absolute;
    left: 0;
    color: var(--success-color);
    font-weight: bold;
}

@media (min-width: 768px) {
    .about-content {
        flex-direction: row;
        align-items: flex-start;
    }
    
    .profile-img {
        flex-shrink: 0;
    }
    
    .about-text {
        flex: 1;
    }
}

/* Projects Section */
.projects {
    padding: 60px 20px;
}

.projects h2 {
    text-align: center;
    font-size: 36px;
    margin-bottom: 40px;
}

.projects-grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 30px;
}

@media (min-width: 768px) {
    .projects-grid {
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    }
}

.project-card {
    background: white;
    border: 1px solid var(--border-color);
    border-radius: 8px;
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 16px rgba(0,0,0,0.1);
}

.project-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    display: block;
}

.project-card h3 {
    padding: 20px 20px 10px;
    font-size: 20px;
}

.project-card p {
    padding: 0 20px 20px;
    color: #666;
}

.project-card .btn {
    margin: 20px;
    width: calc(100% - 40px);
    text-align: center;
}

/* Contact Section */
.contact {
    padding: 60px 20px;
    background-color: var(--light-bg);
}

.contact h2 {
    text-align: center;
    font-size: 36px;
    margin-bottom: 40px;
}

.contact-form {
    max-width: 600px;
    margin: 0 auto;
}

.form-group {
    margin-bottom: 20px;
}

label {
    display: block;
    margin-bottom: 8px;
    font-weight: bold;
}

input[type="text"],
input[type="email"],
textarea {
    width: 100%;
    padding: 10px;
    border: 1px solid var(--border-color);
    border-radius: 4px;
    font-family: var(--font-stack);
    font-size: 16px;
}

textarea {
    resize: vertical;
    min-height: 150px;
}

input[type="text"]:focus,
input[type="email"]:focus,
textarea:focus {
    outline: none;
    border-color: var(--primary-color);
    box-shadow: 0 0 0 2px rgba(0,123,255,0.25);
}

.contact-form .btn {
    width: 100%;
}

/* Footer */
.footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 40px 20px;
    margin-top: 60px;
}

.footer-links {
    margin-top: 20px;
}

.footer-links a {
    color: white;
    text-decoration: none;
    margin: 0 10px;
}

.footer-links a:hover {
    color: var(--primary-color);
}

/* Typography */
h1, h2, h3 {
    color: var(--dark-text);
}

h2 {
    font-size: 32px;
    margin-bottom: 20px;
}

h3 {
    font-size: 24px;
}

/* Accessibility */
@media (prefers-reduced-motion: reduce) {
    * {
        animation: none !important;
        transition: none !important;
    }
}

/* High contrast mode support */
@media (prefers-contrast: more) {
    .btn-primary {
        border: 2px solid white;
    }
}
```

## js/script.js

```javascript
// Mobile menu toggle
const menuToggle = document.getElementById('menuToggle');
const navMenu = document.getElementById('navMenu');
const navLinks = document.querySelectorAll('.nav-link');

menuToggle.addEventListener('click', () => {
    navMenu.classList.toggle('active');
});

// Close menu when link is clicked
navLinks.forEach(link => {
    link.addEventListener('click', () => {
        navMenu.classList.remove('active');
    });
});

// Form validation
const contactForm = document.getElementById('contactForm');
if (contactForm) {
    contactForm.addEventListener('submit', (e) => {
        e.preventDefault();
        
        // Get form values
        const name = document.getElementById('name').value;
        const email = document.getElementById('email').value;
        const message = document.getElementById('message').value;
        
        // Simple validation
        if (!name || !email || !message) {
            alert('Please fill in all fields');
            return;
        }
        
        // Show success message
        alert('Thank you for your message! I will get back to you soon.');
        contactForm.reset();
    });
}

// Smooth scrolling for navigation
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
            target.scrollIntoView({
                behavior: 'smooth',
                block: 'start'
            });
        }
    });
});
```

---

**Next: [Step-by-Step Guide →](04-step-by-step-guide.md)**
