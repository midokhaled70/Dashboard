

# Dashboard Project

A **responsive and interactive dashboard interface** built with **HTML**, **CSS**, and **JavaScript**. Designed for managing tasks, projects, and user information efficiently, it features smooth navigation toggles, context menus, progress indicators, and dynamic content loading.



## Features

* **Responsive Navigation**
  Easily toggle the header’s active state with a navigation button for seamless layout adjustments.

* **Context Menus**
  Access card-specific options like **Edit**, **Refresh**, and **Delete** through intuitive context menus.

* **Load More Button**
  Interactive button with a loading spinner that simulates fetching additional content dynamically.

* **User Profile Section**
  Displays detailed user information, contact details, and progress metrics in a compact panel.

* **Project Cards**
  Highlights recent projects with visual progress bars and team avatars for quick overview.

* **Task List**
  Manage tasks with checkboxes, deadlines, and priority markers for efficient tracking.

* **Revenue Insights**
  Visualizes revenue data alongside comparative metrics to monitor financial performance.

---

## Project Structure

```
dashboard/
├── assets/
│   ├── css/
│   │   └── style.css         # Custom dashboard styles
│   ├── images/
│   │   ├── avatar-1.jpg      # Sample user avatar
│   │   ├── avatar-2.jpg      # Sample user avatar
│   │   └── favicon.svg       # Site favicon
│   └── js/
│       └── script.js         # JavaScript logic for interactivity
├── index.html                # Main HTML entry point
└── README.md                 # Project documentation
```

---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone <repository-url>
cd dashboard
```

### 2. Open the Project

Open the `index.html` file in your preferred web browser.
*No additional server setup is needed since the project uses static files.*

### 3. External Dependencies

* **Fonts:** Uses [Be Vietnam Pro](https://fonts.google.com/specimen/Be+Vietnam+Pro) via Google Fonts CDN
* **Icons:** Uses [Material Symbols](https://fonts.google.com/icons) via Google Fonts CDN

---

## JavaScript Functionality Overview

### Navigation Toggle

Toggles the `active` class on the header element when the navigation button is clicked.

```javascript
const header = document.querySelector("[data-header]");
const navToggleBtn = document.querySelector("[data-menu-toggle-btn]");

navToggleBtn.addEventListener("click", () => {
  header.classList.toggle("active");
});
```

### Context Menu Toggle

Toggles the `active` class on the context menu for each card when the menu button is clicked.

```javascript
const menuButtons = document.querySelectorAll("[data-menu-btn]");

menuButtons.forEach(btn => {
  btn.addEventListener("click", () => {
    btn.nextElementSibling.classList.toggle("active");
  });
});
```

### Load More Button

Toggles a loading spinner on the "Load More" button to simulate fetching more content.

```javascript
const loadMoreBtn = document.querySelector("[data-load-more]");

loadMoreBtn.addEventListener("click", () => {
  loadMoreBtn.classList.toggle("active");
});
```

---

## Usage Guide

* **Navigation:** Click the hamburger menu icon to expand or collapse the navigation sidebar.
* **Context Menus:** Click the three-dot menu on any card to reveal action options.
* **Load More:** Click the "Load More" button to simulate loading additional tasks or projects.

---

## Customization

* **Styles**: Edit `assets/css/style.css` to customize colors, fonts, layout, and responsiveness.
* **Content**: Modify `index.html` to update text, images, or page structure.
* **Interactivity**: Enhance or extend features in `assets/js/script.js` to add new behaviors.

---
## Author
**Mido kha
## Credits

* **Fonts:** [Be Vietnam Pro](https://fonts.google.com/specimen/Be+Vietnam+Pro) by Google Fonts
* **Icons:** [Material Symbols](https://fonts.google.com/icons) by Google Fonts
* ** PhoneNumber:** 01030480083**

---

