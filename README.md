# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.Here’s an example of how to create a responsive layout using **Flexbox** and **CSS Grid**, including a navigation bar and content structure. We'll also use media queries to adjust the layout for mobile, tablet, and desktop devices.

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <header>
        <nav class="navbar">
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main class="content">
        <section class="intro">
            <h1>Welcome to Our Website</h1>
            <p>We offer great services.</p>
        </section>

        <section class="services">
            <div class="service-item">Service 1</div>
            <div class="service-item">Service 2</div>
            <div class="service-item">Service 3</div>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 Company Name</p>
    </footer>

</body>
</html>
```

### CSS (styles.css)

```css
/* General Styles */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Navigation Bar */
.navbar {
    background-color: #333;
    padding: 10px;
}

.navbar ul {
    display: flex;
    list-style-type: none;
    justify-content: center;
    margin: 0;
    padding: 0;
}

.navbar ul li {
    margin: 0 15px;
}

.navbar ul li a {
    color: white;
    text-decoration: none;
    font-size: 16px;
}

.navbar ul li a:hover {
    text-decoration: underline;
}

/* Content Layout */
.content {
    display: grid;
    grid-template-columns: 1fr;
    gap: 20px;
    padding: 20px;
}

.intro {
    text-align: center;
}

.services {
    display: grid;
    grid-template-columns: 1fr;
    gap: 10px;
    justify-items: center;
}

.service-item {
    background-color: #f4f4f4;
    padding: 20px;
    border-radius: 8px;
    text-align: center;
    width: 100%;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px;
}

/* Media Queries */

/* Tablet Layout */
@media (min-width: 600px) {
    .content {
        grid-template-columns: repeat(2, 1fr);
    }

    .services {
        grid-template-columns: repeat(2, 1fr);
    }
}

/* Desktop Layout */
@media (min-width: 1024px) {
    .content {
        grid-template-columns: repeat(3, 1fr);
    }

    .services {
        grid-template-columns: repeat(3, 1fr);
    }
}
```

### Explanation:

1. **Navigation Bar:**
   - The `.navbar` uses **Flexbox** to horizontally arrange the navigation items and center them.
   - We have `display: flex;` on the `ul` element to create a flexible container and space the list items horizontally.
   - Links are styled for better visibility and user interaction with `:hover` effects.

2. **Main Content Structure:**
   - The `.content` section is styled using **CSS Grid**. Initially, it has a single column layout for mobile devices.
   - The `.services` section also uses **CSS Grid** to structure the services in a single column on mobile devices.

3. **Responsive Layout with Media Queries:**
   - For **tablet devices** (width ≥ 600px), the `.content` and `.services` sections switch to two columns using `grid-template-columns: repeat(2, 1fr);`.
   - For **desktop devices** (width ≥ 1024px), the `.content` and `.services` sections switch to three columns using `grid-template-columns: repeat(3, 1fr);`.
   - These breakpoints help ensure the layout adjusts as the screen size increases.

### Result:
- On **mobile devices**, the layout will display one column.
- On **tablet devices**, the layout will switch to two columns.
- On **desktop devices**, the layout will use three columns.

This structure provides a responsive design that adapts gracefully to different screen sizes using Flexbox and CSS Grid, with media queries for specific adjustments.
- 

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨
