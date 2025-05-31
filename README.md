
# Dashboard Project

This is a responsive dashboard interface built with HTML, CSS, and JavaScript. It provides an intuitive layout for managing tasks, projects, and user information, featuring interactive elements like navigation toggles, context menus, and progress indicators.

## Features

- **Responsive Navigation**: Toggle the header's active state using the navigation button.
- **Context Menus**: Click card menu buttons to reveal options like "Edit," "Refresh," and "Delete."
- **Load More Button**: Interactive button with a loading spinner for fetching additional content.
- **User Profile**: Displays user details, contact information, and progress metrics.
- **Project Cards**: Showcases recent projects with progress bars and team avatars.
- **Task List**: Lists tasks with checkboxes, deadlines, and priority indicators.
- **Revenue Insights**: Highlights revenue data with comparison metrics.

## Project Structure

```
dashboard/
├── assets/
│   ├── css/
│   │   └── style.css         # Custom styles for the dashboard
│   ├── images/
│   │   ├── avatar-1.jpg      # Sample avatar image
│   │   ├── avatar-2.jpg      # Sample avatar image
│   │   └── favicon.svg       # Favicon for the page
│   └── js/
│       └── script.js         # JavaScript logic for interactivity
├── index.html                # Main HTML file
└── README.md                 # This file
```

## Setup

1. **Clone the Repository**  
   ```bash
   git clone <repository-url>
   cd dashboard
   ```

2. **Open the Project**  
   Open `index.html` in a web browser to view the dashboard. No additional server setup is required since it uses static files.

3. **Dependencies**  
   - The project uses external Google Fonts (`Be Vietnam Pro`) and Material Symbols for icons, which are loaded via CDN in the HTML `<head>`.

## JavaScript Functionality

The `script.js` file includes the following interactive features:

### 1. Navigation Toggle
Toggles the `active` class on the header when the navigation button is clicked.

```javascript
const header = document.querySelector("[data-header]");
const navToggleBtn = document.querySelector("[data-menu-toggle-btn]");

navToggleBtn.addEventListener("click", function () {
  header.classList.toggle("active");
});
```

### 2. Context Menu Toggle
Toggles the `active` class on the context menu when a card menu button is clicked.

```javascript
const menuBtn = document.querySelectorAll("[data-menu-btn]");

for (let i = 0; i < menuBtn.length; i++) {
  menuBtn[i].addEventListener("click", function () {
    this.nextElementSibling.classList.toggle("active");
  });
}
```

### 3. Load More Button
Toggles the `active` class on the "Load More" button to show a loading spinner.

```javascript
const loadMoreBtn = document.querySelector("[data-load-more]");

loadMoreBtn.addEventListener("click", function () {
  this.classList.toggle("active");
});
```

## Usage

- **Navigation**: Click the menu icon in the header to expand/collapse the navigation bar.
- **Context Menus**: Click the "More" (three dots) icon on cards to view options.
- **Load More**: Click the "Load More" button in the tasks section to simulate loading additional tasks.

## Customization

- **Styles**: Modify `assets/css/style.css` to adjust colors, layouts, or responsiveness.
- **Content**: Update `index.html` to change text, images, or data values.
- **Functionality**: Extend `assets/js/script.js` to add more interactivity or features.

## Credits

- **Fonts**: [Be Vietnam Pro](https://fonts.google.com/specimen/Be+Vietnam+Pro) via Google Fonts.
- **Icons**: [Material Symbols](https://fonts.google.com/icons) via Google Fonts.
- **Author**: © 2025 MIDOKHALED.

