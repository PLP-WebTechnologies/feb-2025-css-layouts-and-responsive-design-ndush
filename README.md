# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Layout</title>
  <style>
    /* Basic Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
    }

    /* Navbar Styling */
    nav {
      background-color: #333;
      padding: 10px;
      color: #fff;
    }

    nav ul {
      list-style: none;
      display: flex;
      justify-content: space-around;
    }

    nav ul li {
      padding: 10px;
    }

    nav ul li a {
      color: white;
      text-decoration: none;
    }

    /* Layout using Flexbox */
    .container {
      display: flex;
      flex-direction: column;
      padding: 20px;
    }

    .header, .main, .footer {
      background-color: #fff;
      margin: 10px 0;
      padding: 20px;
      border-radius: 8px;
    }

    .main {
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 20px;
    }

    .sidebar {
      background-color: #e2e2e2;
      padding: 15px;
      border-radius: 8px;
    }

    .content {
      background-color: #f9f9f9;
      padding: 15px;
      border-radius: 8px;
    }

    /* Media Queries */
    @media (max-width: 768px) {
      .main {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 480px) {
      nav ul {
        flex-direction: column;
        align-items: center;
      }

      nav ul li {
        padding: 15px;
      }

      .container {
        padding: 10px;
      }

      .header, .footer {
        text-align: center;
      }
    }
  </style>
</head>
<body>

  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <div class="container">
    <div class="header">
      <h1>Responsive Layout Example</h1>
    </div>
    
    <div class="main">
      <div class="sidebar">
        <h3>Sidebar</h3>
        <p>Some sidebar content goes here.</p>
      </div>
      <div class="content">
        <h2>Main Content</h2>
        <p>This is the main content area. It adjusts based on screen size.</p>
      </div>
    </div>
    
    <div class="footer">
      <p>&copy; 2025 Responsive Layout. All rights reserved.</p>
    </div>
  </div>

</body>
</html>
